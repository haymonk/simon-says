# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **Haymon T.**

Time spent: **4** hours spent in total

Link to project: https://simon-says-memory.glitch.me

## Required Functionality

The following **required** functionality is complete:

* [x] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [x] "Start" button toggles between "Start" and "Stop" when clicked. 
* [x] Game buttons each light up and play a sound when clicked. 
* [x] Computer plays back sequence of clues including sound and visual cue for each button
* [x] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [x] User wins the game after guessing a complete pattern
* [x] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [x] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [x] Buttons use a pitch (frequency) other than the ones in the tutorial
* [x] More than 4 functional game buttons
* [x] Playback speeds up on each turn
* [ ] Computer picks a different pattern each time the game is played
* [x] Player only loses after 3 mistakes (instead of on the first mistake)
* [x] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] A progress tick indicating the number of consecutive correct guesses

## Video Walkthrough

Here's a walkthrough of implemented user stories:
Full walkthrough - **https://recordit.co/os4ICy5GVr**
<img src='http://g.recordit.co/os4ICy5GVr.gif'>


## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 
Aside from the additional links provided in the tutorial, such as w3schools.com for CSS fonts or about the JS library and synthesizing sound, the other resource I used was by GeeksForGeeks to customize each button with an image upon clicking it (https://www.geeksforgeeks.org/how-to-change-an-input-button-image-using-css/). Instead of following their guide for loading an image upon hovering a button, I altered it to load an image upon clicking and activating a button.

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 
The greatest challenge was implementing the code behind the guess button without assistance. Though the logic seemed simple, it was more difficult to write code in ways that the computer could understand. First, I had to write out step-by-step the possible paths that could come from guessing (e.g. correct/incorrect, the last guess, winning, etc.). While the provided flow chart helped me walk through the logic, I determined how to write my code by identifying the edge cases, with the simplest one being if the player guessed incorrectly. If a player guessed wrong, then the game automatically ended. This was the fastest case and thus became the outermost conditional statement in my program. However, if the player guessed correctly, then I had to use a variable that could store the progress of each guess. Implementing this "progress" proved to be challenging as I was initially unsure of how to tie this with "guessCounter". Eventually, I broke down each step and tried to think of what could be the next outermost conditional statement, essentially the "bigger picture". Overall, though nested conditional statements proved to be the most challenging, taking a step back and slowly dissecting each process made the code easier to implement. Rather than coding arbitrarily, utilizing the provided flow chart along with writing out my own on the side helped me determine the proper sequence and code needed to correctly implement the guesses.

Additional challenges I faced were implementing the three strikes for incorrect guesses. When I immediately went in to write the code, several errors followed, such as the playClueSequence() always speeding up, despite an incorrect guess. Logically, it would make sense for the computer to replay at the same speed the player guessed incorrectly rather than continue speeding up. Similar to the former challenge with the logic behind the guess button, I had to break each step and print various variables in different loops to determine where my code went wrong. Debugging this took a substantial amount of time, especially since it's tied to playClueSequence() and relies on the speed remaining consistent for that turn (clueHoldTime). Rather than thinking about the three strikes and speeding up features as two separate components, I had to determine their correlations and finure out a way to apply one without disrupting the functions of the other.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 
After realizing the amount of information stored for this single page, I wonder how websites with greater traffic and information manage to store all of their data? 
After realizing the amount of information stored for this single page, I wonder how websites with greater traffic and information manage to store all of their data? Also, in UX/UI design, how do you get the color schemes and proportion of elements correct on a page to display everything in an aesthetically pleasing manner? For backend development, while Javascript can be used in both frontend and backend, when would it be more useful to use Python? Additionally, is it possible to use multiple languages in the backend like how frontend uses CSS and HTML, or is it more cumbersome to maintain in the backend?

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 
If I had additional time, I would likely come back to work on implementing all of the optional features listed on the project. In addition, I would incorporate a feature where users can view their progress. Visualizing a player's progress will let them know how much longer until they reach the last clue (eighth), so players don't have to rely on keeping up with this number themselves. Since the memory game resembles that of the electronic Simon game, I would also like to change the buttons to mimic the circular and arc shape of the physical toy rather than leaving the game buttons in a rectangular shape.



## License

    Copyright Haymon Thit

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
