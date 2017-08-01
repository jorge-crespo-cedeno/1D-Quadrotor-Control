# Quadrotor Simulator and PD Controller

Requirements: MATLAB

This is an exercise to implement a Proportional Derivative (PD) height controller for a Quadrotor.

[//]: # (Image References)

[image1]: ./images/fig1.png

## About the code writers
With the exception of the code in the controller.m file, the code in all of the files was written by the University of Pennsylvania. I only implemented the code in the contoller.m file, after the "FILL IN YOUR CODE HERE" comment, and before the "end" keyword.

## PD Controller
The dynamics of the altitude of a quadrotor can be modelled as follows:

d<sup>2</sup>*z*/d*t*<sup>2</sup> = *u*/*m* - *g*

where *u* is the input (motor thrusts) of the quadrotor, *g* the gravity, *m* the mass of the quadrotor, and *z* is the position in the vertical axis.

![alt text][image1]

From this, a PD controller can be derived, where the error between the desired and actual accelerations in the z axis is exponentially reduced, as follows:

*u* = *m*(d<sup>2</sup>*z<sub>des</sub>*/d*t*<sup>2</sup> + *K<sub>p</sub>e* + *K<sub>v</sub>*(d*e*/d*t*) + *g*)

where *e* is the error in position, and d*e*/d*t* is the error in velocity.

