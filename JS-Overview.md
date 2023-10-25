# Javascript

## Why Javascript?

The single biggest advantage that Javascript has over ASH is the fact that it is widely used for other things beyond KoL scripting. This means that when you come across a problem or a concept that doesn't make sense, you will have the entirety of the internet's collective Javascript knowledge to provide you an answer as opposed to just things specifically posted about on the KoLmafia forums. As an added bonus, it means that skills you hone while writing KoL scripts will be applicable elsewhere.

## How Javascript?

This is a very silly question that I've put into your mouth, and so it gets a very silly answer. An answer to one interpretation of this question is Rhino, a Javascript engine written in Java (despite their names, these languages are unrelated), that Mafia uses to read Javascript, uh, scripts.

An answer to another interpretation of this question is pretty similar to ASH: just start writing. When you write in Javascript, you'll need to import any mafia functions you plan on using, by having a big chunk of text at the top of your script that essentially looks like this:

```
const {
 adv1,
 availableAmount,
 buy,
 drink,
 eat,
 getProperty
} = require("kolmafia");
```

Other than that, the world is pretty much your oyster. One thing to note is that you won't need to import fundamental Object types used by KoLMafia: Item, Skill, Effect, Familiar, etc. You will, however, have to import any functions that use these types.

One other important note: the KoLMafia Wiki was written to support ASH. This means that functions on the Mafia wiki are described using their ASH naming conventions (and with written-out ASH examples). Generally speaking, JS uses camel case (e.g. thisIsYourVariable) while ASH uses snake case (e.g. this_is_your_variable). Tactically, what this means is that when you access an ASH page to get information about a specific function (like, say, [elemental_resistance](https://wiki.kolmafia.us/index.php/Elemental_resistance)), you need to be cognizant of the fact that any JS script that references this function will require elementalResistance instead of elemental_resistance. It's a small change, but important to keep in mind when using the wiki to inform your available functions. The other biggest difference is that any fnction that returns a Map in ASH will return an Object in Javascript, so doing `getCampground().has("Witchess Set")` won't tell you anything helpful.

## Improving your JS development with Typescript

"Hold on!", you protest, "I have just learned about Javascript and it seems cool. Why would you introduce something new!" This is a fair criticism, and if you are trying to script simple actions you can probably stop here. That being said, maybe your appetite has been whet and you are ready to tackle a larger project. In these scenarios, it makes sense to consider Typescript. Typescript is a superset of Javascript, meaning that it has everything Javascript has, but it also has more! The primary advantage Typescript has over Javascript is that it has static typing, this is a programming concept which means, in practical terms, that you can catch certain errors when you are writing the code, as opposed to when KoLMafia is executing the code. This gets to be very important when you are dealing with a large script containing many functions and variables. However, this added functionality does not come for free. It comes at the cost of having to transpile, here meaning compiling your Typescript into Javascript so KoLmafia can understand it. This involves doing additional setup for the script you are writing.

## Linting and Libram

LASS provides two very helpful packages for TypeScript projects. The first is [Libram](https://github.com/Loathing-Associates-Scripting-Society/libram), an all-purpose toolkit meant to extend existing mafia functions, with the end goal of making it just about the only external module any KoL scripter will ever need. Its features include the `get()` function, which is a modified version of mafia's `getProperty()` that returns objects of the appropriate type. It also has a system of template literals that makes it slightly easier to talk about Items and Familiars and Skills and the sort. This small change adds up a lot:

```
if (get("_sourceTerminalDigitizeMonster").maxMeat > $monster`garbage tourist`.maxMeat)
```

is much shorter and more legible than

```
if (toMonster(getProperty("_sourceTerminalDigitizeMonster")).maxMeat > Monster.get("garbage tourist").maxMeat)
```

The other spicy package we provide is libram-linked: it is the [eslint Libram plugin](https://github.com/Loathing-Associates-Scripting-Society/eslint-plugin-libram), which is used across all LASS projects. ESLint is a tool that analyzes Javascript and TypeScript code for bad code and bad form, and the plugin adds a variety of features, the most important of which is its ability to verify constants. Normally, in Javascript, if I write something like

```
Item.get("Unwrapped retro knock-off superhero cape")
```

the code will get through just fine, it'll reach mafia, and mafia'll throw a tantrum over the fact that there is no such item. With the eslint Libram plugin, however, it'll catch that

```
$item`Unwrapped retro knock-off superhero cape`
```

is wrong, and you'll be able to correct it before compiling and running your code.

## Starting with TypeScript

TypeScript can be a bit intimidating. Due to the additional hassle in setting a TypeScript project up, we have made a starter library that starts you on your TypeScript journey. Please visit [the following repository](https://github.com/docrostov/kol-ts-starter) if you would like to start your very first KOL TypeScript project, and (as always) reach out on the #mafia-and-scripting channel on the Ascension Speed Society Discord if you have any questions. We'd be happy to help!
