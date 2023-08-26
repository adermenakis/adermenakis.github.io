---
layout: page
title: Ulallama Project Zombie
permalink: /ulallamaprojectzombie/
description: "3D Computer game build on XNA 3.1 in C# with full source code available"
---

Team Members
* Alexandros Dermenakis
* Chris Lamothe
* Albert Trinh
* Timur Utepov

## Game Summary
People have begun turning into Zombies!!! The player's only refuge is drive to the top of “Ullalama Mountains.” The purpose of the game is to survive the Zombie hordes until the car has reached the top of the mountains. The gamer must beware Zombie attacks and obstacles along the way. The game represents a mix of two different game modes: Time trial and Wreck mode. In Time trial games, the player's goal is to collect as many points as possible by killing zombies and by having a good finish time on a lap track. In the Wreck mode games there exists a straight line, where there are multiple objects placed throughout that straight line and at the finish line there is a pile of random objects that explode or broken. The goal of our game is to do damage to all existing piled objects by the time the player reaches the finish line (pile of exploding objects), to get to the finish at the given time limit, and stay alive after zombies’ numerous attacks. The game's setting is the Ullalama Mountains. . It is a single player game where the only enemies are time and zombies. There are no opponent cars racing along with the gamer. However, in order to reach the finish, all piles of objects, and all control points should be passed. These conditions make the game challenging and intriguing.

## Overview
This game has elements that resemble to other games such as Burnout revenge, Resident Evil 5, and Road Rash 3D. The story is about good friends on the car trying to escape the zombie infestation by going to the Ullalama Mountains. The Ullalama Mountains is a fictional world that has been created for the purpose of this game. The area where these mountains appear is similar to Phoenix in Arizona and the Nevada desert. There is a lot of sand, barely building and the big Ullalama Mountains. The safest and quickest way to reach their destination is to use a vehicle and ram through the hordes of zombies. Amongst those zombies, there exist some of them mutated into stronger and quicker creatures. They will cause more troubles for our protagonists. There are in total 2 different tracks. In order to succeed the mission, all power-ups and checkpoints must be passed in a sequence. To help with that the green arrow above the car always points to the next required control point. Passing through the checkpoint adds 15 seconds to the player.  We used a state diagrams to give an overview of how will our game will be presented and there is a simple sketch and description of each state. The controls for the Xbox360 and the mechanical analysis of the game are covered and explained. Also, we have included the schedule and planning of the project for the rest of the time remaining.

## Implementation
All the code was done in C# using XNA 3.1. The physics and collision detection system were made using [JigLibX](http://jiglibx.codeplex.com/){:target="_blank"}. The software artifact of this project (Saying software artifact since it was accompanied by a detailed Game Design Document) was implemented within a 1.5 week timeframe. The purpose of the project was to fulfill the requirements for "COMP 376 - Introduction to game development" being taugh at [Concordia University](http://www.concordia.ca/){:target="_blank"}. The course coordinator/teacher for the course in Winter 2011 I took it was [Dr. S. P. Mudur](http://users.encs.concordia.ca/~mudur/){:target="_blank"}.

Most of the models that have been used in the game were downloaded from [Turbosquid.com](http://www.turbosquid.com/){:target="_blank"}. That website is a pretty good database of free and paid 3D models available in various formats.

The 3D Objects I can take credit for are :

* The Green arrow shown on top of the car
* The Bullseye
* The 2 Tracks of the game
* The Menu buttons
* Which were all constructed using the student version of the Autodesk 3ds max 2011.

## What Can I do with this?
You can download the source code of the project (which is something I am not really proud of) and use it as a base for your game and as example code that uses JigLibX. As mentioned above the code is all C#. The VS2008 project available for download contains also the configurations for Xbox360. We managed to run it on the Xbox but the performance was poor. It seems that JigLibX is not well optimized when it comes to collision detection and the physical body simulation, leading to very high CPU usage.

## Screenshots
![](/assets/data/ulallamaprojectzombie/ulallama_main_screen.jpg) | ![](/assets/data/ulallamaprojectzombie/ulallama_car_selection_screen.jpg) | ![](/assets/data/ulallamaprojectzombie/ulallama_track_selection_screen.jpg)
![](/assets/data/ulallamaprojectzombie/ulallama_track1_screen1.jpg) | ![](/assets/data/ulallamaprojectzombie/ulallama_track2_screen1.jpg) | ![](/assets/data/ulallamaprojectzombie/ulallama_track2_screen2.jpg)

## Binaries
[Windows with Installer](/assets/data/ulallamaprojectzombie/ZombieGame.zip)

## Source Code
[VS2008 source code](/assets/data/ulallamaprojectzombie/ZombieGameSrc.zip)
