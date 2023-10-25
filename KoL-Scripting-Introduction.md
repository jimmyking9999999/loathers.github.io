# Introduction

## Why script KoL?

When the Kingdom of Loathing (KoL) was first created, it was designed to be a game you could play during your coffee break. Each day you have 40 adventures, and you can spend them fighting Knob Goblins or Fiendish Cans of Asparagus or crafting advanced cocktails. At this point, however, KoL has evolved into a game of enormous scope. You may have thousands of turns to play in a day. You may have hundreds of resources to use. For many players, it is impractical to try to do everything by hand.

If you're reading this, you probably already use [KoLMafia](https://wiki.kolmafia.us/index.php/KoLmafia_Guide). It's a fantastic tool to help play turns quickly and efficiently. With scripts written in ASH or JavaScript, you can have KoLMafia make gameplay decisions for you and execute them: you can automate adventuring, inventory management, and even KMails. Hell, you've probably already used some scripts -- [autoscend](https://github.com/Loathing-Associates-Scripting-Society/autoscend) and [garbage collector](https://github.com/Loathing-Associates-Scripting-Society/garbage-collector) are two popular scripts that we here at LASS produce, and there are dozens of other scripts that help automate play, simplify resources, and make the game a better experience for everyone.

But everyone's specific needs and goals are different. It's likely that there's something you want to do in KoL that isn't currently supported by a script. Maybe you have a great idea for improving an existing script, or maybe you need to automate a task that no one has a public script that does. Whatever you need to do in this game, there's probably a way to make it better through scripting.

## What are the tools and resources available for scripting KoL?

There are a number of useful resources you should leverage as you start learning about scripting in KoL:

- The [KoLMafia wiki](https://wiki.kolmafia.us/index.php/Main_Page) has documentation for most existing functions used in Mafia scripts
- KoLMafia can read scripts written in ASH or Javascript, so anything that supports writing those is a good tool; the rest of this page will discuss these languages
- [Visual Studio Code](https://code.visualstudio.com/) is a popular software for scriptwriting that offers, among other things, syntax highlighting and source control; it's highly recommended for your development environment!
- Sometimes, the best way to learn is to read scripts made by others. You can find a wealth of these on the [KOLMafia Forums](https://kolmafia.us/#repository.3) or on the [LASS GitHub](https://github.com/Loathing-Associates-Scripting-Society/)
- Another great place to learn is to visit the [Ascension Speed Society Discord](https://discord.com/invite/k3vR3caDkF); the #mafia-and-scripting channel is full of helpful folk who'd be happy to show you the ropes

# ASH & Javascript

These are the two primary ways you'll be scripting in KoLMafia. What are they?

- **ASH** is a specific-use KoL language that was built by KoLMafia's developers, starting with [Mafia's inception in 2005](http://forums.kingdomofloathing.com/vb/showthread.php?t=88408) and being improved and maintained since
- **Javascript** is a fundamental programming language used across the internet, primarily for backend webpage functionality and is supported for code execution in all major browsers

The two languages are similar, but have some different syntax quirks. To demonstrate, here are some basic, one-line KoL tasks that you might do in ASH or JS:

| Syntax          | ASH                            | Javascript                          |
| --------------- | ------------------------------ | ----------------------------------- |
| Look up an item | `$item[squirming slime larva]` | `Item.get("squirming slime larva")` |
| Restore MP      | `restore_mp(69)`               | `restoreMp(69)`                     |
| Buy a Big Rock  | `buy(1, $item[big rock])`      | `buy(1, Item.get("big rock"))`      |

To test any of these, you can simply run them in the GCLI. For example:

![image](https://user-images.githubusercontent.com/8014761/137573686-d4e90c08-c499-4848-a2e5-becd44106ee9.png)

These are all relatively similar, but differences in syntax and structure become more pronounced as scripts get more complicated. Here are two examples of a more complex task: returning all one-handed weapons that you have, sorted by familiar weight.

In Javascript, this would look like:

```js
Item.all()
  .filter((item) => availableAmount(item) > 0 && weaponHands(item) === 1)
  .sort(
    (a, b) =>
      numericModifier(b, "Familiar Weight") -
      numericModifier(a, "Familiar Weight"),
  );
```

In ASH, the same task would look like this:

```ash
item[int] weapons_by_fam_lbs;		//our desired output
int count;			        //how many items meet our criteria? will be used as the key

//first we want to go through all items and list those who meet our requirement
foreach it in $items[]	//go through all items one by one
{
	//skip an item if it fails our criteria
	if(available_amount(it) == 0 || weapon_hands(it) != 1) continue;
	weapons_by_fam_lbs[count] = it;
	count++;
}
//next we sort and print our list
sort weapons_by_fam_lbs by numeric_modifier(value,"Familiar Weight");
foreach it in weapons_by_fam_lbs {print(weapons_by_fam_lbs[it]);}
```

---

Both ASH and JS have their own use cases and value in the KoL scripting world.

- For an introduction to ASH and an overview on its pros and cons, [check our ASH starter kit](ASH-Overview.html).
- If you would like to see some information about JS in the context of KoL, [check our JS overview page](JS-Overview.html).
