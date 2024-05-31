# Tut-09_GroupB_yhan0830_Functioning-prototype
Tut 09_GroupB_yhan0830
## Instructions on how to interact with the work

Clicking anywhere in the pattern will produce an explosion effect in that area, which will slowly return to its original state after the explosion.

## Details of your individual approach to animating the group code

1. Which did you choose to drive your individual code: audio, interaction, Perlin noise or time.

   A: I used interaction to complete my code, allowing it to interact with the mouse

2. Which properties of the image will be animated and how; highlighting how it is unique from other group members (i.e. one changes colours, the other component sizes, another reveals only some components at a time, etc.). You will need to work with your group members to make sure your work is sufficiently different from each other.

   A: Use the position and rotation angle of the pattern for animation

3. References to inspiration for animating your individual code; these can be images (still or gifs). How did they influence your submission?

   A: The inspiration comes from explosions, where items in a certain area will be blown away during the explosion. This simulates the effect of items being blown away

4. A short technical explanation of how your individual code works to animate the image and any appropriate references.

   1. Firstly, when the user clicks, save the clicked location (mouseX, mouseY) and set the explosion flag "explosion" to true to indicate that an explosion has occurred. At the same time, save the current time when the explosion occurred.
   2. Secondly, when rendering sub elements, determine whether there is currently an explosion and calculate whether they are within the explosion range. If they are within the explosion range, the sub element will be blown to a certain location and slowly return to its original position. The explosion of an item to a certain location is calculated by randomly selecting values from (50100) and using the cos and sin parameters as well as the explosion angle.
   3. When exploded, restrict sub elements from flying out of the Canvas boundary.
   4. The atan2() function was used to calculate the angle at which an object was blown off, which is a function used to calculate the angle from point (0,0) to point (x, y). The value returned by this function is in radians, which can be used to determine the azimuth of a point relative to the origin.