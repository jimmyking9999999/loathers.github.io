# ASH

## Using Common ASH Functions (via Example)

There are a number of useful starter ASH tutorials on the KoLMafia wiki and scattered about Mafia's old home on sourceforge. One that I find particularly useful is [this set of two basic examples of ASH scripts](https://kolmafia.sourceforge.io/advanced.html). At a high level, when thinking about how to use ASH (or, really, any new programming language), the best way to go about it is to start with a small abstract piece of something useful and extend your reach beyond it by bringing in things that add complication and heft to the initial goal. As a start, let's use a very simple, very effective use-case: drinking a nightcap, via the "drink" command.

```ash
drink(1,$item[emergency margarita]);
```

This is easy and straightforward. You could simply save this as nightCap.ash, run it at the end of every day, and you'd be good on your last drink of the day so long as you always had an Emergency Margarita in your inventory. But what if you didn't? It turns out nightcaps can be a bit more complicated! Let's add a check that purchases an emergency margarita for you, if you don't have one lying around.

```ash
item nightcap = $item[emergency margarita];

if (available_amount(nightcap) == 0) buy(1, nightcap);

drink(1, nightcap);
```

But wait! What if a nefarious actor bought up every single emergency margarita in the mall? Computers are smart, but they're also extraordinarily literal -- if you tell it to purchase a margarita, it will do so, no matter how much meat they cost. Let's add a catch that aborts if margaritas become way too expensive to justify.

```ash
item nightcap = $item[emergency margarita];

if (available_amount(nightcap) == 0) buy(1, nightcap, 60000);

if (available_amount(nightcap) == 0) {
  print("Margs are too pricy for me", "red");
  abort();
}

drink(1, nightcap);
```

There's another issue here -- this code doesn't actually take into account how much drunkenness you have. What if you actually forgot to drink a few points of liver before you ran the script? That might equate to lost adventures, and that just won't do. Let's add a function to this that fills your liver with splendid martinis before the margarita is consumed.

```ash
item filler = $item[splendid martini];
while (my_inebriety() < inebriety_limit()) {
  if (available_amount(filler) == 0) buy(1, filler, 10000);
  if (available_amount(filler) == 0) {
    print("Splendids are too pricy for me", "red");
    abort();
  }
  drink(1, filler);
}

item nightcap = $item[emergency margarita];

if (available_amount(nightcap) == 0) buy(1, nightcap, 60000);

if (available_amount(nightcap) == 0) {
  print("Margs are too pricy for me", "red");
  abort();
}

drink(1, nightcap);
```

Please note that while loops can be very dangerous; you need to make sure that what you are doing increments, and if it doesn't, you need to include some sort of catch that allows it to break out of an infinite loop. Regardless, there's one last issue here. What about Stooper, the familiar that gives you +1 drunkenness? Let's make sure we're equipping our little buddy for the extra turns.

```ash
if (have_familiar($familiar[stooper])) use_familiar($familiar[stooper]);
item filler = $item[splendid martini];
while (my_inebriety() < inebriety_limit()) {
  if (available_amount(filler) == 0) buy(1, filler, 10000);
  if (available_amount(filler) == 0) {
    print("Splendids are too pricy for me", "red");
    abort();
  }
  drink(1, filler);
}

item nightcap = $item[emergency margarita];

if (available_amount(nightcap) == 0) buy(1, nightcap, 60000);

if (available_amount(nightcap) == 0) {
  print("Margs are too pricy for me", "red");
  abort();
}

drink(1, nightcap);
```

Oh, wait. One last thing! Why not maximize our outfit for adventures, so that this can truly be the last thing we do for the day? Might as well, right?

```ash
if (have_familiar($familiar[stooper])) use_familiar($familiar[stooper]);
item filler = $item[splendid martini];
while (my_inebriety() < inebriety_limit()) {
  if (available_amount(filler) == 0) buy(1, filler, 10000);
  if (available_amount(filler) == 0) {
    print("Splendids are too pricy for me", "red");
    abort();
  }
  drink(1, filler);
}

item nightcap = $item[emergency margarita];

if (available_amount(nightcap) == 0) buy(1, nightcap, 60000);

if (available_amount(nightcap) == 0) {
  print("Margs are too pricy for me", "red");
  abort();
}

drink(1, nightcap);

if (have_familiar($familiar[left-hand man])) use_familiar($familiar[left-hand man]);
maximize("Adventures", false);
```

Fantastic. We have a script. We went from a very simple [drink()](https://wiki.kolmafia.us/index.php/Drink) statement into a compact script that manages to use quite a few functions in its operation, including [have](https://wiki.kolmafia.us/index.php/Have_familiar)/[use_familiar](https://wiki.kolmafia.us/index.php/Use_familiar), the [$item datatype](https://wiki.kolmafia.us/index.php/Item), [my_inebriety](https://wiki.kolmafia.us/index.php/My_inebriety), [available_amount](https://wiki.kolmafia.us/index.php/Available_amount), [print](https://wiki.kolmafia.us/index.php/Print) statements, [control flow with while/if/abort](https://wiki.kolmafia.us/index.php/Control_Structures), and the notoriously useful [maximize()](https://wiki.kolmafia.us/index.php/Maximize). Pretty cool!

When you're building your own scripts, one of the best ways to learn is to simply pick a simple task and start thinking through what kind of complications could make a simple thing less straightforward. When you figure those out, and start solving them via mafia functions, you quickly turn a very simple one-line script into a larger scale construction that teaches you about all sorts of new functions and commands.

## Examples of High-Level ASH Code

TheDictator (a player /dev) has many complex ASH scripts available on [his pastebin](https://pastebin.com/u/thedictator).

[Autoscend](https://github.com/Loathing-Associates-Scripting-Society/autoscend) is a LASS-maintained general-use ascension script written in ASH.

Notoriously prolific KoL scripter [Ezandora](https://github.com/Ezandora) has scores of ASH scripts available on her github.

Finally, as you develop your own scripts, be sure to check the [KoLMafia forums](https://kolmafia.us/), where you can find an entire repository with years and years of ASH scripts -- some burn turns, some change your KOL relay experience, and [some even put an entire decision tree of complex logic behind every combat](https://kolmafia.us/threads/batbrain-a-central-nervous-system-for-consult-scripts.6445/)!

## The Pros and Cons of ASH

| Pros                                                                           | Cons                                                      |
| ------------------------------------------------------------------------------ | --------------------------------------------------------- |
| Quick & easy to use for short and simple scripts; can deploy without any delay | Can get messy when doing more complicated processes       |
| Automatically can access all KoLMafia functions, doesn't require importing     | As it is KoL-specific, solving errors can be a bit harder |
| Very easy to find KOL-specific examples for how to do things in ASH            | Has a _ton_ of administrative overhaul in large scripts   |
