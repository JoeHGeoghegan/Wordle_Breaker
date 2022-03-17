# Wordle_Breaker
A tool to solve Wordle, a game hosted by the New York Times, using the pandas python dataframes

## Main tools
* play()
    * Displays the 10 Best Guesses. Prompts for your guess, then prompts for Wordle's result.
    * Clears the print area and updates the word pool and scores and then displays updated best guesses
    * Repeats until result is all green or you have run out of guesses.
    > Essentially this code's autopilot!
* process_guess(guess, result):
    * Takes a guess and result and cuts the word pool to only include possible words based on the result's information.
    >guess: string of 5 characters, representing the word you guessed on Worlde
    >result: string of 5 characters, representing the color response by Wordle
    >* g/G means green
    >* y/Y means yellow
    >* b/B means black

* update_scores(sort-(defaults to True)):
    * Populates/updates the score value to a rudamentary point system
        *  The score is a sum of character scores for each character in a word

    > The character score is the count of the letter's occurances in the entire word pool's population at that character spot.
    > Change sort to false if you do not want the list to be resorted.

* disp()
    * Displays only words and the score to help inform your next guess     