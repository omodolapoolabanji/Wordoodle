# Wordoodle 'Wordle' Clone
This repository holds a wordle clone I made for my **CSI-C292** course's final project. It utilizes `Unity` and the `C#` language to create a doodle themed wordle clone
similar to that of the NewYork Time's. 
## Design Process and Description
The game is started out with blank keyboards which are filled during the `awake()` block and a fetch request queries the API provider for a valid 5-letter-word. User input is handled using the keyboard's characters and word tiles. The input is validated with another fetch request to an API provider then depending on the `JSON` response, we validate or invalidate the input. 

Validation is done first by checking if the word is valid, then for character placement on the word tiles and color coding the tiles (green if placement is right, yellow if placement is wrong but the character belongs in the winning word, and grey if the character does not belong in the winning word). After guessing the correct word the user wins the game and a streak system keeps count of the current streak and overall highscore by using a `static variable` for the streak and `playerprefs` for the highscore. 
## Major difficulty I ran into
The original iteration of this project used `File I/O` conventions to read from 2 word libraries into `Lists` for validation and winning word generation. The problem with this however was that on export, files got displaced and could not be read from. The next iteration featured hardcoded lists with a lot (and I mean a LOT) of words. The problem with this however is very obvious and that was the excessively slow runtime and this led to the game crashing severally. Finally I setup coroutines to handle API calls and worked around the problem. 

### Deployment
The project was deployed to itch.io [^1]. 
[^1]: [Check it out](https://omodolapoolabanji.itch.io/wordoodle)

> [!NOTE]
> Although this is a personal project, It is affiliated with my school. 
