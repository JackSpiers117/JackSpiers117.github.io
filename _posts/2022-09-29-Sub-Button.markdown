---
layout: post
title:  "Old Youtube Subscribe Button"
date:   2022-09-29 9:36pm +1000
categories: Design
---
# The Inspiration
I decided I wanted to build one of those old YouTube subscription buttons from 2012 for my net_art as I felt it matched old internet culture well with the anime.js' animation, as old youtube outros include swaying motion of the subscribe button when clicked

---

# Design

I wanted to make my own Subscribe button but also needed to maintain authenticity, as such I hunted down the old 2012 Subscribe button of youtube and started there, I put it into Adobe Illustrator, opened up another Illustrator page with an empty canvas and begun.

![inspo](/etc/images/inspo.PNG)

# Result 

I started by adding a generic rectangle the shape of the subscribe button, an old button like this was perfect since it didn't have any annoying clever rounded edges effect, so all I needed to do was add it as a rectangle, then I added a stroke and shaped the colors to be close to how the old subscribe button was designed, then I worked on adding typography in the middle, I chose 'Roboto' font as that was the closest to the typography I could get. I then centered it and made the text read "Subscrib" with the 'e' left out as part of old internet culture was the use of incorrect grammar and spelling, you'd often hear mock phrases like "thnx 4 subscrib" and that became what was the end result.

![Result](/etc/images/Result.PNG)

# The Code

Reading off of Capegreco's tutorial on adding Anime.js, I was able to utilise this .js to place my button within my net_art and give it an animation like so:

   

    const subs = document.getElementById (`img_Holders`)
    subs.width = subs.parentNode.scrollWidth
    subs.height = subs.width * 9 / 16
    subs.style.height = `${subs.height}px`
    subs.style.cursor = `url("/Cursor.png"), auto`

    //making the subbutton
    const subbutton = document.getElementById (`subscribeButton`)
    subbutton.style.width  = `200px`
    subbutton.style.height = `65px`
    subbutton.style.position = 'absolute'
    const trans_x = `translateX(${subs.width /2 - 800}px)`
    const trans_y = `translateY(${subs.height/2 - -100}px)`
    subbutton.style.transform = `${trans_x} ${trans_y}`

    subs.append (subbutton)

    const subbutton_mover = anime ({

            // targetting the sub button
            targets: subbutton,
            //making it go zoom like a sub button on those youtube outros
            duration: 2500,
            // rotating the sub button all the way around and landing straight
            rotate: `360deg`,
            // to make it scale 1.5x it's size
            scale: 1.5,
            //we want the thing to go back dont we? lets make this bad boy
            //alternate back to it's original position.
            direction: `alternate`,
            //making sure the subscribe button doesn't just play on web page open
            autoplay: false,
            // loop: false,
            synth: 34
        })
        
        subbutton.onclick = () => subbutton_mover.play()
