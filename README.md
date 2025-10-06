<a id="readme-top"></a>

![Status](https://img.shields.io/badge/status-under--development-yellow)
![Made with Construct 3](https://img.shields.io/badge/built%20with-Construct%203-blue?logo=construct3)
![License](https://img.shields.io/badge/license-TBD-lightgrey)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen)
[![Play in Browser](https://img.shields.io/badge/Play--Now-Browser-green?logo=google-chrome&logoColor=white)](https://hielo777.github.io/3dThumbstickControls/)
![GitHub last commit](https://img.shields.io/github/last-commit/hielo777/3dThumbstickControls)

# 🕹️ 3d Thumbstick Controls in Construct 3

This project showcases how to create a simple and effective thumbstick controller for 3D objects in [Construct 3](https://www.construct.net/en).

With 4 events and some clever settings, the game can set the thumbstick controller, which can be used on any touchscreen device.

<div align="center">
  <img src="controlsDemo.gif">
</div>

A million thanks to the [Construct community](https://www.construct.net/en/forum) and to the kind people of [Scirra](https://www.construct.net/en).

***

 ## ⚙️ How it works:

<details>
<summary>&nbsp;&nbsp;&nbsp;&nbsp;Template Game Logic <small>(Click here for full explanation)</small></summary>

The entire system relies on the interaction of 2 different Construct objects:
- The sprite named **thumbstick01**
- The 8 instances of the sprite named **directionMarker**

The **thumbstick01** has the *"Drag and Drop"* behavior and can be moved on the screen by the player.

The 8 **directionMarker** sprites are set in a circle around **thumbstick01** at 45-degree inclination difference. 

Each **directionMarker** has 2 *Instance Variables:* vx and vy. These variables have 3 possible values: -1, 0, and 1. Each combination indicates the movement in the x and y direction that every **directionMarker** represents.

When the player moves **thumbstick01**, C3 determines which **directionMarker** is closest and uses the vx and vy variables to calculate the correct movement direction for the 3D object **Player3D**:

In the third event, C3 takes the *Instance Variable* vx, multiplies it by the speedPlayer variable, and assigns the result to **Player3D**’s *8Direction* Vector X.
The same process is repeated with vy, producing the value for **Player3D**’s *8Direction* Vector Y.

Together, these two values define the movement direction of the **Player3D** object.

<p align="right">(<a href="#readme-top">⬆  back to top  ⬆</a>)</p>
</details>

***

## 🔀 Changes:
<details>
<summary>&nbsp;&nbsp;&nbsp;&nbsp;Implemented Changes <small>(Click here for full explanation)</small></summary>

- [x] The `Basic Version` folder includes two builds that focus exclusively on thumbstick functionality, with slopes and other refinements removed. These streamlined versions are designed for easier integration into other games

- [x] Moved all the html files to the `html export files` folder for easier project navigation

- [x] Basic thumbstick functionality

- [x] Added tiled background to highlight 3D object movement

- [x] Improved the rotation of the 3D object reflecting the thumbstick movement

- [x] Added solid objects. This is to showcase the basics of a possible 3D-based game using the thumbstick

- [x] Added basic 3D slopes functionalities.
> The initial 3D slopes projects can be found at: https://github.com/hielo777/3DSlopes

- [x] Eliminated the older Player object from the screen to make it less intrusive

- [x] Re-created the exported game files

- [x] Adding basic camera support, allowing the player to change the distance of the camera to the Player3D object, and also to change the altitude of the camera

- [x] Adding a minimum distance and height for the camera controls to avoid weird angles and keep the game playable

- [x] Adding a maximum distance and height for the camera controls to avoid weird angles and keep the game playable. The maximums can be adjusted with the variables maxCameraDistance and maxCameraHeight.

- [x] Adding "diagonal camera controls" that allow for modifying the height and distance of the camera at the same time. The logic for these diagonal controls is similar the one used to control the movement of the Player3D object, using a combination of the instance variables to modify the Y and Z attributes of the 3DCamera.

<p align="right">(<a href="#readme-top">⬆  back to top  ⬆</a>)</p>

</details>

***

## 📋 To Do:
<details>
<summary>&nbsp;&nbsp;&nbsp;&nbsp;Roadmap and musings <small>(Click here for full explanation)</small></summary>

- [ ] Add second thumbstick functionality. Perhaps to control the camera to orbit the 3D object representing the main character.
>> This item is in progress. You can see the finished list above, and some camera control functionality has been added.

- [ ] Add comments to the .c3p document to clarify functionality

- [ ] Improve the slopes functionality to:
> Allow the player jump
> Allow the player go to multiple levels
> Better support for going up and down the slopes. Currently is quite basic and the player can get stuck in the wrong height after leaving a slope on the side

<p align="right">(<a href="#readme-top">⬆  back to top  ⬆</a>)</p>
</details>

<p align="left">(<a href="#readme-top">⬆  back to top  ⬆</a>)</p>