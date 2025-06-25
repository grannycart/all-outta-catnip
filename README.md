# All Outta Catnip
*A warning right off the bat: it is impossible to read any of this documentation without hitting spoilers. So if you want to _play_ this scenario, you should stop reading here and give it to someone who could potentially DM it for you.*

This repo contains an All Outta Bubblegum scenario that is based loosely on Dwarf Fortress.

## What is All Outta Bubblegum?
It's a tabletop RPG with maybe 5 rules, and based on a single line from the 80s action movie [They Live](https://youtu.be/Du5YK5FnyF4?t=23). Basically, you can only do two things: chew gum or kick ass. Eventually you can _only_ kick-ass. [Read the rules as originally written here](./all-outta-bubble-gum.md).

While the rules are awesome, it's challenging to come up with a playable scenario for the game. This repo is one such scenario, inspired by Dwarf Fortress.

## What is Dwarf Fortress.
Can't get into that here. Go google it. But one of the (many, possibly infinite) things that can happen in Dwarf Fortress is a [catplosion](https://dwarffortresswiki.org/index.php/DF2014:Catsplosion) where cats start reproducing at such a rate that they take over your fortress. (Actually, this can happen with any animal in Dwarf Fortress, but it's a particular problem with cats because the dwarves often adopt them as pets, and then won't allow them to be culled...)

The main goal of the scenario is for the players to prevent a catplosion. There are many ways to achieve this, not all of them pleasant.

You do not have to have played Dwarf Fortress to play this scenario (but it will make more sense if you have).

## Another warning before you jump in
The main goal of the scenario is to prevent a cat population bomb. While it's _possible_ to do that in the scenario without _harming_ cats, it's much more likely to get brutal, particularly as the gum runs out. This is actually the point. The scenario (if all goes well) should _force_ the players to start kicking-ass --- _cat_ ass. While this might sound funny on the face of it, it could also get all too real. Some players might have real problems with it. Obviously it's your job as the DM to make sure the players don't get uncomfortable. A good measure that you are doing a good job is if, as the players get forced into more reprehensible actions, you are getting groans, not tears. It's supposed to be funny.

Having said that, the cat overpopulation is a very real problem in the real world. And all those cute little fuzzy friends of ours are doing real damage to the world in dramatic ways. Maybe it's not the worst thing to force people to choose between cute fuzziness and the good of the fortress.

This is why there is "A warning from the DM" at the begining of the scenario. Feel free to modify/adapt/drop based on your players. Just don't let your players go into the game believing it's nothing but lighthearted fun! (Of course if your players are all a bunch of assholes who think golfing cats with a giant hammer is hilarious, then you have nothing to worry about.)

## The Scenario
* See: [AOBG-DF-catplosion-mashup-scenario.md](./AOBG-DF-catplosion-mashup-scenario.md)
* The [maps/](./maps/)) folder contains ASCII maps and pdfs of the levels
* [post-test-play-notes.md](post-test-play-notes.md) --- things I want to fix after the first round of play-testing.
* [all-outta-bubble-gum.md](all-outta-bubble-gum.md) --- the rules for AOBG

## License:
* MIT (Except the original AOBG rules, which are still under whatever copyright they were originally released under and are included here only for convenience.)
* See: [LICENSE](./LICENSE)

--------------------------------------------------------------------------------

## Map making and editing
* I used asciiflow to draw the maps: https://asciiflow.com/#/
    * https://github.com/lewish/asciiflow
* Copy the text out of ascciflow and paste into your favorite editor. 
    * (Note you are likely to have used unicode-only characters like `├ ─ ┐` which cab be a problem for some editors.)
    * You can paste the ASCII back into asciiflow if you want to use it to make further edits.
    * Note for vim users (like me): vim can handle unicode, but if you try to :hardcopy the file, vim sends it to the printer dropping the unicode, so those characters all come out as upsidedown question marks. 
* Best method is to print using pandoc to create a pdf.

### Printing the map:
* Be sure to install:
    * pandoc
    * xelatex (texlive-core package)
    * Install JetBrains font: `sudo pacman -S ttf-jetbrains-mono` on Arch Linux
* Use pandoc to convert text to pdf:
    * `pandoc map.txt -o map.pdf --pdf-engine=xelatex -V monofont="JetBrains Mono" -V fontsize=12pt -V geometry:margin=0.3in`
    * The maps are put in code blocks (three backticks) because sometimes pandoc doesn't treat the text as monospace (throws a `Missing character` error) and then doesn't use the JetBrains font.
    * (You'll have to use this command if you want to make a pdf version of these instructions too. Or just delete the one place with unicode characters.)



