---
layout: post
title:  "Mock NFT Horse"
date:   2022-09-29 9:36pm +1000
categories: Design
---
# The Inspiration
The inspiration for this one was simple, it's based on the NFT's of today that are about as basic as they come, sold for high value with little variation between each image, as such I wanted to design a mock HorseNFT that actually served no purpose, kind of like NFT's, you simply click on it and it gives you a new variation to *cough* hopefully not screenshot *cough*

---

# Design

It was quite simple, I drew an image on illustrator based on a generic photograph of a man riding a horse as reference to the side to get the shaping right, then I changed the fill colour up to 8 times and saved them each as their own variants.

![HorseResult](/etc/images/HorseResult.PNG)

# Result  and Code

From here I placed each variant on an array and made an if statement, then I made a button with an onClick function, once I grabbed all the images and had them on the array I told the if statement that if the user clicks on the onClick function of the button, it must cycle to the next image in the array. Result and code below:

![NFTResult](/etc/images/NFTResult.PNG)

Javascript:

    img_array = ['/etc/HorseRider1.png','/etc/HorseRider2.png','/etc/HorseRider3.png','/etc/HorseRider4.png','/etc/HorseRider5.png','/etc/HorseRider6.png','/etc/HorseRiderDeluxe.png','/etc/HorseRiderPastel.png'];
i=0;
//building a button function that lets the user click and get a new image on the array
function myButton()
{
     i++;
    document.getElementById("myImg").src=img_array[i];
    //if statement declaring if the array hits the value of 1 then it 
    //goes back to the beginning of the first iteration
    if(i==img_array.length-1) {
   i=-1;
    // var audio = new Audio('25th_hour.wav');
    //     audio.play();
    //     audio.loop = true
    }
}
