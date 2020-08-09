Hi! You've reached the folder that holds the files I've changed in SU2 v 7.0.5. When you build SU2 from source, you should find the files with the same names as the ones included in this folder, and replace them with the ones in this folder! 

Why? Well, building SU2 from source will not include any of the changes I made to the source code. The changes I made are relatively local, however, so just swapping the relevant files with mine shouldn't cause any problems.

I've included a config file. This is really just to show you that there are new functions that can be used. Specifically, the inputs SPHERICAL_COORDINATES, FIELD_STRENGTH, CENTER_OF_MASS, PLANET_MASS, and PLANET_RADIUS are new config inputs.

If you build SU2 from source and try to run a simulation with any of the previously mentioned config inputs, SU2 will throw an error and exit. 

The most important files are CEulerSolver.cpp and flow_sources.cpp. In lies these lies the actual code for computing central gravitational acceleration. I have tried to make the code as clear and self-explanatory as possible, and the Project Diary which contains my notes on the project thus far also contains an index of which methods have been changed in each file.


