# 3D-Laser-Scanner-Kaptura-Similation

## Introduction
The working of Kaptura 3D Laser Scanner is such that an object is fed into it or kept in the scan space, where the Kaptura 3D Laser Scanner measures the object in length, width and height and determines the volume from this. The weight is also recorded. The IMS 360 generates a 3D model of the object from the acquired data and places an imaginary “bounding box” around it to determine the dimensions. In addition, high-resolution 360° photos of your articles are created in the same process.

To facilitate the same ambience in blender, first the dimensions with respect to the Kaptura scanner and the object were noted such as distance of the camera from the center of the scan space, angle of the camera pointing the object, width and intensity of the laser hitting the object etc.

## Approach
* Image with the pixel coordinates, where r from bgr is more than 240
* The object is rotating 5 degrees after ever scan
* The object is made up of thousands of vertices; comprising of x, y and z coordinates, these are further replicated as pointclouds for the object
* JSON file is created when the object has rotated 360 degrees, with x, y, z localising information of the pointclouds

## Using OpenCV
OpenCV (Open Source Computer Vision Collection) is a cross-platform library of programming functions for a broad range of applications, including deep neural networks, augmented reality, and facial recognition. To enhance your lightmaps, we shall make use of the two latter.

There are many other programming languages that are available for it, but because we will be interacting with it via Blender, Python will be used. Of course, you won't need to write any code; all you need to do is install it to use the following lightmapping features:
* Filtering (Mainly blurring, including Box, Median, Bilateral and Gaussian) (Mainly blurring, including Box, Median, Bilateral and Gaussian)
* picture manupulation

## Implement OpenCV in Blender 2.90
* Start the terminal on Linux as an administrator
* Change the directory to blender python binary: **cd '/home/Documents/.../blender-2.90.0-linux64/2.90/python/bin'**
* It is necessary to first ensure if pip is installed: **./python3.7m -m ensurepip**
* Upgrade the pip: **./python3.7m -mpipinstall --upgrade pip**
* Finally its ready to install opencv in blender: **./python3.7m pip install opencv-python**

## Command Line Interface
Open the terminal and run: 
