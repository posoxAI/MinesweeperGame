# Minesweeper

[Русская версия](README.ru.md)

A browser version of the classic game. Mines are hidden in the field; open every cell that has no mine and never step on one. It has the three classic field sizes, flags, a timer and best times.

**[Play in the browser](https://posoxai.github.io/MinesweeperGame/)**

<p>
  <img src="screenshots/day.png" width="300" alt="Minesweeper in the light theme with the Russian interface: a 16 by 16 field mid-game, with some mines flagged">
  <img src="screenshots/night.png" width="300" alt="The same game in the dark theme with the English interface, on the 9 by 9 field">
</p>

Left: the light theme with the Russian interface. Right: the dark theme with the English one.

## Rules

- A number in an open cell tells how many mines are in the eight cells around it.
- A cell with no mines around it opens all its neighbours by itself.
- A flag marks a cell where you think a mine is. The Mines left counter shows the number of mines minus the number of flags.
- Step on a mine and the game is lost. The field then shows every mine, and wrong flags are crossed out.
- The game is won when every cell without a mine is open. Flags are not needed to win.

## Field sizes

| Difficulty | Field | Mines |
| --- | --- | --- |
| Beginner | 9 × 9 | 10 |
| Intermediate | 16 × 16 | 40 |
| Expert | 30 × 16 | 99 |

On a narrow screen the Expert field is turned on its side, 16 × 30, so the cells stay big enough to tap.

## First move

Mines are laid after the first click. The opened cell and the eight cells around it get no mines, so the first move always opens some ground.

After that it is the classic game: the field is not guaranteed to be solvable by logic alone, and sometimes you have to guess.

## Controls

- Mouse: the left button opens a cell, the right button plants or removes a flag.
- A click on an open number opens its covered neighbours when exactly that many flags surround it. With a wrong flag this can set off a mine.
- Phone: a tap opens, a long press plants a flag. The Dig / Flag switch under the field swaps the two.
- Keyboard: arrow keys move the cursor, Space or Enter opens a cell, F plants a flag.

The clock starts with the first opened cell. A best time is kept for each difficulty, to a tenth of a second. An unfinished game, the best times and the settings are kept in the player's browser.

## Language

The interface is in English and Russian. It opens in Russian when Russian is among the browser's languages and in English otherwise. The RU/EN switch remembers your choice.

## How to run

The whole game is one file, `index.html`. There is no build step and there are no dependencies.

- Locally: open `index.html` in a browser.
- Online: the game is published with GitHub Pages at https://posoxai.github.io/MinesweeperGame/. Every commit to `main` updates it automatically.

Fonts load from Google Fonts. Without a network the game falls back to system fonts.

## Credits

The game was written by Claude, the AI assistant made by Anthropic: the logic, the canvas graphics, the sound and the page design.

The rules and the three field sizes come from the classic Minesweeper known from Windows. The design of this version is its own.

The idea of making a browser version came from posoxAI.

## License

MIT. The full text is in [LICENSE](LICENSE).
