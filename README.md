# Jingxuan-Xu-Major-Project-Individual-Task
Perlin noise and randomness - Utilise Perlin noise AND random values or random seed to drive animation.
![An image of Lego Package Artwork](<readmeImages/Lego Package Artwork.jpg>)
[Functioning prototype - *Lego Package Artwork*]

I chose Perlin noise and randomness to drive my code for animation.

I took the original group code's wall grid and used the Perlin noise function `noise()` to calculate the offset of each rectangular grid to create a shaking animation. In addition, I drew the grids and cells on the base of the group code, and by setting random values to take advantage of setting the grid's moving path, I gave the overall screen a wobbly animation effect. My animation was different from the rest of the group members in that I used a vibration effect to make the elements move regularly within a defined range. The other members of the group used music or interactive techniques to make the elements move, thus creating different animation effects.

My personal inspiration for the code animation came mainly from Lego blocks, referenced below:
![Orderly LEGO Grid with Yellow and Dark Blue Bricks](<readmeImages/Orderly LEGO Grid with Yellow and Dark Blue Bricks.jpg>)

[*Orderly LEGO Grid with Yellow and Dark Blue Bricks*](https://stablediffusionweb.com/zh-cn/image/7891719-orderly-lego-grid-with-yellow-and-dark-blue-bricks)


![Christmas LEGO Grid Game](<readmeImages/Christmas LEGO Grid Game.jpg>)

[*Christmas LEGO Grid Game*](https://www.stirthewonder.com/christmas-lego-grid-game-for-preschoolers/)

In code, I created code that uses Perlin noise and random values to generate animated patterns. The core of the code is two classes: `Pattern` and `MyRectangle`.

The purpose of the `Pattern` class is to generate vertical and horizontal patterns consisting of small rectangles. The constructor defines the length of the sides of each rectangle and colors. The `drawVerticalPattern` and `drawHorizontalPattern` generate vertically and horizontally aligned rectangles, respectively. During the creation of each rectangle, I choose random colors  to make each part of the pattern look with some randomness.

Next, the `MyRectangle` class is responsible for the drawing and animation of the individual rectangles. The constructor sets random x and y offsets (`xOff` and `yOff`) for each rectangle, which will be used to generate the perlin noise effect. In the `display`, I use the Perlin noise function `noise()` to calculate the offset position of each rectangle in order to add some slight movement at each rendering so that the pattern appears to be swaying slightly. By increasing the values of the offsets `xOff` and `yOff`, the rectangles animate continuously and smoothly.

In the `setup()` function, I set the dimensions of the canvas, initialize the color, size of the rectangle, and x/y position of the pattern, and generate the rectangular pattern by calling the `drawVerticalPattern` and `drawHorizontalPattern` methods.

The `draw()` function is used to loop through the entire canvas. In `draw()`, I draw the rectangles, calling each rectangle's `display` to keep them slightly animated, driven by Perlin noise. In this way, the entire pattern takes on a sense of organic, slight movement across the canvas, bringing origin group coding to creative animation artwork.