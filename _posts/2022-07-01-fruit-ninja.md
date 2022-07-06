---
layout: post
section-type: post
title: Featured Project Section - Fruit Ninja AR
category: tech
tags: [ 'Project' ]
---
**Fruit Ninja AR**

This is a game product of the classic fruit ninja game classically played about decade ago but this is now possible in augemented reality!

Link to this repository is [here](https://github.com/LuCkYProgram/Fruit-Ninja-AR)

**Description**

What is Augmented Reality? These days, AR is one of the better-known terms in the Extended Reality landscape, and one of the most accessible disruptive technologies around.

Using that knowledge in mind, I am going to dive deep into what I can use for augmented reality using python and its dependencies/packages of [mediapipe](https://mediapipe.dev/)!
Mediapipe is a python library that takes  a Framework for building machine learning pipelines for processing time-series data like video, audio, etc. 
This cross-platform Framework works in Desktop/Server, Android, iOS, and embedded devices like Raspberry Pi and Jetson Nano.

Using the mesh type of framwork in the optimization and initiazation of the program, it used to as a collection of trained data using real life data such as images or arrays.

In this repository, it is coded to use a image of many frames on a video to detect the positiosn of a person and indicating on the screen.

**Aha!** This is much better. `pose_landmarks` is a big list of landmark points on the image. As you can see, there are many landmarks, and each landmark has an x, y, z, and visibility.

To understand what these mean, take a look at the following diagram, provided by mediapipe:

![Pose landmark map](https://google.github.io/mediapipe/images/mobile/pose_tracking_full_body_landmarks.png)

As you can see, each "landmark" (special point) on the body is assigned a number. The nose is number 0, the right thumb is number 22, and so on. `results.pose_landmarks` contains these landmarks in order.

Strangely, `results.pose_landmarks` is an object, and to get the actual list, you have to write `results.pose_landmarks.landmark`. So if you want to get the location of the left eye (which is landmark number 2), you would write `results.pose_landmarks.landmark[2]`.
...