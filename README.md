# git hub test trial

Hi there 👋

Welcome to SWE 585 - Fall 2022 repository.

The Authors of this repository:

atilla
How to deploy?
Clone this repo locally
Demo of the Game
https://youtu.be/SDEn6DaUr2c
Execution Details
In order to build this project I took a Udemy tutorial. Most of the assets are coming from the tutorial but I also used unity's default tree prefabs and also a free ghost asset that I downloaded from the unity asset store.

https://www.udemy.com/course/unityplatformer3d/
https://assetstore.unity.com/packages/3d/characters/little-ghost-free-229325
The tutorial and the game that I develop are not quite the same but the tutorial helped me understanding the concepts of unity better. The tutorial is not using rigidbody component for the main character "flameboy". Instead the instructor wrote his own logic to deal with the gravity. Also the tutorials camera controller is not following the flameboy from back. The ghost enemy is completely different and it's purely my code. The buzzboy enemy also have a feature that is unique. When It hits the flameboy it pushes him away.

I am creating ghost enemies programmatically and if they dont hit the flameboy they get repositioned to their original start point. This feature makes the game harder if the player takes a lot of time to complete the game. However, I observed this functionality in the profiler since the amount of prefabs that are being rendered increases as the time goes by and this has a negative effect on the cpu usage. I like this behavior and makes the game competitive. I believe I need to set a time limit so that there wouldn't be a lot of ghosts in the game.

The code is sadly not bug free. The buzzboy's hit and push effect causes problems when the flameboy is on the air (jumping). I enabled this functionality by adding a force to the flameboy at the direction of buzzboy and used velocity instead of vectors. It works perfectly while the flameboy is on the ground, however as I mentioned earlier if the flameboy hits the buzzboy while jumping, the flameboy goes to y direction with a rapid speed. An easy get around was to set a limit to the y direction of the flameboy and set its velocity to 0, causing the flameboy to fall back to the ground by the help of gravity.

Also when the flameboy falls to the sea the collision happens while the flameboy is inside of the sea and it looks ugly. I could have increased the bounding volumes of the sea to fix this issue.
