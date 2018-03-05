# CarND-Path-Planning-Project
Self-Driving Car Engineer Nanodegree Program
   
### Simulator.
You can download the Term3 Simulator which contains the Path Planning Project from the [releases tab (https://github.com/udacity/self-driving-car-sim/releases).

### Goals
In this project your goal is to safely navigate around a virtual highway with other traffic that is driving +-10 MPH of the 50 MPH speed limit. You will be provided the car's localization and sensor fusion data, there is also a sparse map list of waypoints around the highway. The car should try to go as close as possible to the 50 MPH speed limit, which means passing slower traffic when possible, note that other cars will try to change lanes too. The car should avoid hitting other cars at all cost as well as driving inside of the marked road lanes at all times, unless going from one lane to another. The car should be able to make one complete loop around the 6946m highway. Since the car is trying to go 50 MPH, it should take a little over 5 minutes to complete 1 loop. Also the car should not experience total acceleration over 10 m/s^2 and jerk that is greater than 10 m/s^3.

## Project Rubric

### Complilation

The code compiles following the instructions

### Valid Trajectories

The car is able to drive at least 4.32 miles without incident: The car is able to drive at least 4.32 miles between 5 and 6 minutes. It depends on traffic. 

The car drives according to the speed limit: The car is a good driver and never exceed he speed limit because we code that the desired speed is 49.5 Mph and using the approach from the Q&A of the project is impossible to exceed the speed limit setting the desired speed below the speed limit.

Max Acceleration and Jerk are not Exceeded: I used the Q&A approach again and I don´t get warnings about acceleration and Jerk.

Car does not have collisions: I think that I took a very conservative approach to pass cars. It´s based in the Q&A solution and in a finite state machine. You can see the states in lines 23-27 and the behaviour between lines 370 and 506.

The car stays in its lane, except for the time between changing lanes: The finite state machine tries to mantain the lane until one vehicle is in front of us and the aren´t vehicles near our vehicle in the contiguous lanes.

The car is able to change lanes: The car is able to change lanes to pass cars. If we are in the central lane we decide to use the faster lane (if it´s possible) to pass the car.

### Reflection

There is a reflection on how to generate paths: I generate the paths using the Q&A of the project and using the results of the FSM that I´ve designed. This approach is based in generating the trajectory using a spline.


