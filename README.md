# Quadrotor Simulator and PD Controller

Requirements: MATLAB

This is an exercise to implement a Proportional Derivative (PD) height controller for a Quadrotor.

## About the code writers
The code of all files was written by the University of Pennsylvania. I only implemented the code in the contoller.m file, after the "FILL IN YOUR CODE HERE" comment, and before the "end" keyword.

## PD Controller
The dynamics of the altitude of a quadrotor can be modelled as follows:

*d<sup>2</sup>z/dt<sup>2</sup> = u/m - g*

where *u* is the input (motor thrusts) of the quadrotor, *g* the gravity, *m* the mass of the quadrotor, and *z* is the position in the vertical axis.

From this, a PD controller can be derived, where the error between the desired and actual accelerations in the z axis is exponentially reduced, as follows:

*u = m(z<sub>des</sub><sup>2</sup>/dt<sup>2</sup> + K<sub>p</sub>e + K<sub>v</sub>(de/dt) + g)*

where *e* is the error in position, and *de/dt* is the error in velocity

