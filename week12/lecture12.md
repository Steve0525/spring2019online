---
title: Lecture 12
layout: lecture
visible_lec: true
visible_n: true
---

<!-- .slide: class="titleslide" -->

# Data Visualization
<div style="height: 6.0em;"></div>
## Jill P. Naiman
<<<<<<< HEAD
## Spring 2019 (online)
=======
## Spring 2019 (Online)
>>>>>>> 88327e0e4253d9514a3c283d68f06466ce7f18c2
## Lecture 12

---

## If you are on campus: April 22nd at NCSA, ~~9:30am~~ 9am

In-person class is having live demos from the Advanced Visualization Lab.  Feel free to join!

We will meet in 1005 on the ground floor.

The address is 1205 W Clark St, just north of the Siebel computer science building.

---

## Quick HW poll

Move due date to Sunday?

---

## Warm-Up Activity Part 1

 1. What is the visualization trying to show?
 1. What are its methods?
 1. What are the strengths / weaknesses?

https://xkcd.com/2135/

---

## Warm-Up Activity Part 2

 1. What is the visualization trying to show?
 1. What are its methods?
 1. What are the strengths / weaknesses?
 1. Would you know how to make something like this?

http://biologylabs.utah.edu/farmer/index_dinosaur.html

---

## Today

 * Scientific Visualization
<<<<<<< HEAD
 * (And some JS if we have time)
 
We'll also go through the pathway of GitHub -> uploading your Jupyter notebook again.

---

## Information Visualization

So far: Spatial encoding is chosen by the designer

<img src="images/circlesTree.png" width="500"/>

notes: so far, a lot of our placement of objects has been up to us

---

## Scientific Visualization

Sci Viz: Spatial encoding is provided in the data

<img src="images/orf2D.png" width="500"/>

notes: but with sci viz, we are usually dealing with spatial data - so we are told by the 
science where we should be placing things in 3D space

we did this sort of thing in 2D for data on maps, but this gives even more detail on 
where each data point should be placed
=======

---

## Information Visualization

So far: Spatial encoding is chosen by the designer

---

## Scientific Visualization

Sci Viz: Spatial encoding is provided in the data
>>>>>>> 88327e0e4253d9514a3c283d68f06466ce7f18c2

---

## Spatial Data
<<<<<<< HEAD

 1. Geometry
  * Volumetric Fields

<img src="images/smoke.gif" width="800"/>

note: there are different kinds of spatial datasets

Here is shown some volumetric data - i.e. you are given points of things in 3D space

shown here is a simulation in Houdini (a special effects software package) showing smoke rising

The left plot shows the simulation data points, the middle plot shows how they are interpolated to a surface and the right shows how they are "rendered" i.e. made into a movie using a smoke "shader" which dictates how light rays will travel through the object
=======

 1. Geometry
 1. Volumetric Fields
>>>>>>> 88327e0e4253d9514a3c283d68f06466ce7f18c2

---

## Spatial Data

 1. Geometry
   * Polygons
<<<<<<< HEAD

<img src="images/wheel.gif" width="800"/>

notes: another thing you will see a lot is 3-dimensional surfaces like the one shown here

Instead of specifying data at each point in the 3D volume, we are specifying the surface - i.e. an interconnected list of polygons that makes this shape

(we'll actually play with surfaces later in class and volumes either next week or the last week)
=======
   * Point Clouds

notes:
point clouds can be static, or they can have physics which make them a "particle system".

---

## Spatial Data

 2. Volumetric Fields
    * Scalar
    * Vector

notes:
Fields can be 2D or 3D. Images can be used as 2D data fields.
>>>>>>> 88327e0e4253d9514a3c283d68f06466ce7f18c2

---

## Spatial Data

<<<<<<< HEAD
 1. Geometry
   * Polygons
   * Point Clouds

<img src="images/cme.gif" width="800"/>

notes:

Sometimes you'll see data shown by points.  Before, we were showing data that "filled up" the space, but here point clouds are almost like infinitely small data points at specific locations in space

point clouds can be static, or they can have physics which make them a "particle system".

FYI this is a non-final render of some data from the "Solar Super Storms" movie that the AVL created

---

## Spatial Data

 2. Volumetric Fields

<img src="images/redDropShort.gif" width="600"/>

notes:
How do you represent something like this with data?

You need scalars to describe things like material.

You need vectors to describe things like motion (velocity). 

---

## Spatial Data

 2. Volumetric Fields
    * Scalar

<img src="images/grids.gif" width="600"/>

notes:
This sequence reveals the underlying 3D grids of several scalar fields including:

H1 density

H2 density

photogamma

temperature

metallicity

Basically, you can think of the centers of each cubes specifying where the data points actually are - more densely packed cubes means *higher resolution* data

---

## Spatial Data

 2. Volumetric Fields
    * Scalar

<img src="images/sapasmons.jpg" width="500"/>

notes:
Fields can be 2D or 3D. Images can be used as 2D data fields.

AVL used this image from the Magellan satellite to create a "displacement map" for this venusian volcano called "Sapas Mons".

2D fields can also be layered in formats common to GIS, or Hollywood formats like EXR.

---

## Spatial Data

 2. Volumetric Fields
    * Scalar
    * Vector

[Windy Weather Map](https://www.windy.com)

<img src="images/maria.png" width="600"/>

notes:
Windy is an interactive wind velocity map. It's always interesting to look at, but especially during hurricane season. I captured this image as Hurricane Maria flirted with the East coast in Sept 2017.

---

## Spatial Data

 2. Volumetric Fields
    * Scalar
    * Vector

Its even possible to do this in real time: [Earth map](https://earth.nullschool.net/)



---

## Spatial Data

 2. Volumetric Fields
    * Scalar
    * Vector

<img src="images/streamlines.gif" width="600"/>

notes:
In this visualization we're seeing 3D velocity streamlines.

We're ALSO seeing a scalar volume called "vorticity" which is directly derived from the velocity field by taking a mathematical operation called the "curl".

In this case we are plotting *both* scalar (volume glow) and vector (streaming lines) data in the same viz!

Also from solar super storms

---

## Spatial Data

 2. Volumetric Fields
    * Uniform or non-uniform
    * Rectangular or non-rectangular

<img src="images/gridTypes.gif" width="400"/>

notes:
Adaptive mesh refinement is an especially efficient 3D storage for datatypes that have small areas of high detail.

This is why dealing with scientific data can be a little tricky - it can be hard to make surfaces or volumes out of irregularly gridded data

---

## Spatial Data Types

 1. Statistical
    * Star species
    * Atom prevalence
 1. Observational
    * Telescope images
    * Microscope images
    * LIDAR
 1. Simulated by computer models
    * First principles physics
    * Astronomy, geology, biology

---

## Visualizing Point Data

 * Dots with scale

<img src="images/pointCloud.gif" width="600"/>

notes: some other, less used data types include things like dots with scale

---

## Visualizing Point Data

 * Dots with scale
 * Sprites

<img src="images/energy.gif" width="600"/>

notes:
All the moving dots in this video are represented by a gaussian splat image. You can see how they are adjusted to be different size and color (the important things are the purple ones)

FYI this is a little pre-final version of an upcoming movie called "Birth of Planet Earth"

---

## Visualizing Point Data

 * Dots with scale
 * Sprites

<img src="images/energyLetters.gif" width="600"/>

notes:
But gaussian blur isn't the only way to put a sprite on a point. This version used text instead. (purple q's instead of sprites)

---

## Visualizing Point Data

 * Dots with scale
 * Sprites
 * Meshing

<img src="images/canup.gif" width="600"/>

notes:
This is a test AVL worked on with an SPH "smooth particle hydrodynamics" dataset where we created a surface across points. The surface was generated at a density threshold - aka, it was an infinitely thin shell shrinkwrapped onto all particles that were above a certain density.

This is a way to turn particles into surfaces or polygons.

We'll play with surfaces later

---

## Visualizing Polygons

 * Vector lines with width, can be filled

<img src="images/platecarree.png" width="600"/>

notes:
We're already familiar with this data from MAPS week.

---

## Visualizing Polygons

 * Vector lines with width, can be filled
 * Direct rendering of architectural schematics

<img src="images/lsst.gif" width="600"/>

notes:
Sometimes you will be given a description of geometric objects that you need to construct.

---

## Visualizing Polygons

 * Vector lines with width, can be filled
 * Direct rendering of architectural schematics
 * Direct rendering of 3D scans (pre-meshed)

<img src="images/mammoth.gif" width="600"/>

notes:
Sometimes you will get something that was originally generated from a point cloud but has already been meshed. Domain experts sometimes have access to better meshing tools, particularly in the realm of 3D scanning.

---

## Visualizing Scalar Fields

 * Slice

<img src="images/mri.png" width="600"/>

notes:
You might remember from Week 5 when we played with this brain scan data - this is only a single image slice out of a 3D gridded dataset.

Even if you're not showing your final visualization as a slice, this is a good step for understanding and troubleshooting. As we've mentioned before, reducing dimensionality makes things clearer to the human brain.

---

## Visualizing Scalar Fields

 * Slice
 * Isosurface

<img src="images/isocontours.png" width="400"/>

notes:
You have probably seen this type of topographic map where lines indicate elevation. These lines are called isocontours. You can combine isocontours to get isosurfaces.

---

## Visualizing Scalar Fields

 * Slice
 * Isosurface

<img src="images/isosurfaces.png" width="700"/>

notes:
This is an isosurface of a tornado-forming storm cloud, and another of a supernova that the scientist called "the walnut".

Isosurfaces can make analysis easier.

---

=======
 2. Volumetric Fields
    * Uniform or non-uniform
    * Rectangular or non-rectangular

notes:
Adaptive mesh refinement is an especially efficient 3D storage for datatypes that have small areas of high detail.

---

## Spatial Data Types

 1. Statistical
 1. Observational
 1. Simulated from computer models

---

## Visualizing Point Data

 * Dots with scale
 * Sprites
 * Meshing

---

## Visualizing Polygons

 * Vector lines with width, can be filled
    * Think geographic data
 * Direct rendering of architectural schematics
 * Direct rendering of 3D scans (pre-meshed)

---

>>>>>>> 88327e0e4253d9514a3c283d68f06466ce7f18c2
## Visualizing Scalar Fields

 * Slice
 * Isosurface
 * 3D Volumetric Rendering

<<<<<<< HEAD
<img src="images/bock.gif" width="600"/>

notes:
But of course, you can always render the volume as a volume too. This is a volumetric tornado-forming storm cloud by Dave Bock who also works at the NCSA. 

While this looks similar to the volume rendering at the beginning of class its a better representation of reality - this includes a lot more physics, making it a scientific dataset.

---

## Visualizing Vector Fields

 * Arrow glyphs

<img src="images/arrows.gif" width="700"/>

notes:
vectors are often represented with arrows at specific points

I'm actually not sure what this is showing, but my guess is magnetic field lines, probably in some explosive astro event (like a super novae or something)

=======
>>>>>>> 88327e0e4253d9514a3c283d68f06466ce7f18c2
---

## Visualizing Vector Fields

 * Arrow glyphs
 * Streamlines / Streamtubes
<<<<<<< HEAD
    * Particle Advection!

<img src="images/tornado.gif" width="600"/>

notes:
But you can also show streamlines, which track vectors across the whole grid. Particle advection is releasing massless particles into a vector field, letting the vectors push them around, and tracing their progress.

This tornado visualization actually shows arrow on the ground AND streamlines in the air.

---

## yt

yt is an open-source, permissively-licensed python package for analyzing and visualizing volumetric data.

[yt-project.org](https://yt-project.org/)

There is a big yt community at the iSchool and NCSA!

---

## Final Project: Part 3

Due by class on April 18nd, submitted in a repository and a link that can be rendered in HTML.

You can approach this as:
 * Raw HTML
 * Idyll
 * Github pages
 * Embedded Jupyter notebooks
 * Others?

---

## Final Project: Part 3 (cont)

You will be writing an interactive data visualization article aimed at the public. Your article should feature:
  * A compelling title don't forget to specify that you are the author!
  * At least one central interactive visualization featuring your primary dataset. This can be similar to what you submitted in the last phase, but does not need to be a dashboard. Remember, this is for the public so it should be large and friendly.
  * At least two contextual visualizations - these can be other data visualizations you've done, or images from other places (remember to site your sources!!).
  * At least 3 paragraphs of connective information to help a novice understand what is happening in your datasets.
  * Citations of all the data sources used and information for the reader to be able to find those datasets themselves.

---

## Final Project: Part 3 (cont)

You should submit:

Code:
 * The GitHub (or other) URL where the code is stored or a link specifying what to enter in nbviewer/mybinder. 
 * You can receive extra credit for including more than the required minimum. This can include making more than one visualization interactive, incorporating more than 1 visualization you've done yourself, or incorporating more than your main dataset into the three visualizations.
 * Look to data visualization articles on fivethirtyeight.com, the New York Times website, or elsewhere for inspiration.

---

## Final Project: Part 3 (cont)

In class:

 * We'll allow everybody to give a short 2-3 minute explaination of their dataset and viz.  Come prepared to say something about what you've done!  

---

## Code today

1. More details about mybinder.org
1. yt and sci viz, output to other formats
1. JS if we have time
=======

---

## yt

yt is an open-source, permissively-licensed python package for analyzing and visualizing volumetric data.

There is a good portion of the yt group here at UCSC and NCSA!

<!--yt creator Dr. Matt Turk originated this course!-->

---

## Final Project: Part 3
>>>>>>> 88327e0e4253d9514a3c283d68f06466ce7f18c2
