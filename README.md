# Dino Game

This project is a simple implementation of the classic Dino game using vanilla JavaScript, HTML, and CSS. The code focuses on creating an interactive, real-time game where the player controls a dinosaur to jump over the cacti.

## Game Logic:
- Behind the scenes, the game's code dictates how the dinosaur moves and reacts to player input. It handles the animation of the dinosaur's movements, such as running and jumping, as well as the appearance and movement of obstacles like cacti. This ensures that the game feels responsive and realistic to the player's actions.
- The game creates the illusion of a scrolling desert landscape. As the dinosaur moves forward, the ground seems to scroll backward, giving the impression of continuous movement. This scrolling effect adds depth to the game world and enhances the player's immersion in the desert environment.
- The code manages the flow of the game from start to finish. It controls how the game begins, updates in real-time as the player progresses, and handles events like collisions with obstacles or reaching the end of the game. Additionally, it listens for player input, such as keyboard commands to make the dinosaur jump, ensuring an engaging and interactive experience.



## index.html

The `index.html` file sets up the basic structure of the game. It includes the main game elements within a world container where all elements are placed. The score display shows the current score of the player, and the start screen provides initial instructions for starting the game. The game area includes two ground elements for the scrolling ground effect and a dino element representing the dinosaur character that the player controls.

## cactus.js

The `cactus.js` script handles the creation and movement of cactus obstacles in the game. The **setupCactus** function initializes the cacti by setting the initial time for the next cactus and removing any existing cacti. The **updateCactus** function moves the cacti leftwards based on the game speed and delta time, removes cacti that have moved off-screen, and creates new cacti at random intervals. The **getCactusRects** function returns the bounding rectangles of all current cacti, which is useful for collision detection. The **createCactus** function creates a new cactus element, sets its initial position, and appends it to the game world.

## dino.js

The `dino.js` script controls the dinosaur character. The **setupDino** function initializes the dinosaur’s state, setting it to not jumping, resetting the animation frame, and setting the initial vertical velocity. The **updateDino** function handles both running and jumping actions. The **handleRun** function changes the dinosaur's animation frame while running, and the **handleJump** function updates the vertical position during a jump, applying gravity to bring the dinosaur back down. The **getDinoRect** function provides the bounding rectangle of the dinosaur for collision detection. The **setDinoLose** function changes the dinosaur's image to a losing state when the game ends. The **onJump** function handles the jump action triggered by a spacebar press.

## ground.js

The `ground.js` script manages the movement of the ground to create the illusion of the dinosaur running. It repositions ground elements continuously to simulate a moving ground and loops them back to the starting position once they move off-screen.

## script.js

The `script.js` script is the main entry point of the game. It initializes the game, handles the game loop, and manages the game's start and end conditions. The **handleStart** function starts the game by setting initial values and requesting the first animation frame. The **update** function updates all game elements (ground, dinosaur, and cacti) and checks for collisions. If a collision is detected, the game ends by calling **handleLose**, which resets the game after a short delay.

## updateCustomProperty.js

The `updateCustomProperty.js` script provides utility functions to handle custom properties (CSS variables) for game elements. The **setCustomProperty** function sets a custom property on an element, **incrementCustomProperty** increments a custom property’s value, and **getCustomProperty** retrieves the current value of a custom property.
