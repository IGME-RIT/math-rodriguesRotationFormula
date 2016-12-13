# Rodrigues' Rotation Formula

This tutorial derives Rodrigues' Rotation Formula.

Rodrigues' Rotation Formula is a matrix formula for a rotation in 3D space centered at the origin about an arbitrary axis of rotation and arbitrary angle.

Given an arbitrary unit vector *k* and angle &theta;, Rodrigues' Rotation formula gives us that the matrix for the rotation about *k* by &theta; radians is

R = I<sub>3</sub> + sin(&theta;)\[k\]<sub>&times;</sub> + (1-cos(&theta;))\[k\]<sub>&times;</sub><sup>2</sup>,

where I<sub>3</sub> is the 3D identity matrix and \[k\]<sub>&times;</sub> is the [skew-symmetric cross product matrix](<https://en.wikipedia.org/wiki/Cross_product#Conversion_to_matrix_multiplication>).

# Setup

You will need to have CMake installed on your computer, and properly added to your path. In order to setup, run the following in a shell, then open the project in your preferred editor. Windows setup has been configured for use with Visual Studio.

Windows:
```
cd path/to/folder
setup.cmd
```
Linux:
```
cd path/to/folder
./setup
```
