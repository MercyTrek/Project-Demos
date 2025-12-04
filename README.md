# Table of Contents
- [Overview](#overview)
- [Software Implementation](#software-implementation)
- [Hardware Implementation](#hardware-implementation)
## Overview
THe aim of this project was to develop a scaled ARASE MEO satellite model to ultimately show that it obeys Kepler's laws of planetary motion. The ARASE satellite follows an elliptical with high eccentricity. The purpose of the satellite was to study the Van Allen Radiation Belt. This project was done as part of the coursework for the Lecture: ELEC 442 – Satellite Communications taught by Prof. Ridha Hamila in Spring 2022. The project partner was Husam Al Ardah. 
### Software Implementation
The first step in modeling the orbit on a small scale, a software was needed to get the actual coordinates of the satellite with respect to a reference point. The software used for this purpose was the “SSC 4D Orbit Viewer” by NASA. From the software, the cartesian coordinates (x,y and z) were extracted and then MATLAB code was written to find the semi-major and semi-minor axis as these are needed to define an ellipse. Figure shows the Plot of the ARASE Satellite Orbit including the orbit parameters. 
![alt text](https://github.com/MercyTrek/Project-Demos/blob/main/OrbitMatlab.png "MATLAB Plot of the ARASE Satellite Orbit showing the orbit parameters.")

### Hardware Implementation
To develop an accurate model of the orbit, the approach chosen was to model the orbit as a train track with the satellite being modelled by the train moving on the
track. Note that all the parameters were appropriately scaled down using the suitable formulae which has been omitted here for sake of brevity. Using the original train track as a guideline, a new set of train tracks were designed and 3D printed (with the help of a mechanical engineer). Furthermore, following Kepler's law, the speed of the satellite (train) should change depending on its location in the orbit (train track), hence an Arduino microcontroller was used to adjust the speed of the DC motor controlling the two wheels on the train through a gear mechanism. The train track was then segmented into 8 sections and a speed for each section was set. The beginning of each section was marked with an obstacle an infrared sensor mounted on the train was used to detect this obstacle which signalled the microcontroller to set the speed of the train for that appropriate section. Click [here](https://drive.google.com/file/d/17LtwRl4XQcVeRRSzUO4H58QVIJcOm6Cz/view?usp=sharing)
 here for the demo video.  

