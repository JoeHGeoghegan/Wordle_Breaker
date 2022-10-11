# Wordle_Breaker
A tool to solve Wordle, a game hosted by the New York Times, using the pandas python dataframes

## Usage
The wordlebreaker.ipynb file contains all the code necessary to utilize the below functions.

## Main tools
* play(auto_help=True,num_guesses=5)
    * Displays the 10 Best Guesses. Prompts for your guess, then prompts for Wordle's result.
    * Clears the print area and updates the word pool and scores and then displays updated best guesses
    * Repeats until result is all green or you have run out of guesses.
    * Can disable "auto_help" to stop it from giving you to top answers (Defaults to shown)
    * Can change "num_guesses" to change the number of guesses/turns allowed (Defaults to 5)
    > Essentially this code's autopilot for solving for the actual Wordle of the day!

* play_word(show_answer=False,auto_help=True,num_guesses=5)
    * Same as play but you get to choose the word!
    * It will evaluate your guesses as you go!
    * Can enable "show_answer" to show the answer (Debug Mode, defaults to off)

* play_random(show_answer=False,auto_help=True,num_guesses=5)
    * Chooses a random word for you to play
    * It will evaluate your guesses as you go!
    * Can enable "show_answer" to show the answer (Debug Mode, defaults to off)

* auto_solve(solution,printable=True)
    * Computes how many turns it would take to solve a particular solution.
    * If "printable" is true will return a readable string represenation, if false the number of turns will be returned

* process_guess(guess, result):
    * Takes a guess and result and cuts the word pool to only include possible words based on the result's information.
    >guess: string of 5 characters, representing the word you guessed on Worlde
    >result: string of 5 characters, representing the color response by Wordle
    >* g/G means green
    >* y/Y means yellow
    >* b/B means black

* update_scores(sort-(defaults to True)):
    * Populates/updates the score value to a rudamentary point system
        * The score is a sum of character scores for each character in a word
        * Note: This scoring system will not solve every Wordle automatically, fails in 62 cases. The purpose of this code is to assist not solve it for you

    > The character score is the count of the letter's occurances in the entire word pool's population at that character spot.
    > Change sort to false if you do not want the list to be resorted.

* disp()
    * Displays only words and the score to help inform your next guess     
