## Jest Scrabble

***Lab:*** In your iteration planning meeting you were assigned the following stories for the current sprint. Use test driven development to implement the features.

### User stories

***Level One***
- When a player plays a word, the score of the word is calculated. Implement a function that returns the score of a word.
- A player is only allowed to play valid words. Implement a function that throws and error for invalid input that includes numbers or non-letter characters.
- When the game begins, each player receives 7 tiles from the `GAME_START_TILES` collection. Implement a function that returns a set of 7 random tiles. (*Requires stubbing Math.random**)

***Level Two***
- During the normal course of the game, players should have seven tiles. After a player plays a word, they will draw as many tiles as they need to bring their tile count back to seven. Implement a function that takes in the current tile distribution and an array of letters that the player has removed, and return the new tile distribution.

***Level Three***
- Ensuring that the tile selection only returns available tiles. For example, there is only one "Q", so the set of generated tiles can not include more than one "Q".

### Resources

***Tile Values***

The object below represents the VALUE of each tile used in calculating the word score.

```javascript

const LETTER_VALUES = {

"A": 1, "B": 3, "C": 3, "D": 2, "E": 1, "F": 4,

"G": 2, "H": 4, "I": 1, "J": 8, "K": 5, "L": 1,

"M": 3, "N": 1, "O": 1, "P": 3, "Q": 10, "R": 1,

"S": 1, "T": 1, "U": 1, "V": 4, "W": 4, "X": 8,

"Y": 4, "Z": 10, "blank": 0

}

```

- ***Tile Distribution***

The object below represents the quantity of each tile at the beginning of each game.

```javascript

const GAME_START_TILES = {

"A": 9, "B": 2, "C": 2, "D": 4, "E": 12, "F": 2,

"G": 3, "H": 2, "I": 9, "J": 1, "K": 1, "L": 4,

"M": 2, "N": 6, "O": 8, "P": 2, "Q": 1, "R": 6,

"S": 4, "T": 6, "U": 4, "V": 2, "W": 2, "X": 1,

"Y": 2, "Z": 1, "blank": 2

}

```

[Scrabble rules](http://www.scrabblepages.com/scrabble/rules/)