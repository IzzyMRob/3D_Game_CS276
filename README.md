# Creativly Named FPS

## Play the Game
**Unity Play Link**: (https://play.unity.com/en/games/a7af36f3-a6fb-4b64-85f8-081c2c48b511/creatively-named-fps)
I dont think the game plays in unity, i literally have no idea why. It is uploaded the exact same way all the other game are, it works perfectly fine in the editor. Also, I am very sorry if this is not well-written, I am getting sick and do not feel well. Sorry, I liked this project.

## Game Overview
Explore your environment and fight multitudes of robot enemies.

### Controls
- Use WASD to move
- Use Space to jump
- Shoot with the left mouse, aim with the right
- Pause with Escape

## Base Game Implementation

### Completion Status
- [x] Player movement and controls
- [x] Obstacle spawning system
- [x] Collision detection
- [x] Score system
- [x] Game over state
- [X] Pause Menu
- [X] Dynamic Lighting for Enemies
- [X] Health Pickups
- [X] Changed Enemy Spawning Rules

## Extensions Implemented

### 1. Pause Menu
**Implementation**: I added a UI element for the pause menu, and set it active and paused the time when the player hits the pause button.
**Game Impact**: Gives the palyer more controll over the game, and lets them take a break while playing.
**Technical Details**: Created a UI and  activated it with the Escape button. Paused and resumed the game time when paued or played.
**Known Issues**: WHen the game is over the menu can still be opened, it will overlap the win text.

### 2. Dynamic Lighting
**Implementation**: I edited the perfabs of the enemies to have lights in them corresponding to their colors, and made the environment darker. I also gave the player a "flashlight" that matches the gun color to make them feel more grounded in the scene.
**Game Impact**: The game feels darker and more sinister, and it looks a lot cooler to play.
**Technical Details**: I added lights to the prefabs of each enemy matching their glow color, and dimmed the preexisting directional lights significantly. The player's light is a child of the camera so it follows their mouse movement, and it is slightly in front of them to avoid hitting the guns.
**Known Issues**: N/A

### 3. Health Pickups
**Implementation**: I added a new type of pickup that gives the player 5 health when they get it.
**Game Impact**: The player has more of a chance to recover from making a mistake and getting hit by something, it feels more fun to play because it isn't as one-and-done.
**Technical Details**: The health pickips look likt the ammo ones, except they are a skinnier shape. I didn't want to change too much but it still looks distinct enough to be recognized from a distance. They will always give the player 5 health, I also didn't want to force a max health in this game because I think it is unlikley the player ever gets that much extra health, so a few bars doesn't make a negative impact.
**Known Issues**: N/A

### 4. Health Pickups
**Implementation**: I gave each spawner a limit n how many enemies it could spawn.
**Game Impact**: It feels more concrete and managable to win the game bacause enemies don't spawn infinitly.
**Technical Details**: I added an if statement into the Spawn coroutine to check if the amount of enemies spawned by this spawner is equal to the max, and if so not spawn anymore.
**Known Issues**: N/A

## Credits
- All visual assets from the base template repository.
- Scripts from the base template reposetory and edited by me.

## Reflection
**Total Points Claimed**: Base: 80% + Extensions: 3x
**Challenges**: One of the most difficult parts was diving into the code someone else had written and understanding what every part of it meant. Whei I wanted to change something about the game I had to do wuite a lot of searching through files to find where specific things happened.
**Learning Outcomes**: I got good practice working with a game design that has SOLID principle application. It took a bit to understand from the outside, but once I got it many things were straightforward to change.

## Development Notes
I think I would much rather have created my own game from scratch, however given the time constraints of the assignment I know it wouldn't have been at this level had I done so.
