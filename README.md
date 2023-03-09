# Haskell Tiny Game Jam

![](hackage/ski/ski-lol10-fs8.png)

The first Haskell tiny games contest has taken place in February 2023.
Inspired by the [BASIC 10Liner contest](https://www.homeputerium.de)
(see their english rules at the bottom of that page, and [their 2023 entries](https://gkanold.wixsite.com/homeputerium/games-list-2023)).
Your mission: make a playable game in 10 lines of 80 characters of Haskell.
The prize.. glory! 
Also fun, learning, and advancing Haskell's suitability for game dev and programming in the small.

The contest ended 2023-02-28 23:59:59 UTC and is now in judging phase.


<div align=center>

[Rules](#rules)
| [Games](#games)
| [Let's play!](#lets-play)
| [Development](#development)

</div>

[Matrix]: https://matrix.to/#/#haskell-game:matrix.org
[IRC]:    https://web.libera.chat/#haskell-game

## Rules

Entries were submitted in the last three weeks of February 2023.
sm and f-a are your judges.
See the #haskell-game [Matrix] or [IRC] chat 
or this repo's [issue tracker](issues) for help/feedback/announcements.

Here were the contest rules for this round:

1. You can submit any number of entries to the official repo, haskell-game/tiny-games-hs.
   Each should be a playable game or amusement in one haskell file
   of up to 10 lines of up to 80 characters each, in one of the following categories:
   - `prelude-10-80`, allowing no imports
   - `base-10-80`, allowing imports from the base package
   - `default-10-80`, allowing imports from GHC's default packages, 
     plus an optional file named `Import.hs` to gather and re-export imports (only)
   - `hackage-10-80`, allowing imports from all of Hackage, and an `Import.hs` file.

2. The entry can be a script ([runghc], [stack], [cabal], ...)
   or a small program requiring compilation, but not a multi-file project.
   Our ideal is a self-contained executable 10 line program that just works, like BASIC programs.
   Here are some templates to give ideas:
   [prelude/template1](prelude/template1.hs),
   [base/template1](base/template1.hs),
   [default/template1](default/template1.hs),
   [hackage/template1](hackage/template1.hs)

3. Unlimited comments are permitted after line 11.
   The game's `category/gamename (author)` info should appear here,
   plus any essential info like player controls, so that the game is usable
   to someone seeing just this file.

4. Achieving programs that "just work" is a core principle and part of the challenge.
   The script or program must either
   be reliably runnable via shebang line (these use up your line count, but improve runnability; `env -S` is allowed)
   or contain a reliable build/run command line with all needed options, in the comments
   (the `play` script will use this).
   Games which aren't straightforward to run and enjoy are incomplete.
   See also the [runnability](#runnability) tips below.

5. The game should be portable, running on all major platforms, ideally.

6. A square thumbnail (screenshot) must be provided for the repo README -
   either a static png (which will be hyperlinked)
   or an animated gif (which should not be, so as not to break Github's player overlay).

7. A README file is optional but makes browsing your game more pleasant for website visitors.
   Feel free to include animations, or discussion of the game/code/your experience.

8. An unminified version of the code, easier to read and learn from, is optional but welcome.

9. You can update your entries freely until the contest end, 2023-02-28 23:59:59 UTC,
   at which time they are frozen (in the `contest` branch) for posterity and judging
   (no exceptions except minor updates at judges' discretion, eg metadata fixes).
   Also the last commit received before deadline has been tagged with the `pre-deadline` tag.
   If you need to share post-contest improvements, you are welcome to keep publishing updates in the `main` branch.
   The main version is the one that will be presented to players.

[runghc]: https://downloads.haskell.org/ghc/latest/docs/users_guide/runghc.html
[stack]:  https://docs.haskellstack.org/en/stable/script_command
[cabal]:  https://cabal.readthedocs.io/en/3.6/cabal-commands.html#cabal-v2-run

## Games

Here are all the entries!

### prelude-10-80
<!-- (No imports) -->
<table>
<tr>
<td><a href="prelude/guess1"><img src="prelude/guess1/guess1.png" width=140 height=140><br>guess1</a><br>(sm)</td>
<td><a href="prelude/pure-doors"><img src="prelude/pure-doors/pure-doors.png" width=140 height=140><br>pure-doors</a><br>(tristanC)</td>
<td><a href="prelude/fifteen"><img src="prelude/fifteen/fifteen.png" width=140 height=140><br>fifteen</a><br>(bradrn)</td>
<td><img src="prelude/chess/chess.gif" width=140 height=140><a href="prelude/chess"><br>chess</a><br>(fizruk)</td>
<td><a href="prelude/sudoku"><img src="prelude/sudoku/sudoku.png" width=140 height=140><br>sudoku</a><br>(elderephemera)</td>
</tr>
<tr>
<td><img src="prelude/matchmaking/matchmaking.gif" width=140 height=140><br><a href="prelude/matchmaking">matchmaking</a><br>(migmit)</td>
<td><img src="prelude/tiny-brot/tiny-brot.gif" width=140 height=140><br><a href="prelude/tiny-brot">tiny-brot</a><br>(tristanC)</td>
<td><img src="prelude/mini-othello/mini-othello-1.gif" width=140 height=140><br><a href="prelude/mini-othello/mini-othello.hs">mini-othello</a><br>(hellwolf)</td>
<td><a href="prelude/one-dot"><img src="prelude/one-dot/one-dot.png" width=140 height=140><br>one-dot</a><br>(OsePedro)</td>
<td><a href="prelude/expressit"><img src="prelude/expressit/expressit.png" width=140 height=140><br>expressit</a><br>(Greg8128)</td>
</tr>
<tr>
<td><a href="prelude/life"><img src="prelude/life/life.png" width=140 height=140><br>life</a><br>(Rens van Hienen)</td>
<td><img src="prelude/call-by-push-block/call-by-push-block.gif" width=140 height=140><br><a href="prelude/call-by-push-block">call-by-push-block</a><br>(cole-k)</td>
<td><a href="prelude/companion"><img src="prelude/companion/companion.png" width=140 height=140><br>companion</a><br>(Greg8128)</td>
<td><a href="prelude/hangman"><img src="prelude/hangman/hangman.png" width=140 height=140><br>hangman</a><br>(kukimik)</td>
<td><a href="prelude/quine"><img src="prelude/quine/quine.png" width=140 height=140><br>quine</a><br>(tristanC)</td>
</tr>
</table>

### base-10-80
<!-- (Just the base package) -->
<table>
<tr>
<td><a href="base/timing"><img src="base/timing/timing.png" width=140 height=140><br>timing</a><br>(TravisCardwell)</td>
<td><a href="base/shoot"><img src="base/shoot/shoot.png" width=140 height=140><br>shoot</a><br>(migmit)</td>
<td><img src="base/log2048/log2048.gif" width=140 height=140><a href="base/log2048"><br>log2048</a><br>(Lysxia)</td>
<td><img src="base/rhythm/rhythm.gif" width=140 height=140><a href="base/rhythm"><br>rhythm</a><br>(elderephemera)</td>
<td><a href="base/peyton-says"><img src="base/peyton-says/peyton-says.png" width=140 height=140><br>peyton-says</a><br>(gergoerdi)</td>
</tr>
<tr>
<td><a href="base/acey-deucey"><img src="base/acey-deucey/acey-deucey.png" width=140 height=140><br>acey-deucey</a><br>(trevarj)</td>
<td><a href="base/flower-seeds"><img src="base/flower-seeds/flower-seeds.png" width=140 height=140><br>flower-seeds</a><br>(tristanC)</td>
<td><img src="base/lambda-ray/lambda-ray.gif" width=140 height=140><br><a href="base/lambda-ray">lambda-ray</a><br>(tristanC)</td>
<td><a href="base/7up7down"><img src="base/7up7down/7up7down.png" width=140 height=140><br>7up7down</a><br>(akshaymankar)</td>
<td><a href="base/snake"><img src="base/snake/snake.png" width=140 height=140><br>snake</a><br>(akshaymankar)</td>
</tr>
<tr>
<td><img src="base/woosh/woosh.caves.gif" width=140 height=140><a href="base/woosh">woosh.caves</a><br>(Kindaro)</td>
<td><img src="base/woosh/woosh.forest.gif" width=140 height=140><a href="base/woosh">woosh.forest</a><br>(Kindaro)</td>
</tr>
</table>

### default-10-80
<!-- (Just the packages that come with GHC) -->
<table>
<tr>
<td><a href="default/type-and-furious"><img src="default/type-and-furious/type-and-furious.png" width=140 height=140><br>type-and-furious</a><br>(lsmor)</td>
<td><a href="default/shmupemup"><img src="default/shmupemup/shmupemup.png" width=140 height=140><br>shmupemup</a><br>(elderephemera)</td>
<td><img src="default/tsp/tsp.gif" width=140 height=140><br><a href="default/tsp">tsp</a><br>(tristanC)</td>
<td><img src="default/lol/lol.gif" width=140 height=140><br><a href="default/lol">lol</a><br>(hellwolf)</td>
<td><a href="default/space-invaders"><img src="default/space-invaders/space-invaders.png" width=140 height=140><br>space-invaders</a><br>(meooow25)</td>
</tr>
<tr>
<td><img src="default/swish/swish.easy.gif" width=140 height=140><a href="default/swish">swish.easy</a><br>(Kindaro)</td>
<td><img src="default/swish/swish.survival.gif" width=140 height=140><a href="default/swish">swish.survival</a><br>(Kindaro)</td>
<td><a href="default/lc"><img src="default/lc/lc.png" width=140 height=140><br>lc</a><br>(byorgey)</td>
</tr>
</table>

### hackage-10-80
<!-- (All of Hackage) -->
<table>
<tr>
<td><a href="hackage/guess2"><img src="hackage/guess2/guess2.png" width=140 height=140><br>guess2</a><br>(sm)</td>
<td><a href="hackage/wordle"><img src="hackage/wordle/wordle.png" width=140 height=140><br>wordle</a><br>(halogenandtoast)</td>
<td><a href="hackage/ski"><img src="hackage/ski/ski.png" width=140 height=140><br>ski</a><br>(sm)</td>
<td><a href="hackage/guesscolor"><img src="hackage/guesscolor/guesscolor.png" width=140 height=140><br>guesscolor</a><br>(TravisCardwell)</td>
<td><a href="hackage/bulls-n-cows"><img src="hackage/bulls-n-cows/bulls-n-cows.png" width=140 height=140><br>bulls-n-cows</a><br>(akadude)</td>
</tr>
<tr>
<td><img src="hackage/hallway-to-hell/hallway-to-hell.gif" width=140 height=140><br><a href="hackage/hallway-to-hell">hallway-to-hell</a><br>(juliendehos)</td>
<td><a href="hackage/1234-hero"><img src="hackage/1234-hero/1234-hero.png" width=140 height=140><br>1234-hero</a><br>(gelisam)</td>
<td><a href="hackage/crappy-flappy"><img src="hackage/crappy-flappy/crappy-flappy.png" width=140 height=140><br>crappy-flappy</a><br>(gergoerdi)</td>
<td><a href="hackage/pong"><img src="hackage/pong/pong.png" width=140 height=140><br>pong</a><br>(gergoerdi)</td>
<td><a href="hackage/minesweeper"><img src="hackage/minesweeper/minesweeper.png" width=140 height=140><br>minesweeper</a><br>(Greg8128)</td>
</tr>
<tr>
<td><a href="hackage/pong2"><img src="hackage/pong2/pong2.png" width=140 height=140><br>pong2</a><br>(sm)</td>
<td><a href="hackage/brickbreaker"><img src="hackage/brickbreaker/brickbreaker.png" width=140 height=140><br>brickbreaker</a><br>(fgaz)</td>
<td><img src="hackage/lazy-march/lazy-march.gif" width=140 height=140><br><a href="hackage/lazy-march">lazy-march</a><br>(tristanC)</td>
<td><a href="hackage/balances"><img src="hackage/balances/balances.png" width=140 height=140><br>balances</a><br>(sm)</td>
<td><a href="hackage/vaders"><img src="hackage/vaders/vaders.png" width=140 height=140><br>vaders</a><br>(gergoerdi)</td>
</tr>
<tr>
<td><a href="hackage/tetris"><img src="hackage/tetris/tetris.png" width=140 height=140><br>tetris</a><br>(gergoerdi)</td>
<td><a href="hackage/short-guess"><img src="hackage/short-guess/short-guess.png" width=140 height=140><br>short-guess</a><br>(RimuhRimu)</td>
<td><a href="hackage/hexescape"><img src="hackage/hexescape/hexescape.png" width=140 height=140><br>hexescape</a><br>(nevrome)</td>
<td><a href="hackage/snake-lemma"><img src="hackage/snake-lemma/snake-lemma.png" width=140 height=140><br>snake-lemma</a><br>(gergoerdi)</td>
<td><a href="hackage/subpar-hexagon"><img src="hackage/subpar-hexagon/subpar-hexagon.png" width=140 height=140><br>subpar-hexagon</a><br>(gergoerdi)</td>
</tr>
</table>

## Let's play!

You will need a suitable version of GHC (9.2.5+ or 9.4.4+ recommended), and stack (or cabal).
See <https://www.haskell.org/get-started/>.
Once Haskell is installed, and if you have bash, you can run `./play` in this repo:

![](play.dark.png)

or:

![](play-2.dark.png)

If you don't have bash, cd into each `*/GAME` directory and try running `GAME.hs`.
If that fails, look for running clues in that file, a readme, or the `play` script.
You can also run `./play GAME -h` to view a game's source code and readme.

The [lol](default/lol/) entry is a meta "game" that colourises other games.
It works with most games but may cost a little performance.
(Hint: each extra "lol" argument modifies the effect.)

![](play-lol.dark.png)

### More install/run tips

Some games use unicode glyphs, emojis and/or double-width characters.
For best results:

- Use a terminal with good support for double-width characters
- And with a font configured that contains attractive unicode glyphs and emojis.
- On mac, don't use the default Terminal or iTerm 3.4 or less, they render emojis slowly.
  Use a faster terminal, such as iTerm 3.5 beta, or the terminal built in to VS Code.

Many games are implemented as [stack scripts](https://docs.haskellstack.org/en/stable/script_command/)
for reliable running and compactness. You can install stack with ghcup (see the get-started link above).
Note:

- When you run a game for the first time, stack will automatically fetch the latest package database
  and install the required GHC version and haskell dependencies if needed.
  This can take a long time (eg minutes), up to 1-2G of disk space, and may or may not show progress output.
  The OpenGLRaw package required by the graphical, gloss-based games is particularly slow to build.
  If you need more progress output, you can add --verbosity info to the game's shebang line or run command in `play`.

- We have configured all games to use the same GHC version (from the latest LTS snapshot at stackage.org). 
  If you have a similar GHC version/stackage snapshot already installed
  (or even a quite different one that you think might work), you can try using it instead,
  to save on install time and disk space. In the games' shebang lines or run command in `play`,
  change the `--resolver` argument to your snapshot and see if they run.

To quit graphical games built with the gloss library, press the ESCAPE key.

If you see an error message like "user error (unknown GLUT entry glutInit)",
install the system package named "freeglut" or similar using your system package manager.

Nix users: a flake.nix is provided; running `nix develop .` should give you
a reproducible environment for running the games.


## Development

Tips for developers while the jam was in progress, and for future jams.

### Runnability

- Avoid requiring problematic GHC versions. In particular GHC <9.2 doesn't work well on mac.
   If you specify a GHC version/stackage snapshot, the current release is ideal (GHC 9.2, lts-20).
- env -S in the shebang line doesn't work on older GNU/Linux systems, but we allow it
   (see https://github.com/haskell-game/tiny-games-hs/issues/25).
- stack scripts can seem to hang at first startup while downloading snapshot info.
   For prelude/base/default categories, using --resolver=ghc-9.2.5 avoids this
   (see https://github.com/haskell-game/tiny-games-hs/issues/38).
- stack scripts can use --verbosity=error to silence the "Selected resolver" output.
  (Or --verbosity=info to show dependency building progress.)
- If using packages which require compilation (gloss) or more speed, use stack script --compile or stack script --optimize.
  (Downsides: creates .o and .hi files; a compiled binary with newer timestamp than source can cause confusion.)
- cabal scripts are also welcome; they don't have --compile and require more lines (unless you use env -S)
- On mac, Terminal and iTerm 3.4 render emojis very slowly; iTerm 3.5 beta or VS Code terminal work better.

### Minifying

Here are some minifiers you can try; either or both may be able to turn your game into
a brick of inscrutable code no more than 80 characters wide.

- [hackage/brickbreaker/minify.hs](hackage/brickbreaker/minify.hs) (from haskell-game/tiny-games-hs#63; contact @fgaz)

  This minifier requires that you first add curled braces and semicolons throughout your code to make it white space insensitive.

- [minify.hs](minify.hs) (from haskell-game/tiny-games-hs#14; contact @kindaro with issues/feedback)

  #### Features

  * Will automatically add curly braces for you so long as you put the line
    `module Main where` into your source file. _(This line will then be
    automatically removed, so you lose no space.)_
  * Will automatically replace variables and constructors surrounded with curly
    braces `{example}` with single letters, for extra minification.

### Animations

Here's one way to make animated GIFs or APNGs for your README (see also [ski/Makefile](hackage/ski/Makefile)):

```
# Install Noto Emoji font, required by agg to show emojis
$ asciinema rec game.cast
$ agg -v --cols 80 --rows 25 --font-family 'Essential PragmataPro' --font-size 16 game.cast game.lg.gif
$ gifsicle -V --lossy=50 -k8 -O2 -Okeep-empty game.gif -o game.gif
$ gif2apng game.gif game.png
```

agg doesn't show colour emojis [yet](https://github.com/asciinema/agg/issues/2).
The Noto Emoji glyphs are monochrome and less pretty, but will give the idea.
(asciicast2gif which predates agg does show colour emojis, but doesn't convert ansi-terminal-game output well.)

Shrinking the gif, eg with gifsicle, is recommended for repo longevity and page load times.
It helps gif2apng a lot also.

[APNGs](https://github.com/haskell-game/tiny-games-hs/issues/70) are preferable if you can manage it:
they will not be obscured by Github's gif player button, they can be hyperlinks, and they can have smaller file size.
https://sourceforge.net/projects/gif2apng works well, it can be built from its source tarball.

### Experience reports

- <http://miaozc.me/2023-02-27-hs-tiny-games.html>
- <https://tristancacqueray.github.io/blog/tiny-game-engine>
- <https://www.cole-k.com/2023/02/21/tiny-games-hs/>
