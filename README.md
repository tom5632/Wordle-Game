# Wordle-Game

Project 1 for General Assembly SEI

## Work plan

- [ ] Create HTML contents ✅
- [ ] Add basic CSS ✅
- [ ] Define the Model
    - Look up the list of possible 5 letter words that are playable ✅
    - create an array containing these words ✅

- [ ] Define basic logic 
    1) In the original wordle game, a new word is selected every day at 00:00:00 and players have exactly 24hrs to guess that word until a new word is selected. To begin with lets select a new word every time the page is loaded from the list of possible words (this will be shown in the console).✅

    2) When the user clicks a key on the keyboard, the letter corresponding to the key should appear in the appropriate square in the grid ✅. Alternatively, when the user clicks the 'backspace' key, the most recent tile should be cleared. ✅

    3) When the user enters a 5 letter word and presses 'ENTER', the controller should invoke a 'checkWord()' function that firstly checks if the word is valid (i.e is included in the list of possible words) ✅ and secondly compares it to the correct answer. 

        - Split the answer into an array of characters and compare each character to each corresponding tile. If they match - change the tile CSS to green. ✅ 
        - If the answer includes the tile but not at the correct index - change the tile CSS to yellow. ✅ 
        - Alternatively, if the answer does not contain the tile - change the tile CSS to grey. ✅
    
    4) The user must only be able to type a maximum of 5 letters until the word has been checked by the 'checkWord' function. Once the first guess has been checked, allow user to commence 2nd guess. ✅

        - NOTE: This prooved to be quite the challenge. How could I stop the user from guessing until the word had been checked by the 'checkword' function? At first I gave each square a unique Id corresponding to its index. If the index was a factor of 6; stop play and checkWord (Notice none of the squares have an Id divisible by 6). After the word had been checked, +1 to the tileIndex i.e. resume play. 

    5) Tiles that have been checked should have their corressponding letters on the keyboard coloured accordingly to alert the user which letters to include in subsequent quesses. ✅

    -[ ] Add CSS animations 
     1) When a tile is entered it should pop out and back slightly.


    ### Glitches to fix:

    - Restrict the user from being able to backspace previous rows
