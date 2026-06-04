# GDIM 33 In-Class Activities
## W1
### Activity 1

[Pinterest](https://pin.it/I6WVC8aFu)
1. All the games are rage/foddian or climbing games, they are one of my favorite genres of games by far. 
2. My tablemate Landon is really interested in Elden Ring, a similarly punishing genre. It's punishing with combat challenges rather than platforming, but it is still a game that is both mechanically challenging and rewarding.
3. My LA also expressed interest in Souls games like Bloodborne as well as games like Minecraft. Minecraft is a game that also has a lot of platforming challenges, which I really want to channel in my vertical slice.

### Activity 2
<img width="2494" height="3222" alt="Activity2Breakdown" src="https://github.com/user-attachments/assets/4d05e522-bece-4869-92f3-57cc2e85e90a" />


## W2
<img width="2494" height="3136" alt="climbingfoddiangameBreakdownV2" src="https://github.com/user-attachments/assets/59b208a5-3d41-4d9a-b802-ba58ae2a5854" />


1. Its advantageous to save as a scene variable so that you can easily reference it in other scripts and not have to worry about getting the name wrong.
2. Debug log helped me figure out click was being triggered
3. Yes, because the cursor is locked in gameplay and unlocked in UI menus.
4. Yes, game states are relevant to my slice because there are multiple states that the player can be in.


## W3

### Activity 1

Right now the basic climbing is implemented. The player can control each arm with Left and Right Joystick accordingly, and the player can grab onto the air and climb up. I still need to implement kbm movement, and only being able to grab level walls.

__Here are my playtesting goals__
- See if the climbing speed is good and responsive with the controller
- See if it feels intuitive. Do the controls make sense to use? Do they feel natural? There is an expected learning curve, but it shouldnt feel completely foreign to use after a while.

Playtesting Group
- Rebecca Feng
- Frances Kim 
- Landon Her
- Jess Tran
- Kaleb Reyes

### Playtesting notes
- Arm movement should move at exponential curve instead of linear curve, allowing for minute movements to be more precise and larger movements to be faster.
- Joystick movement should reflect real life climbing movement. You should be able to pull down with the arm that is grabbing, and still move the other arm freely. Right now the non grabbing arm is the only thing you can move around. This reflects a keyboard and mouse only control sceheme, but should be changed specifically for controller.
- Add walls that you can only grab onto, remove grabbing onto air.

### Activity 2
1. Yes they could easily add more dialogue because scriptable objects allow for easy data management outside of the code (MVC). Scriptable objects are specifically allow to be edited in the inspector.
2. There is no limit to the number of dialogue nodes. Writers could easily allow a dialogue that has 100 nodes if they wanted to.
3. Regenerate nodes is like hitting refresh to make the visual scripting aware of the changes you have made to the project. If you add something new, sometimes the graph won't be aware of it until you regenerate nodes.

## W5
### Activity 1
Intro Cutscene

1. Make new scene and UI for cutscene
	- Duplicate scene
	- Play timeline on start of scene
	- Move to main scene on timeline finish
2. Import rigs
	- Add rig of Player properly scaled with the current player model
	- Add rig of the Bird with the included animations
	- Add sandwich rig/model?
3. Move rigs and camera in timeline w/ animation 
	- Add rigs to timeline
	- Move camera in timeline 
	- Move rigs in timeline
	- Add animations to timeline

### Activity 2
- Added timeline that rotates camera and player, and then switches to the main gameplay scene.
- Added rig for the bird and animation, and made the bird fly by the player.

## W6
### Activity 1
New Additions:
- Added stamina bar that depletes dynamically based on how much the player is pulling down with the arm that is grabbing.
- Adjusted climbing speed and made the speed differ more between mouse and controller.


Playtesting questions:
1. Do the controls feel snappy and intuitive on both controller and keyboard/mouse? Is it too fast or slow?
2. Does the stamina bar feel intuitive? Do you know what replenishes your stamina?
3. Is it fun?

[Itch Build](https://cheva360.itch.io/sandwichclimber)

Playtesting notes:
- Feels intuitive on both controller and mouse, moreso on one than the other depending on the player. 
- The first intuition of most players who havent seen the level is to just purely climb upwards, not go to the side. Make the level design generally more vertical OR add an obstacle to force them a certain way. When the players fall, they should slide or be moved back to the beginning. 

### Activity 2
1. Multiplying two values between 0.0 and 1.0 will always result in a smaller value, which is why the resulting color is darker and less saturated. 0.2 * 0.8 = 0.16, which is less than both 0.2 and 0.8.
2. Multiplying two alpha values between 0.0 and 1.0 will also result in a smaller value, meaning that it will end up more transparent overall.
3. The UV values are stored in the data within the mesh of the object the material is applied to. 
4. Yes! I think it allows for a lot of unique effects and things that can be manipulated in the same ways vector 3's are in code.

## W7

### Activity 1
1. The data for the vertex color node came from the data stored in the mesh of the shiba. Each vertex has an associated color value.

2. The vertex colors are blended because the color is only stored at the point of the vertex, to fill in the color between vertices the shader interpolates the color values between vertices.

3. The shiba is less detailed because its color is only determined by the color values at the vertices, which are then blended together. Texture mapping allows for pixel-level color detail, something only having vertex color is incapable of.

4. There is a sploch on the left hind leg of the shiba that is a different color than the rest of the shiba. 

5. Another piece of vertex data that could possible be useful is the vertex positions. There could be issues with vertexes that are not in the correct position.

6. Theres an error because the light direction is in the oppsosite direction. Its lighted improperly until you multiply the light direction by -1, which flips the direction of the light and makes it light the shiba properly.

7. We set the blend mode to additive for the texture so that the alpha channel of the texture can be used to make parts of the texture transparent, and so that the colors of the fire can be added on top of the fires noise texture.


## W8
### Activity 1
Playtesting Notes:
- Leg glitch is back :sob:, needs to be patched.....
- stamina buff is good, just needs a bit more praticing for the player to get used to the difficulty of the game. The level is meant to be difficult, and its still plenty possible with a lot of leeway right now.

Changes from Milestone2
- Buff to stamina amount (200 -> 300)
- Player could get stuck at a certain point of the level, now fixed

[Itch Build](https://cheva360.itch.io/sandwichclimbermilestone3)


### Activity 2A
How are we utilizing the stencil buffer- specifically the Compare Function and Pass/Fail operations for both the Outline and Cel renderer features- in Step (2) to create the outline effect?
1. The stencil buffer is being used to create the outline effect by rendering the shiba to the stencil buffer and comparing it to a stencil value of 1. In the areas that the shiba is not rendered (the outline) the stencil value is equal to 0 which is where the outline is rendered.
2. The shiba is being drawn twice, due to the outline effect, specifically because of the stencil buffer.
3. We add them together because we want the final color to be contributed to both of them without being darkened. If we multiplied them together, the color would be darkened and saturated.
4. Changing the layer of the shiba enables the outline because the outline is only rendered on objects in the 'outline' layer.

## W9
### Activity 1
Red Dead Redemption 2

### Activity 2
In Read Dead 2 the camera has a lot of rendering systems affected by gameplay. 
- When the player activates dead eye, the camera lowers the post processing vibrance, adds a bit of vignette, and changes the color grading to a sepia tone. This affect is also done for certain cinematic death cutscenes when a player hits a good shot/kill.
- When the player enters a dialogue cutscene with an NPC, the depth of field changes to keep the NPC's in focus and blur the background. Its a very subtle effect that changes depending on the scene, but keeps the focus on the NPC's.

Generally both of these effects could be recreated by changing the post processing volume setting values dynamically through a script of the player state.

### Activity 3

ShaderGraph:

<img width="2469" height="1249" alt="image" src="https://github.com/user-attachments/assets/2925d549-5a35-4dce-abf3-ac90edb37af2" />


This shader graph is my attempt at making an ease out fade shader. When the player enters a trigger, the script sets the IsFade bool to true and the start amount to time.time. The shader then subtracts the start time from the current time to get the elapsed time, and is divided by the duration float as well as put into a smooth step to create the ease effect. 

The shader is activated when a player triggers a stamina bubble, which replenishes stamina and also activates the bool and sets the start time to create the visual effect.


## W10
### Activity 1
1. Little Changed from Milestone 3, mostly just changes in values and some bug fixes based on feedback from playtesting outside of class.
2. [Itch Build](https://cheva360.itch.io/sandwichclimbermilestone3)
3. How does the game currently feel? Does the rotation make sense?
4. Stamina bubbles can be easily cheesed by just staying by a bubble and letting it respawn, basically making for infinite height. Stamina bubbles should only respawn after falling and hitting a trigger. 

### Activity 2
For future projects, here is the general plan for the development process (based on both what I planned for this project as well as my game for GDIM 129):
1. Game Design Document:
	- Pretty Much everything should go here. Writing, ideas, mechanics, and most importantly breaking down these ideas into a plan of how they will be implemented into the game. It can be more reformed later on, but it was extremely useful for other projects with bigger scope for understanding what the vision for the game is, and what should be put onto the task sheet next, especially all the super small parts of a bigger system.
2. Google Sheets Task Sheet:
	- This one I would say is heavily dependent on the scope of the project, as well as whether you are a solo dev or in a team, but generally its really good for reminding yourself what to work on, and keeping yourself accountable. My brain was so scattered with so many projects this quarter that having something to come back to that I had already planned was super helpful for keeping myself on task on what is most important for me to work on at the moment.

### Activity 3
Today I worked on adjusting the map a bit after seeing playtesters navigating up more than they were navigating to the side. 