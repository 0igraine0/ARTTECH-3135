---
layout:     assignment
categories: assignment
title:      Assignment 4
subtitle:   Intro to computer vision ...
author:     bakercp
date:       2016-09-28 00:00:00
due:        2016-10-05
---

1. Read the following.  This is an introduction to artists using computer vision in their work.
  - [http://www.flong.com/texts/essays/essay_cvad/](http://www.flong.com/texts/essays/essay_cvad/)

2. Coding!
  - Building from the [Background Subtraction Example](https://github.com/SAIC-ATS/ARTTECH-3135/tree/master/Week_04/00_BackgroundSubtraction), use the resulting mask of the "foreground" to only allow the color image of the foreground through.
      - Tips:
          - Make sure that your output pixel array has enough planes (i.e. your background mask will be a 1-plane grayscale image, but your output image will need to be RGB or RGBA - i.e. 3 or 4 planes).  
          - Remember that for each pixel you'll be checking the corresponding "foreground" mask pixel to decide which of the raw camera pixels you want to show in your output image (think ... if foreground pixel, then use the camera pixel ... otherwise set it to black).
  - Bonus:
      - Instead of setting the background to black, set it to a video (or image) of your choice.  For reference, Apple's Photo Booth has filters like this that allow you to set the background to the video or scene of your choice.
      - Tips:  
          - There are lots of ways to achieve this effect ...
              1. Instead of setting each "background" pixel to black, set it to the corresponding pixel color from your background video (make sure the foreground and background videos are the same size!!).
              2. Instead of setting each "background" pixel to black, set it to transparent (`ofColor(0, 0, 0, 0)`).  Then just play the background video in the underneath the foreground pixels.