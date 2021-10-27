---
layout: post
title: "How to model a simple geometry in Gmsh"
categories: Gmsh
---

Meshing is the most important part of the finite element analysis. We use Gmsh as a tool for  mesh generation. Gmsh is a open- source 3D finite element mesh generator with a built-in CAD engine and post-processor. It is very user friendly and has a very good visualisation capabilities. 

In this post I will explain simple steps which you can adopt to model and mesh a simple geometry in Gmsh. 

Steps:

* Create the layout of the geometry with proper dimensioning and coordinates. In this I will be considering the following geometry.

* Create points as per your geometry. For this go to Modules --- Geometry --- Elementary entities --- Add --- Point. You will see a dialogue box opened, just enter the coordinates of each point and click on add.
* After creating all point next step is to join all those point using line to form a complete geometry. For this Go to Modules --- Geometry --- Elementary entities --- Add --- Line. Follow the instructions shown on the screen, i.e you have to select the start and end point of the line. 
* Next step is to create a Plane surface.  For this Go to Modules --- Geometry --- Elementary entities --- Add --- Plane Surface. Then select the surface boundary and press 'e' to end selection. 
* For 2D geometries it is very important to define Physical group for the created surface. For this Go to Modules --- Geometry --- Physical groups --- Add --- Surface --- Give a proper name tag -- select the surface  and press 'e' to add. 
* Next step is for meshing. You can simply go to  Modules --- Mesh --- 1D --- 2D. 
* Last and final step is to save the mesh. 

The file generated here will be saved in .msh format, which you can further convert into xdmf with the help of "Meshio" and you are good to import this mesh file in FEniCS. 

