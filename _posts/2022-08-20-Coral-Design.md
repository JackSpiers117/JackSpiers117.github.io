---
layout: post
title:  "Coral Design"
date:   2022-08-20 11:51:07 +1000
categories: Idea
---

# The Process
In my P5 Sketch there is an element where the fish swims from one row of corals to the next row of corals. 

![coralexample](/etc/images/coralexample.PNG)

This design was interesting as I couldn't simply build squares and triangles that can have their vertices changed into complex shapes, as such I had to go hunting through the p5js library and found that you can build shapes through the "beginShape()" function.

![beginshapeexample](/etc/images/beginshapeexample.PNG)

 That allows me to add as many vertices for building a shape as I'd like while still being able to close the vertices and fill it with color like a regular shape. So I used this function and begun building a coral shape. 

However I ran into a problem with the build, since I am not a human computer/calculator, I am unable to build a coral using x and y positions off of the top of my head, as such I looked towards solutions. 

The big solution I came to was using Adobe Illustrator, this illustrating application allows you to draw lines as vertices points on the same kind of xy plane that canvas work on. So I built the illustrator page to the specifications of the canvas and began drawing the coral on the parts of the page I wanted them on, here I hovered over the vertice points, grabbed their x and y values and inputed them into the "vertex(x,y)" in the "beginShape()" function.
 
 ![coralaxis](/etc/images/coralaxis.PNG)
 
 With all the vertices inputted I was met with success, coral shapes for my fish to navigate from a to b.