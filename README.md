# VrTask

## VrGame 
## Name: Zuzanna Pawelczyk
## Student Id: 2506784

I worked on a VR Game with Sam and Harry, and we split the tasks so that Sam worked on finding an environment, any static meshes needed in general along with sounds for the game. Harry was to work on the UI, as well as he was the only one with a vr headset on hand so he served to test the game for us when not in class. My task was to work on a mechanic for the game, which also led me to having to figure out bugs with the game.

My idea for the mechanics was very simple I wanted to use the fact that the base VR template had a gun built in that upon clicking a button spews out projectiles. So I thought to make a target that the player has to shoot at from afar to gain points. I created a target blueprint with varying collision boxes so that depending on where the projectile ends up coliding with, it will assign the player a different amount of points. I ran into a minor issues where the target seemingly wasnt registering the projectile, it turned out that the projectile just had dubious collision settings so I altered it to trigger any collision box so that the target worked without any issues.

While trying to make this and another mechanic we ran into issues while testing that I had to work through. The first issue was that seemingly two different sets of players spawned in that were connected to the same vr headset, I managed to fix this by simply removing the camera in the stage that seemed to be causing this issue. Our next issue was that the player couldnt move in the space. This stumped me for a while, so we decided to test run the VR template to check if the moving works there or not, and it did. So in the editor I looked around to what was allowing the player to move there and I found the area where the testing area didnt allow the player to walk in. I clicked on that and saw that the intentional area where you cant move was a nav mesh modifier, which meant that if to not be able to walk somewhere you have to modify a nav mesh, that must mean that to walk somewhere you need a nav mesh in the first place. I added a nav mesh into our level and that was the fix, the player could walk around anywhere the nav mesh was and registered the ground as solid and walkable. 

