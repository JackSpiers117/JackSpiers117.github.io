---
layout: post
title:  "Old Youtube Subscribe Button"
date:   2022-09-29 9:36pm +1000
categories: Design
---
# The Inspiration
I decided I wanted to build a subscription button for my net_art as I felt it matched old internet culture well with the anime.js' animation

<iframe width="560" height="315" src="https://www.youtube.com/embed/5mGuCdlCcNM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
---

# Design

At first this idea was a little complicated, despite following several tutorials on how to build a DVD Logo in p5js I couldn't quite find one that made sense to me, so I changed up my idea, I looked into the knowledge I already knew from capagrego's tutorials, if statements can be set so that the axis of an object bounces off in reverse, this was perfect for creating an image of an icon that could bounce off of walls and corners

![inspo](/etc/images/inspo.PNG)

Using the if statements to tell the image to move in reverse the second it touches a point of the axis creates this really interesting and similar movement that a dvd logo makes when it bounces off of the walls of the television screen, I also adjusted the screen size so that it bounced off a set tv instead of the whole canvas.

I now struggled with a new problem, it bounced but it didn't change colours just like the dvd logo would do on television sets. Fortunately, there were plenty of p5js library resources on how to make a functions that chooses things, and how to set RGB. With this I built a function that picks an RGB colour when the conditions are met.

![Result](/etc/images/Result.PNG)

Then I jumped into my if statements and simply included that when the if statement is met, it changes the colour using the "pickRGB" function

![pickRGBstatements](/etc/images/pickRGBstatements.PNG)

This was a better success than I could have hoped, it was very straightforward and ended up with this result to input into my p5 sketch.

<iframe width=576 height=366 src="https://editor.p5js.org/JackSpiers117/full/YEhuWQwrL"></iframe>
