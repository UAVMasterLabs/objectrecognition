#! /bin/bash

/*
The camera must be set up for proper use with the object recognition algorithm.  Because it is a color-based algorithm, the automatic color and exposure correction performed by the LogiTech camera must be disabled and the colors made more vibrant.  The v4l2 tool below allows us to change the properties of the camera.

*/

v4l2-ctl -l
//v4l2-ctl -c //then do each of the following
v4l2-ctl -c white_balance_temperature_auto=0
v4l2-ctl -c exposure_auto_priority=0
v4l2-ctl -c saturation=250
v4l2-ctl -c exposure_auto=3
v4l2-ctl -c contrast=200
