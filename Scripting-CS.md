# Scripting Community Service

## Introduction

[Community Service](https://kol.coldfront.net/thekolwiki/index.php/Community_Service) (CS) has become a commonly scripted challenge path due to its simplicity and speed (both in-game and real-time). Rather than need to perform all of the standard council quests, the player gets 11 tasks that take a single button click each. Said tasks can be accelerated by buffing up things like stats, familiar weight or item drops. It doesn't take a lot of shiny to do a two-day run, and sufficiently loaded accounts can perform replicable one-day ascensions with low turn counts and organ use. This is desirable as it allows for a second shot at valuable once per day item generation, as well as extra aftercore turns for farming or event participation.

Unfortunately, it's not easy to create a one-size-fits-all high-end CS solution due to a lot of moving parts. The path rewards access to a lot of old shinies, but it's possible to get creative and plug holes in your setup in various unconventional ways. Once you have an operational CS run plan, it's not that hard to precisely execute it. Scripting can assist with consistency, doing anything from buffing you up so you don't forget some effect all the way to performing a whole run for you.

## Creating a Run Plan

A typical CS ascension consists of the following stages:

- Using [borrowed time](https://kol.coldfront.net/thekolwiki/index.php/Borrowed_time) and doing coil wire, a 60-turn task that can't be accelerated.
- Using the resulting reward to kick-start your stats, and levelling up as quickly as possible via (free) scaling fights to help with the stat tests.
- Performing the stat tests, and then all others:
  - It's common to group hot resistance, noncombat and familiar weight together as they all benefit from having a heavy familiar - [exotic parrot](https://kol.coldfront.net/thekolwiki/index.php/Exotic_Parrot) helps with hot resistance, while [disgeist](<https://kol.coldfront.net/thekolwiki/index.php/Disgeist_(familiar)>) helps with noncombat. Plus if you do this early then you can use some of the familiar weight buffs during levelling.
  - A number of buffs are shared between weapon damage and spell damage.
  - Doing the item test last allows the item buffs used to carry over into aftercore, and if you have the [emotion chip](https://kol.coldfront.net/thekolwiki/index.php/Emotionally_Chipped) then you can use [Feeling Lost](https://kol.coldfront.net/thekolwiki/index.php/Feeling_Lost) for an additional +60% on the test; one of your first post-run actions should be to remove the effect due to its built-in Teleportitis.

Levelling is one of the more individualised portions of the run. The general idea is to use free fights with scaling monsters, derived from various IotMs like the [Neverending Party](https://kol.coldfront.net/thekolwiki/index.php/The_Neverending_Party). The more free fights you have the better, and access to the [makeshift garbage shirt](https://kol.coldfront.net/thekolwiki/index.php/Makeshift_garbage_shirt) doubles their yields. The higher you can pump your main stat and your experience gains from fights the better, which makes [Sweet Synthesis](https://kol.coldfront.net/thekolwiki/index.php/Sweet_Synthesis) with its +300% stat and +50% experience gain buffs a very desirable skill to have access to. However, as mentioned, it is possible to use replacement shinies to achieve these goals. For example, one can use a [diabolic pizza](https://kol.coldfront.net/thekolwiki/index.php/Diabolic_pizza) to get a [+500% buff](https://kol.coldfront.net/thekolwiki/index.php/Mallowed_Out) to all stats, which helps both with levelling and the subsequent tests. Another option is to use copies from the [backup camera](https://kol.coldfront.net/thekolwiki/index.php/Backup_camera) or [Pocket Professor](https://kol.coldfront.net/thekolwiki/index.php/Pocket_Professor) to get extra free scaling monster fights.

The non-stat tests are pretty much just a checklist. Captain Scotch created a [very helpful sheet](https://docs.google.com/spreadsheets/d/1CooctXongsf2nt1JmR8G-Qm_Dhs4V6oHDO04hLRCI_s/edit#gid=1299653939) listing the various buffs that can be used to accelerate the tests. Make a copy of the sheet and filter the lists to what you have access to, possibly adding some buffs or items that got skipped. [Bow-Legged Swagger](<https://kol.coldfront.net/thekolwiki/index.php/Bow-Legged_Swagger_(effect)>) and [Steely-Eyed Squint](<https://kol.coldfront.net/thekolwiki/index.php/Steely-Eyed_Squint_(effect)>) save a lot of turns. The [Fourth of May Cosplay Saber](https://kol.coldfront.net/thekolwiki/index.php/Fourth_of_May_Cosplay_Saber) with its wonky combat-ending mechanic allows you to carry out buffs like [Meteor Showered](https://kol.coldfront.net/thekolwiki/index.php/Meteor_Showered) that were not meant to leave combat. But other than that there aren't any crazy turn saves, it's more about how much quantity you can put together. Remember that not every test needs to be capped, and familiar weight and spell damage in particular are likely to take a long time. The sheet is going to be a good estimate of how long your run is likely to take, as stat tests are likely to be quick and there's nothing you can do about coil wire. If it seems that six [astral pilsners](https://kol.coldfront.net/thekolwiki/index.php/Astral_pilsner) plus whatever "free" turn generation you may have won't be enough to get you to finish the run in time, then you'll need to consider how to make extra required turns as part of your plan.

Another aspect of planning a run are softcore pulls. These can be used to cut turns from tests, or compensate for lacking certain IotM. For example, it's common to pull [borrowed time](https://kol.coldfront.net/thekolwiki/index.php/Borrowed_time) to help with generating turns for coil wire if not in possession of [Clip Art](https://kol.coldfront.net/thekolwiki/index.php/Summon_Clip_Art).

If in need of assistance, ask in `#community-service` in the [ASS discord](https://discord.gg/JqwXkyWF4m). Be prepared with your [snapshot](http://forums.kingdomofloathing.com/vb/showthread.php?t=218735), as it allows for better theorycrafting of a levelling plan or whatever else you may need help with. There are a lot of helpful pinned messages, such as a full-shiny ordering of scaling fights based on their caps or lists of easily accessible pizza ingredients. The folks there are very helpful - I went from an inattentive AFK farmer to creating my own CS script in the space of a couple months with their assistance.

## Doing a Run

Putting together a plan can feel nebulous, and it's a good idea to try it out in practice once it takes a bit of shape. Do whatever pre-run preparations your plan assumes, hop the gash, and try to carry things out. While you're doing so, take excruciatingly detailed notes for every single fight you do. Write down buffs you cast, take screenshots of outfits you've put on. Once you clear the stat test hurdle then you can relax a bit with the note-taking as the Scotch sheet has you covered for the tests. If anything, you may find yourself missing some of the buffs you had planned! In that event, use Mafia's `modtrace` to compare against the sheet. Something as basic as counting how many modifiers you have in each can help you determine how many you're missing, and then you can go fishing for what you forgot.

The end result will be a nice confidence boost as you perform your plan in action, get a run out of it, and obtain a very solid set of detailed notes to work with going forward. Now if you were to do the run again, the experience and notes will let you do so quicker. The first go through is the hardest, it gets easier once you're done with it.

Another thing that's likely to happen is you'll look over your notes, ponder your plan, and notice certain things you could improve. My original plan assumed using [Map the Monsters](https://kol.coldfront.net/thekolwiki/index.php/Map_the_Monsters) in a zone where the skill does not work, so I had to reconsider my plans to work around that. I ended up altering the amount of familiar weight that was needed at that point in the run, which led me to change my [hatter buff](https://kol.coldfront.net/thekolwiki/index.php/The_Mad_Tea_Party) and the order in which I was using my familiars. This iterating process is likely to continue going forward. For example, I recently realised that I can sometimes skip summoning a Chubby and Plump bar for my Synthesis plan, if I happen upon an early lavender candy heart.

## Initial Automation

Now that you're armed with an exhaustive set of notes that let you perform your desired CS run, you can continue performing those runs with reduced effort by following your steps. However, this does leave room for human error (seeing how transferring a Scotch sheet to in-game buffs can already be challenging), and sounds rather mundane in the long run. Thankfully, scripting is perfect for this sort of thing, and the notes are the ideal foundation to use for it.

Let's consider an example scenario. You are a Pastamancer, you just did coil wire, and you're buffing up your Mysticality to go beat up various free fights. Your notes feature the following list of effects that you acquired to help you with this task:

- [Uncucumbered](https://kol.coldfront.net/thekolwiki/index.php/Uncucumbered)
- [Favored by Lyle](https://kol.coldfront.net/thekolwiki/index.php/Favored_by_Lyle)
- [Starry-Eyed](https://kol.coldfront.net/thekolwiki/index.php/Starry-Eyed)
- [Feeling Excited](https://kol.coldfront.net/thekolwiki/index.php/Feeling_Excited)
- [Song of Bravado](<https://kol.coldfront.net/thekolwiki/index.php/Song_of_Bravado_(effect)>)
- [Glittering Eyelashes](https://kol.coldfront.net/thekolwiki/index.php/Glittering_Eyelashes)
- [Big](<https://kol.coldfront.net/thekolwiki/index.php/Big_(effect)>)
- [Confidence of the Votive](https://kol.coldfront.net/thekolwiki/index.php/Confidence_of_the_Votive)
- [Broad-Spectrum Vaccine](https://kol.coldfront.net/thekolwiki/index.php/Broad-Spectrum_Vaccine)
- [Total Protonic Reversal](https://kol.coldfront.net/thekolwiki/index.php/Total_Protonic_Reversal)
- [Mystically Oiled](https://kol.coldfront.net/thekolwiki/index.php/Mystically_Oiled)
- [Stevedave's Shanty of Superiority](<https://kol.coldfront.net/thekolwiki/index.php/Stevedave%27s_Shanty_of_Superiority_(effect)>)

Now that you are armed in this list of buffs, you can go and retrieve them one by one, visiting the appropriate locations, casting the appropriate skills. But all of them can be acquired via Mafia's CLI, which you're likely familiar with. For example, you can get Feeling Excited by writing `cast 1 Feel Excitement` into the CLI, similar to what you could do in chat. Seeking out the equivalent to all of the effects above yields the following list of calls:

```
daycare mysticality;
monorail buff;
telescope look high;
cast 1 Feel Excitement;
cast 1 Song of Bravado;
use 1 glittery mascara;
cast 1 Get Big;
use 1 votive of confidence;
spacegate vaccine 2;
crossstreams;
use 1 ointment of the occult;
cast 1 Stevedave's Shanty of Superiority;
```

You can take the text above and paste it into the CLI and it will acquire the effects for you. This reduces the chance you'll miss anything. You could do a CS run in this fashion - have a list of CLI calls to paste in, then do combats manually, and hit up the tests once prepared. Rather than needing to follow the notes to a dot, you now copy-paste things into the CLI. Things are already getting somewhat automatic, and they can get even more automatic if you want! Next stop - combat.

## Combat Macros

There's a very good chance you've crossed paths with KoL's combat macros before. They're an incredible quality of life feature that helps at any level of play, and they're also very useful here. Just in case you're unfamiliar with them, the [documentation](http://forums.kingdomofloathing.com/vb/showthread.php?t=181641) provided on the forums is extremely helpful and easy to follow. Let's go back to the Pastamancer hitting up free fights to level up scenario, and let's assume you're abusing the Saber for combat (scaling fights scale their combat stats to Muscle/Moxie, but Saber hits like a train based on Mysticality, and the fight's stat gain is also Mysticality based). You go into combat, do some staggers and value stuff, and then apply the Saber for an easy win. Putting it all together looks like so:

```
skill Micrometeorite
skill Sing Along
attack
repeat
```

You can then save this as `CS_kill` or whatever other name you fancy, and then you have the power to `/aa CS_kill` from chat or the CLI to have this set up as an auto-attack for you. You have the power to make this macro quite a bit more complex than the demo case, and the combination of native KoL macros on auto-attack with Mafia scripting has been used by power users for years.

Problems arise when you want to code up more complex scenarios. For example, you decide to pursue [Tomes of Opportunity](https://kol.coldfront.net/thekolwiki/index.php/Tomes_of_Opportunity) and burn various free banishes/runaways in the Neverending Party. However, just as you're running out of said runaways, you want to [Bowl Sideways](https://kol.coldfront.net/thekolwiki/index.php/Bowl_Sideways) to get extra stats from the monsters you do end up fighting. While you can know from within Mafia when the relevant fight comes up, the KoL macro does not have access to that information. This leaves two main options, and the way to go depends on whether you prefer compactness or clarity:

- Create multiple macros for multiple situations, and set them to auto-attack when they're needed. This can result in partially redundant macros performing similar tasks, and potentially increases the number of macros you need to modify in the event of wanting to implement a change.
- The macros can check for certain things, namely the presence/absence of effects, skills and combat items. That means you can use the presence/absence of easily acquired items/effects to drive the macro's behaviour. [Timers](https://kol.coldfront.net/thekolwiki/index.php/Timers) are freely castable/shruggable, while [hair spray](https://kol.coldfront.net/thekolwiki/index.php/Hair_spray) and [seal tooth](https://kol.coldfront.net/thekolwiki/index.php/Seal_tooth) are easy to get in run and can be ushered between your inventory and closet as required. This can result in code that's harder to interpret once enough time has passed for you to forget the exact details, so be sure to mention what you're doing in comments both in the macro and your script.

## Putting It Together in Javascript

Buffing and combat are the two main building blocks of CS, and now that there are approaches to handling both, you can start thinking about automating a longer stretch of a run. When writing KoL code, it's recommended to do so in Javascript as it's an actual language. You can google some of the problems you encounter with syntax and find solutions. However, Javascript is a relatively recent development in Mafia, and its [wiki](https://wiki.kolmafia.us/index.php/Main_Page) is aimed at ASH, a bespoke scripting language. It's not hard to convert the function names to their JS equivalents going from snake case to camel case - for example, ASH's `cli_execute()` becomes `cliExecute()` in JS. Revisiting the buffing bit from earlier:

```javascript
const { cliExecute } = require("kolmafia");

cliExecute("daycare mysticality");
cliExecute("monorail buff");
cliExecute("telescope look high");
cliExecute("cast 1 Feel Excitement");
cliExecute("cast 1 Song of Bravado");
cliExecute("use 1 glittery mascara");
cliExecute("cast 1 Get Big");
cliExecute("use 1 votive of confidence");
cliExecute("spacegate vaccine 2");
cliExecute("crossstreams");
cliExecute("use 1 ointment of the occult");
cliExecute("cast 1 Stevedave's Shanty of Superiority");
```

This imports the required function, and then performs the same series of CLI executions that were set up previously. However, you can put this in a `.js` file and call it from the client. You can begin experimenting with using other Mafia functions. For example, you can set your auto-attack to a macro from earlier and go do a fight via `adv1()` (recommended for automation as it goes and does a single encounter in the specified zone) in the Neverending Party:

```javascript
const { adv1, Location, setAutoAttack } = require("kolmafia");

setAutoAttack("CS_kill");
adv1(Location.get("The Neverending Party"));
```

You can test putative syntax in Mafia by pasting in your line prefaced with `js`. So for example you could technically call `js cliExecute("crossstreams");`, even if that's just telling Javascript to call a CLI command... with the JS line called from the CLI. But it's good for seeing if your syntax is operational, and checking just about every written line is honestly not a bad idea.

At this point, it should become possible to string together longer sequences of preparation, involving buffing, fights and gear. Another commonly used function will be `visitUrl()`, as some things like [voting](https://kol.coldfront.net/thekolwiki/index.php/Voting_Booth) require hitting a series of URLs and are not natively supported in automation by Mafia. The Saber is wonky, set the `choiceAdventure1387` property to whatever outcome you want (likely 3 for items) and add `if (handlingChoice()) runChoice(-1);` after the combat to sort out the choice adventure. In theory, you could go from start to end of a run now! However, if you feel like it, there's an option which will make your scripting life more convenient.

## Libram

[Libram](https://github.com/Loathing-Associates-Scripting-Society/libram) is an ASS project that adds a number of utility functions, making certain things a lot easier and more controlled:

- Combat handling is phenomenal. Prior to a fight, you can use all sorts of in-Mafia information to build a native KoL macro, which you can set as an auto-attack or pass in other ways. No more awkward interfacing between script and combat!
- Dedicated CS test handling. Run a provided function as preparation, and then go check if you're buffed up enough to clear the test in your provided turn count. Great for catching weird things going wrong and making it possible to fix them on the fly in run. It even prints out a neat little log with predictions vs. reality and run time at the end!
- Loads of convenient helper functionality. For example, `have()` is a ridiculously useful function that is a one-stop shop for checking if you have something, be it an effect, item, whatever. And then there are things like picking a [Witchess](https://kol.coldfront.net/thekolwiki/index.php/Play_against_the_Witchess_Pieces) monster to fight (surprisingly fussy to do otherwise), economically fuelling up your [Asdon Martin](https://kol.coldfront.net/thekolwiki/index.php/Asdon_Martin), or listing today's holiday wanderers. Plenty of useful stuff!

Libram's main downside is that it's in Typescript, which requires some dedicated installation and subsequent code compilation. However, ASS offers a [demo repository](https://github.com/docrostov/kol-ts-starter) that aims to get you acquainted with the process. Once you install Yarn and set up the folder, it becomes a case of calling `yarn run build` whenever you want to get a new version of the script in a form Mafia can run. TS is also closely related to JS, so your expertise from the previous step will carry over and make things easier.

Setting up an environment from scratch for this to work in is honestly a little daunting. There's nothing wrong with making a fork (your own independent copy) of the demo repository, cloning that, and following up the `yarn install` with a `yarn upgrade libram@latest kolmafia@latest eslint-plugin-libram@latest`. This installs the newest versions of Libram and Mafia, and nets you a functional TS setup to mess around in. That's what I did for my script.

A lot of Libram users us Visual Studio Code when working in TS, and this ends up informing the nature of the package's documentation. For an optimal experience, clone Libram, open it up in the editor, and you gain the power to perform a repository-wide search that should also direct you to the associated docstring. If you're not a VS Code user, you can find the IotM-related functionality in `src/resources` and try other means of searching for a particular word. It's also a possibility to take a look at how other scripts are using Libram for inspiration or syntax.

## Exploring Established Scripts

You should now be familiar enough with the subject matter to be able to look at the various existing CS scripts and get a general idea of what they're doing. It's also possible to largely forego this entire write-up, just take one of those scripts and run with it, but there's a chance it's going to explode somewhere along the way due to its bespoke nature. And then you're stranded mid run, not sure what to do to pick things up and get them going again. The less you know about everything mentioned up to now, the more uncomfortable you'll be when this happens.

However, there's no point forcing down open doors, and it's often very useful to look at existing scripts to find inspiration for solutions to common problems. The three originator scripts are [bean-hccs](https://github.com/phulin/bean-hccs), [phccs](https://github.com/horrible-little-slime/phccs) and [seventy-hccs](https://github.com/s-k-z/seventy-hccs), with a [number of descendants](https://loathing-associates-scripting-society.github.io/KoL-Scripting-Resources/CS-Scripting-Resources.html) making active use of the code base of the originators. For example, when I was making my script, I used Bean's test ordering, Phred's outfit logic and Katarn's fight sequencing, along with bits of utility syntax from everyone mentioned. The existing scripts taught me about routing and cool programming solutions to problems I didn't even know I had.

In general, it's probably best to start from the top of a script and slowly work your way down. Look for an `index.ts` or `main.ts` in the script files, that's likely the starting point. Take a look what files it imports functions from, the big ticket ones like levelling or test prep or whatever interests you. Go look at those. If you encounter something there that seems worth exploring, go look at the source code for the utility function that interests you. This is likely to be spread out across a number of files in the interest of legibility. Alternately, if you're just looking for something particular, you can do a repository-wide search instead to find the relevant bit of code.

## Crafting Utility Functions

In the event of wanting to build your own CS TS thing, it makes sense to start from some common utility functions that will keep being used in your code. For example, while it's fine to add the choice handling thing after every single Saber force you do, it's tidier to have one chunk of code that you then just run with a given set of values to perform the force in a particular way in a particular location. The following are worth figuring out:

- Regular combat, accepting a location and a macro to perform
- Special case combat:
  - Mapping a given monster
  - Saber force
  - [God Lobster](<https://kol.coldfront.net/thekolwiki/index.php/God_Lobster_(monster)>)
- Familiar selection function, going down a checklist of goals to acquire from familiars
- Buffing function, accepting the desired effects
- Common combat scenarios in macro form - regular kills, free kills, free runaways
- Some sort of outfit logic, be it maximiser use, Phred-like or whatever else
- Some sort of plan for Synthesis

As usual with the Saber, its wonkiness means that any sort of preference-trackable stuff that gets changed in an auto-attack combat won't actually get picked up by Mafia. The combat page never gets to load, so Mafia can't see the things happening. You'll need to manually adjust any affected preferences after the fight. For the familiar function, it's worth accepting an argument specifying whether the familiar is allowed to attack to avoid surprises with free kill uses. It's not fun to have your attack familiar accidentally kill the [amateur ninja](https://kol.coldfront.net/thekolwiki/index.php/Amateur_ninja) for you. From experience, if going for a simultaneous Synthesis decision, I'd recommend storing the candies to use in `_`-starting preferences named after your script. The fact they're `_`-starting means Mafia will delete them after rollover, and storing them as preferences is good for retaining the plan in the event of a script crash.

The good news is none of this is CS-specific, and can be tested in aftercore at your leisure. You don't necessarily need to perform the exact combat you'll be doing later, but it's usually enough to see your map syntax take you to the desired monster and then do a controlled free runaway or something. As mentioned, there are plenty of solutions to these issues out there already, and you can take one and run with it. However, I'd recommend becoming somewhat acquainted with what it's doing and why, making it easier to fix any issues that may be encountered at a later time. In my case that meant writing simpler takes on existing concepts like Phred's outfit handling, so that if something were to go wrong I'd understand exactly where and why.

Once those building blocks are in place, a lot of the meat of the script will be quite easy to accomplish. Some things like various run start collecting will require their own set of calls, but there's even less point to trying to be inventive here and mirroring existing script solutions should work fine. Once there's syntax in place that gets you prepped for all the tests accordingly, then you can start messing around with making your script re-entrant.

## Making Your Code Re-Entrant

Sometimes things fry. Recently I was about to do the non-combat test but the script aborted out, as for some reason my cop dollars didn't get counted correctly and I couldn't get a [shoe gum](https://kol.coldfront.net/thekolwiki/index.php/Shoe_gum). But once I sorted that out, I was able to re-run my script and it picked up right where the crash happened and finished the run for me. Being re-entrant is also good in the event of trying to change things around. When adding softcore support, I remembered most things... apart from stopping getting one errant [Ghost of Crimbo Carols](https://kol.coldfront.net/thekolwiki/index.php/Ghost_of_Crimbo_Carols) buff that triggered a knock-on cascade of failures. But my script was able to pick up and crawl on when asked to do so.

Making code re-entrant involves asking yourself what any given chunk is trying to accomplish, and then checking if it's done. This can be the presence of an item, an effect, the number of turns spent in a zone. Essentially slapping a whole bunch of `if`s and `while`s into the script. Let's revisit the buffing from earlier in the write-up, now armed with Libram and the desire to make re-entrant code:

```typescript
import { cliExecute, Effect } from "kolmafia";
import { have } from "libram";

// Get a provided list of buffs
export function getBuffs(buffs: Effect[]): void {
  for (const buff of buffs) {
    // If the buff is not there, get it
    // the .default thing is a CLI-compatible way to do so
    if (!have(buff)) {
      cliExecute(buff.default);
    }
  }
}
```

Most effects in Mafia have a `.default` property that contains the CLI way to summon said effect, so we can use that for buffing up. However, we're only doing so if we don't already have the effect present. This way, if something goes haywire a bit further down the script and we need to re-run things, the script can go get the buffs, realise it already has them, and not waste resources needlessly reapplying them.

An example use of this buffing function, for the earlier list of effects:

```typescript
// +myst stuff! Quite a lot of it!
getBuffs([
  $effect`Uncucumbered`,
  $effect`Favored by Lyle`,
  $effect`Starry-Eyed`,
  $effect`Feeling Excited`,
  $effect`Song of Bravado`,
  $effect`Glittering Eyelashes`,
  $effect`Big`,
  $effect`Confidence of the Votive`,
  $effect`Broad-Spectrum Vaccine`,
  $effect`Total Protonic Reversal`,
  $effect`Mystically Oiled`,
  $effect`Stevedave's Shanty of Superiority`,
]);
```

## Conclusion

It's not easy to sit down and start belting out competent CS TS code, especially if you're unfamiliar with anything from the KoL or programming side. However, taking it one step at a time and becoming acquainted with the task at hand and various existing solutions should get you to a point that you find desirable. This may be a list of CLI calls to paste in to set you up for your tests. This may be a fully fledged, re-entrant script inspired by existing TS scripts. The goal of scripting is to make things easier in the grand scheme of things, and finding a solution that works for you is what's important. The `#community-service` and `#mafia-and-scripting` channels should be able to help you out if you need it.
