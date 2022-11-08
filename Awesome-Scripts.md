# Awesome KoL Scripts

This document contains a list of commonly used and (largely) regularly updated scripts that are used for a wide variety of different use cases. We've sorted these scripts out into four distinct categories, which are (in some cases) split into smaller sub-categories, such as farming & ascension within automation:

- **Automation**: Scripts that allow you to automate pieces of KOL, usually for farming purposes.
- **Organization**: Scripts that organize items and resources in specific ways
- **Relay**: Scripts that create or modify pages in KoLMafia's relay browser, for added UI benefits and information
- **Miscellaneous**: Scripts that do not fit the mold of the other 3 categories; these are usually informational in nature, or automate specific tasks in specific ways

If you would like to submit a script to be placed on this page, please post in the **#mafia-and-scripting** channel in the [Ascension Speed Society discord](https://discord.gg/8p7hh8BRSF); tag Captain Scotch (whose Discord name is DocRostov#7004) to ensure it gets seen in a timely fashion.

## Automation (Ascension)

### autoscend

| owner | link | usage |
|---------|------|---------|
| [L. A. S. S.](https://github.com/Loathing-Associates-Scripting-Society) | [autoscend GitHub](https://github.com/Loathing-Associates-Scripting-Society/autoscend) | Run the script in the GCLI |

**autoscend** is one of the crowning achievements of the Loathing Associates Scripting Society. In a nutshell, autoscend is a script that will play through an entire ascension for you in KoL. The guiding philosophy of autoscend is that while it may not get you through an ascension as efficiently as humanly possible, it will brute force the ascension using as many resources as it can reasonably use, and it will finish (most) paths within 3-4 days. Given the complexity of KOL, this is pretty impressive! In a few recent paths, autoscend has actually been good enough and efficient enough at resource usage to get a few players bronze buttons, which gives you a view into how effective the autoscend team has been in working on the script. If you have questions regarding autoscend, please post issues on the GitHub or reach out in the **#autoscend** channel within the [ASS discord](https://discord.gg/8p7hh8BRSF).

## Automation (Farming)

### Garbage Collector (AKA Garbo)

| owner | link | usage |
|---------|------|---------|
| [L. A. S. S.](https://github.com/Loathing-Associates-Scripting-Society) | [GARBO GitHub](https://github.com/Loathing-Associates-Scripting-Society/garbage-collector) | Run the script in the GCLI |

**Garbage Collector** (more commonly known as "Garbo") is the Loathing Legion Knife of Barf Mountain farming scripts. It does it all! Barf Mountain is a zone from the 2015 Dinseylandfill IOTM. It features the highest ambient meat drop in an infinitely accessible zone in the game. Garbo will buy a ticket to Barf Mountain and use every drop of a player's resources to earn meat -- it features bespoke valuations engines that analyze the value of every free fight source, a knapsack-style dieting system that tabulates potential profit given current mall prices of every possible diet configuration, and both Embezzler/Yachtzee maximization chain logic to use every copier in the game. Garbo is actively developed, and generally supports new IOTMs within a week after their release; for questions or comments, there is a well-described system for bug reports and feature requests within the pins in the **#garbage-collector** channel within the [ASS discord](https://discord.gg/8p7hh8BRSF).

### freecandydotexe

| owner | link | usage |
|---------|------|---------|
| [Loathers](https://github.com/loathers) | [freecandy GitHub](https://github.com/loathers/freecandydotexe) | Run the script in the GCLI |

**freecandydotexe** is a script meant to run a large gob of turns for trick or treating. In KOL, Halloween is a massively valuable exercise, often netting users tens of millions of meat in a single day; freecandy is a script that both trick or treats and fights things like guaranteed kramcos, voting monsters, and nemesis hitmen. It handles familiar swaps (to properly utilize your Trick or Treating Tot) and fills your Pantsgiving stomach. Freecandydotexe is actively developed, and (with some exceptions) will support new IOTMs within 1-2 Halloweens of the IOTM's introduction. For questions, bug reports, or comments, please post relevant details in the **#freecandydotexe support thread** thread within the **#garbage-collector** channel on the [ASS discord](https://discord.gg/8p7hh8BRSF).

### COMBO

| owner | link | usage |
|---------|------|---------|
| [L. A. S. S.](https://github.com/Loathing-Associates-Scripting-Society) | [COMBO GitHub](https://github.com/loathing-Associates-Scripting-Society/combo) | Run the script in the GCLI |

**COMBO** is a beach-combing script that will harvest known scarce tiles for fun and profit. When the beach comb was introduced in KOL, TPTB introduced 1000 "scarce" tiles; these tiles, when refreshed, contain the rarest items the beach has to offer, such as cursed pirate gear, meteorite fragments, and rainbow pearls. The tiles refresh on an unknown cadence, and when they are not refreshed, they are indistinguishable from common tiles. However, many enterprising souls spent years combing the beach to figure out exactly where these 1000 tiles are, so that they would be more likely than anyone else to get the scarce items when the tiles refreshed -- COMBO is a project that publicizes these tiles, allowing anyone to have that increased chance at getting rares from their beach. COMBO is a nonprofit project supported by volunteers. Please do not yell at us. For questions, bug reports, and comments, please post relevant details in the **"sharing-new-scarce-tiles"** thread within the **#spading** channel on the [ASS discord](https://discord.gg/8p7hh8BRSF).

## Organization (Inventory Management)

### Philter

| owner | link | usage |
|---------|------|---------|
| [L. A. S. S.](https://github.com/Loathing-Associates-Scripting-Society) | [Philter GitHub](https://github.com/loathing-Associates-Scripting-Society/philter) | Run the script in the GCLI, after relay-organizing your items |

**Philter** is a next-generation version of a classic KOL script, the "OCD Inventory Control" system designed by Bale of the KOLMafia forums. Philter's goal is to cleanse your inventory of junk items, autoselling & using items that warrant that action and mallselling or Sellbot-sending items that warrant mall action. This involves a detailed relay interface that can be used to sort, organize, and create rulesets around what you want Philter to do with your items. For a sample ruleset, Butts McGruff has shared his rules on the [ASS discord](https://discord.gg/8p7hh8BRSF) in a pinned post within the **#mafia-and-scripting** channel. It is worth noting that making a ruleset you are comfortable with takes quite a lot of time -- expect a significant period of adjustment even if you start at Butts' well-designed sample ruleset. 

### Keeping Tabs

| owner | link | usage |
|---------|------|---------|
| ReverKiller (#892618) | [Keeping Tabs GitHub](https://github.com/pstalcup/keeping-tabs) | Run the script in the GCLI, after tab-organizing your items |

**Keeping Tabs** is a lower-user-effort version of Philter (discussed above), which uses the native KOL inventory tab system to organize your items and allow users to modify their desired tab behavior. Essentially, you as a user just need to make a number of custom-named tabs that reflect what you want to do to your items; running `keeping-tabs` will then do exactly what you told it to do, flushing your inventory out and emptying it in the way you outlined. There is no active support system for Keeping Tabs -- if you have questions, please post an [issue](https://github.com/pstalcup/keeping-tabs/issues) on the GitHub linked above and Rev will get to it on his own time. 

## Relay (General Purpose)

### TourGuide

| owner | link | usage |
|---------|------|---------|
| [Loathers](https://github.com/loathers) | [TourGuide GitHub](https://github.com/loathers/TourGuide) | After installing, select it from the topbar of the relay browser to run the assistant |

**TourGuide** is, effectively, an advice script. It provides a large-scale summary of all available resources that you -could- be using in KoL, with things like lists of available free banishes, steps to complete active quests, tips on how to finish tasks in the fewest turns, and large bright reminders when you have a limited use resource up that you may want to go to a specific place to use. TourGuide is based on the script "Guide" by [Ezandora](https://github.com/Ezandora); while it is based on the bones of Guide, TourGuide has evolved into a vastly different fork of the original brainchild, with roughly two years of extra IOTMs covered and added to the script, along with several additional features. TourGuide developers acknowledge and appreciate Ezandora's work in creating the scaffolding behind TourGuide.

### ChIT

| owner | link | usage |
|---------|------|---------|
| Soolar (#2463557) | [ChIT GitHub](https://github.com/Loathing-Associates-Scripting-Society/ChIT) | Once installed, will show up automatically |

**ChIT** is an upgraded character pane. It features a vastly customizable set of tiles that can be moved, twiddled, and re-sized to create a perfect view of what you need to know about your character. Many speed ascenders use it explicitly for the additional support it gives for quick equipment swaps, familiar management, easy buff shrugging & management, and highlighted timers that allow you to remind yourself of future actions you should do in future turns. It is under active development and generally supports IOTMs relatively soon after they are released; if you have ChIT installed and notice that new IOTMs are not supported, please check the GitHub to see if an update was pushed, and consider deleting/re-installing; due to the "always on" nature of ChIT vs other scripts, it is slightly more common for people to experience issues where ChIT does not properly update. Soolar is an active member on the [ASS discord](https://discord.gg/8p7hh8BRSF) and is actively developing ChIT; if you have questions, please post issues on the GitHub or reach out in the **#mafia-and-scripting** channel. 

### Bale's Relay Overrides

| owner | link | usage |
|---------|------|---------|
| Bale (#754005) | [KoLMafia Forum Thread](https://kolmafia.us/threads/bales-relay-overrides.12644/) | A variety of different formats; see description |

Bale is an old-time scripter who made a truly absurd number of helpful and powerful scripts. **Bale's Relay Overrides** is a difficult-to-summarize series of scripts that impact a ton of elements of the game in the relay browser. A handful of old classics include a leaderboard script that highlights gold/silver/bronze commendation holders, a wiki-links script that adds links to KOL Wiki pages in all item descriptions, [and DarthNed's Source Terminal GUI that requires a few less clicks than Ezandora's script below](https://kolmafia.us/threads/bales-relay-overrides.12644/page-14#post-137665). One important caveat -- these scripts are no longer supported, as Bale is no longer an active KOL player. That said, very few of these scripts have seen any errors or bugs in the last 7 years, so it is generally unlikely you'll see major bugs or issues from any of them. If you do, we would recommend posting about them in the forum thread linked above for other helpful KoLMafia scripters to try and assist you, or reach out in the **#mafia-and-scripting** channel in the [ASS discord](https://discord.gg/8p7hh8BRSF). If you choose to update any of these scripts, let us know and we'll link a new version on this page! 

## Relay (Supplemental UI for IOTMs)

### Briefcase

| owner | link | usage |
|---------|------|---------|
| Ezandora (#1557284) | [Briefcase GitHub](https://github.com/Ezandora/Briefcase) | Shows up in the relay browser when you examine your KGB |

**Briefcase** is a relay override that *dramatically* simplifies usage of the [Kremlin's Greatest Briefcase](https://kol.coldfront.net/thekolwiki/index.php/Kremlin%27s_Greatest_Briefcase) IOTM. The KGB is perhaps the most confusing and difficult-to-use IOTM ever released, requiring a user to play a devilishly complicated game of visual Mastermind to unlock the tabs, cycle the effects, and generate useful buffs. It took almost the entire month of the KGB's release for people to figure out how the hell the IOTM was supposed to be used. Ezandora's KGB override is completely necessary to actually use the IOTM in an ascension context; without it, you're effectively flying blind and spending 30-45 minutes solving a puzzle to try and figure out how the hell the IOTM can be used. This script is not actively updated or maintained, but has not required significant changes in years, so likely will still work very well for your purposes -- and, as noted, is *100% required* if you have any intention of using the KGB within an ascension context.

### Pizza Cube GUI

| owner | link | usage |
|---------|------|---------|
| Lacey Jones (#2993889) | [Pizza Cube GUI GitHub](https://github.com/ggvgiu/PizzaCubeGUI/) | Shows up in the relay browser when you click on your workshed with the Pizza Cube installed |

**Pizza Cube GUI** is a relay override that improves the experience of baking diabolic pizzas in KoLMafia. The [Diabolic Pizza Cube](https://kol.coldfront.net/thekolwiki/index.php/Diabolic_pizza_cube) IOTM allows users to sacrifice four items into your pizza oven to generate a diabolic pizza. The items chosen give the pizza various effects and beneficial attributes to the user. This GUI features predictions of the effects pizza would generate with a given selection of items, suggestions for possible pizzas that could be helpful to you, various ways to filter and sort large inventories when trying to make your perfect pizza, and filters out effects that do not work in the pizza cube. Highly recommended if you plan on baking pizzas in your KOL career. Lacey is a semi-active user in the [ASS discord](https://discord.gg/8p7hh8BRSF); if you have questions, please post issues on the GitHub or reach out in the **#mafia-and-scripting** channel for our scripters to take a look. 

### Genie

| owner | link | usage |
|---------|------|---------|
| Ezandora (#1557284) | [Genie GitHub](https://github.com/Ezandora/Genie) | Shows up in the relay browser when you make a wish |

**Genie** is a relay override that makes wishing using the [genie bottle](https://kol.coldfront.net/thekolwiki/index.php/Genie_bottle) in KoL considerably easier to do. The native UI for wishes (both pocket wishes and rubbing the Genie bottle) is frustratingly simplistic, requiring checking the wiki to figure out how to do even very basic activities; Ezandora's relay override fixes this issue by spawning a page that gives you a well-formatted list of possible options you can use for your wish. This script is not actively updated or maintained, but has not required significant changes in years, so likely will still work very well for your purposes.

### Shorts UI

| owner | link | usage |
|---------|------|---------|
| worthawholebean (#1972588) | [Shorts UI GitHub](https://github.com/phulin/shorts-ui/) | Shows up in the relay browser when you \[use\] your cargo cultist shorts |

**Shorts UI** is a relay override that improves the experience of picking the pocket of your cargo shorts in KoLMafia. The [Cargo Cultist Shorts](https://kol.coldfront.net/thekolwiki/index.php/Cargo_Cultist_Shorts) IOTM allows users to pick the shorts pocket once a day; this gets you useful buffs, useful items, or free fights against useful monsters. As there are 666 pockets in the shorts, it can be very hard to remember what's what; this UI summarizes the most useful picks and lets you select them very quickly in an ascension, without having to reference the wiki or a spading sheet to figure out which pocket you'd need to pick for which effect. The script's creator, worthawholebean, is a moderator on the [ASS discord](https://discord.gg/8p7hh8BRSF); if you have questions, please post issues on the GitHub or reach out in the **#mafia-and-scripting** channel for us to take a look.

### Locket UI

| owner | link | usage |
|---------|------|---------|
| [L. A. S. S.](https://github.com/Loathing-Associates-Scripting-Society) | [LocketUI GitHub](https://github.com/Loathing-Associates-Scripting-Society/locket-ui/) | Click "reminisice" to activate the Locket UI page |

**Locket UI** is a relay override that improves the experience of reminisicing using the [Combat Lover's Locket](https://kol.coldfront.net/thekolwiki/index.php/Combat_lover%27s_locket) IOTM. The native UI is just a drop down with every possible monster; this UI maintains that dropdown, but allows users to filter it to specific desired phylums, while also pulling out a variety of ascension-relevant picks into easy buttons that can be quickly activated during an ascension. This script is actively updated and maintained by LASS; for support, visit the [ASS discord](https://discord.gg/8p7hh8BRSF) and reach out in the **#mafia-and-scripting** channel for us to take a look.

### Bastille

| owner | link | usage |
|---------|------|---------|
| Ezandora (#1557284) | [Bastille GitHub](https://github.com/Ezandora/Bastille) | Shows up in the relay browser when you use the Bastille item |

**Bastille** is a relay override that makes selecting your rewards for the [Bastille Battalion control rig](https://kol.coldfront.net/thekolwiki/index.php/Bastille_Battalion_control_rig) minigame much easier, and runs the minigame for you in order to save time during your ascensions. This script is not actively updated or maintained, but has not required significant changes in years, so likely will still work very well for your purposes.

### Asdon Martin GUI

| owner | link | usage |
|---------|------|---------|
| Ezandora (#1557284) | [Asdon GUI GitHub](https://github.com/Ezandora/Asdon-Martin-GUI) | Shows up in the relay browser when you click on your workshed with the Asdon Martin installed |

**Asdon Martin GUI** is a relay override that simplifies usage of the [Asdon Martin](https://kol.coldfront.net/thekolwiki/index.php/Asdon_Martin) IOTM. The process of fueling and upkeep for an Asdon Martin is a little bit annoying; this GUI abstracts the annoying issue of fueling and toggling buffs by placing them all on the same page, and offering automated buttons that will do things like create soda bread to fuel your Asdon or fuel up to specific points. Unlike many of Ezandora's scripts, does require a more recent version of Mafia than the rest, as it has a few specific changes in how worksheds are used that require more recent mafia installs than most of her work. This script is not actively updated or maintained, but has not required significant changes in years, so likely will still work very well for your purposes.

### Source Terminal GUI

| owner | link | usage |
|---------|------|---------|
| Ezandora (#1557284) | [Source Terminal GUI GitHub](https://github.com/Ezandora/Source-Terminal-GUI) | Shows up in the relay browser when you click on your source terminal |

**Source Terminal GUI** is a relay override that simplifies usage of the [Source Terminal](https://kol.coldfront.net/thekolwiki/index.php/Source_Terminal) IOTM. Natively, the terminal effectively acts as a unix-style terminal, ingesting commands like "dir, exit, help, ls, reset, status" and running enhance/enquiry/educate/extrude commands at the user's urging. It's a very cute piece of native UI, but can be a little annoying if you have to use it every single ascension; Ezandora's GUI takes the text-based terminal and turns it into a button-based GUI where you simply need to press easily labeled buttons to get the terminal to do what you want. This script is not actively updated or maintained, but has not required significant changes in years, so likely will still work very well for your purposes.

## Miscellaneous

### Snapshot Maker (av_snapshot)

| owner | link | usage |
|---------|------|---------|
| Aventuristo (#3028125) | [av_snapshot on the KoL Forums](http://forums.kingdomofloathing.com/vb/showthread.php?t=250707) | Run the script in the GCLI |

**Snapshot Maker** (more commonly known as **av_snapshot**) is a script that populates a public, shareable webpage you can use to show people what you own in KoL. This page will display every IOTM that is bound to your account, what skills you have permed, what your character has consumed, what tattoos your character has unlocked, and whether or not you own a variety of cool semi-relevant items from years prior. When other KOL players ask to see your snapshot (or talk about "greenboxen"), this is what they're talking about. This is a more-updated fork of cc_snapshot, a long-used script by Cheesecookie. Thanks Cheesecookie!

### Greenbox
| owner | link | usage |
|---------|------|---------|
| [Loathers](https://github.com/loathers) | [Greenbox on GitHub](https://github.com/loathers/greenbox) | Run the script in the GCLI |

**Greenbox** is a new format for the aforementioned av_snapshot. It is coded in Typescript, with a slick React-based GUI. It is under active development, and while it does not yet have as many Greenboxen for the aspiring Greenboxer to find compared to av_snapshot, it is trying its best. It also has a cool logo! Wow! Amazing!

### KoL AccountVal.js

| owner | link | usage |
|---------|------|---------|
| Irrat (#3469406) | [Kol AccountVal GitHub](https://github.com/libraryaddict/KolAccountVal/) | Run the script in the GCLI |

**AccountVal.js** is a spiritual successor to an ASH script by the wise and curious Soolar, written in JavaScript by the also-wise and ever-curious Irrat. It will analyze your inventory and report back on the value of everything you've got. Unlike it's predecessor, this script will run faster on subsequent runs after the first run, as it has caching support for items it has already evaluated. It also has an option that only generates the value of your tradeable items; ergo, you can both revel in the riches you've bound to your account and get excited about the un-accumulated riches your tradeable items could give you.

### Gain

| owner | link | usage |
|---------|------|---------|
| Ezandora (#1557284) | [Gain GitHub](https://github.com/Ezandora/Gain) | Run the script in the GCLI |

In a nutshell, **Gain** is an efficient buffing script. It will analyze pricing on various buff options and get the user to the cheapest possible configuration that achieves their goals. As the help file states, `gain 400 initiative` is a command that will figure out the most cost-efficient way to get your character to 400 initiative and get you there. This is most useful in the context of other scripts, but can be useful in limited scenarios within an ascension, for instance if you are trying to quickly complete an ascension and need to hit a specific threshold for a specific test. As with other scripts by Ezandora, Gain is not actively updated or maintained, but has not required significant changes in years, so likely will still work very well for your purposes. It relies on Mafia's background data when running its calculations, so it is likely it will still evaluate things that were released after the script's most recent update (in February 2021, as of this writing). 

### KoLGrimace

| owner | link | usage |
|---------|------|---------|
| Irrat (#3469406) | [KolGrimace GitHub](https://github.com/libraryaddict/KolGrimace/) | Run the script in the GCLI |

**KoLGrimace.js** is a script that does one thing, and does it well. It provides you a one-line answer to the rate of human monsters vs aliens in the Domed City of Grimacia, a zone in which adventurers can farm Maps to Safety Shelter Grimace Prime. This tells you days where it is optimal to farm up maps to Safety Shelter Grimace, if you want to farm those maps so you can build a stockpile of Distention Pills and Dog Hair Pills. Simple but useful!

### ScotchLog

| owner | link | usage | 
|---------|------|---------|
| Captain Scotch () | [ScotchLog GitHub](https://github.com/docrostov/ScotchLog) | Run the script in the GCLI |

**ScotchLog** is a log parser. It does what it says. It was coded by a fiddly speedrunner who also happened to write this document; as a result, it tracks a few more things than [other log parsers](https://kolmafia.us/threads/runlogsummary.22963/) do, like freerun usage and (for unrestricted runs) loadouts of key choices the user made during their run. Examining one's run logs for turn leaks, routing improvements, RNG screw, and general strategic play is usually a good way to improve your play and become better at the game. You probably don't need all the data logged by ScotchLog, but you might need some of it, so it might be for you. I dunno, dogg. I don't know your life.

# Awesome KoL Scripts... that require Compiling

Everything above this line is usable out-of-the-box. You can install the script and use it either from the GCLI or the relay browser without going through additional pre-installation steps. Below this line, everything listed requires a bit more effort; these projects are built in TypeScript, which requires compiling into a usable script that KoLMafia can read and use. You won't simply be able to run an "SVN install" command and just run the script. 

For more on how to do compile and build these scripts, please cross-reference our [KOL TS Starter repository](https://github.com/docrostov/kol-ts-starter) with the readmes for the individual scripts. Our starter repository will walk you through the often lugubrious process of compiling and staging scripts such that your system can run them, while the readmes should give more guidance on things that may need changing for your specific situation.

### LoopCasual

| owner | link | usage |
|---------|------|---------|
| Kasekopf (#1210810) | [LoopCasual GitHub](https://github.com/Kasekopf/loop-casual) | Compile the script's JS file, import into your scripts folder, then run the script in the GCLI |

**LoopCasual** aims to complete a casual ascension in one day. It tries to use as few turns as possible to accomplish this, allowing someone to use one of the farming scripts below to use the rest of a character's turns. At a high level, this will power your character up to level 13 and complete quests using a relatively customized quest engine. It was originally built by Kasekopf to work very specifically for Kasekopf's account; it is more flexible than it used to be, but we would recommend having patience and being ready to work with account-specific bugs as you work your account into a place where LoopCasual works for your account. Kasekopf is an active member on the [ASS discord](https://discord.gg/8p7hh8BRSF) and is actively developing LoopCasual; if you have questions regarding LoopCasual, please post issues on the GitHub or reach out in the **#mafia-and-scripting** channel. 
