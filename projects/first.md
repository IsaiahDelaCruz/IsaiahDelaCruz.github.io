---
layout: project
type: project
image: img/micromouse/micromouse-square.jpg
title: "Bank Database"
date: 2025
published: true
labels:
  - Database
  - C
  - C++
summary: "This Bank Database was a project from ICS 2__. It's intended to recreate the way a Bank Database works with the programming languages C and C++"
---

The goal of the project was to mimic a real world work assignment by trying to create a bank database piece by piece with vague instructions each time. With the assignment being given with vague instructions and to many students there were many ways for the project to be completed but with efficiency in mind as well.

The bank database itself works mostly similar to how you'd think a bank database would work for your average bank, just on the lower scale with some security concerns being ommitted. When running the program you're greeted with a user interface and directions on how to use the program. The database saves the clients information and records if they decide to choose the 'add record' button and keeps the information stored after an instance of the program is exited. The program offers many more options to work with if its the users desire.


<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

Micromouse is an event where small robot “mice” solve a 16 x 16 maze.  Events are held worldwide.  The maze is made up of a 16 by 16 gird of cells, each 180 mm square with walls 50 mm high.  The mice are completely autonomous robots that must find their way from a predetermined starting position to the central area of the maze unaided.  The mouse will need to keep track of where it is, discover walls as it explores, map out the maze and detect when it has reached the center.  having reached the center, the mouse will typically perform additional searches of the maze until it has found the most optimal route from the start to the center.  Once the most optimal route has been determined, the mouse will run that route in the shortest possible time.

For this project, I was the lead programmer who was responsible for programming the various capabilities of the mouse.  I started by programming the basics, such as sensor polling and motor actuation using interrupts.  From there, I then programmed the basic PD controls for the motors of the mouse.  The PD control the drive so that the mouse would stay centered while traversing the maze and keep the mouse driving straight.  I also programmed basic algorithms used to solve the maze such as a right wall hugger and a left wall hugger algorithm.  From there I worked on a flood-fill algorithm to help the mouse track where it is in the maze, and to map the route it takes.  We finished with the fastest mouse who finished the maze within our college.

Here is some code that illustrates how we read values from the line sensors:

```cpp
byte ADCRead(byte ch)
{
    word value;
    ADC1SC1 = ch;
    while (ADC1SC1_COCO != 1)
    {   // wait until ADC conversion is completed   
    }
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```

You can learn more at the [UH Micromouse News Announcement](https://manoa.hawaii.edu/news/article.php?aId=2857).
