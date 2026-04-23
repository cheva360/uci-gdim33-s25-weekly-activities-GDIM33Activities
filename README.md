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

