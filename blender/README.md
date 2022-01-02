# Blender basics workshop

> 💡 Content of this workshop is work in progress

## 📙 What you will learn

* Blender basics
	* Installation
	* User interface
	* Moving
* Low poly modeling
	* Is low poly some kind of sect ?
	* You said vertex ?
	* Let's practice !
* Animating models
	* 3d animation concepts
	* Your first animation
	* Introduction to rigging

## Blender basics

### What is Blender. Who are it's competitors ?

- Blender is a **free** and **open source software** suite for 3d creation. While it is not an industry standard just yet, it is [backed by large corporations](https://fund.blender.org/) and has a good community. It's the most well known open source software of it's kind.
- It's most often cited competitors I know of are [Autodesk's Maya and 3ds max](https://www.autodesk.com/) and [Cinema 4D](https://www.maxon.net/en/cinema-4d).
- Even though there are [some addons](https://github.com/EleotleCram/blender-cad-tools) to do that, blender should not be used as a [CAD](https://en.wikipedia.org/wiki/Computer-aided_design) tool. You should look into [FreeCAD](https://www.freecadweb.org/) (FOSS), [AutoCAD](https://www.autodesk.com/products/autocad/overview) (proprietary) or [SolidWorks](https://www.solidworks.com/) (proprietary).

### Installation

> ✅ Version required is **2.8** or superior. To check that do 
`blender --version` or `flatpak run org.blender.Blender --version`.

- Blender is open source so you should have it in the repositories of
your distribution of choice.
- Another way to get it is via flatpak on the 
[flathub](https://flathub.org/apps/details/org.blender.Blender) repository.
- If needed you can download the binary directly 
on [blender.org](https://www.blender.org/download/) and add it to your path.

### User interface

Let's begin by a few important facts on the user interface :

- Blender has a modular interface composed of multiple panels within a window.
They can be resized, reordered, added, deleted or detatched. (try hovering your mouse on the corner of a pannel and dragging it)
![Windows](https://i.postimg.cc/PqpWqxZ3/image.png)

- They are themself arranged within workspaces in the top bar.
![Workspaces bar](https://i.postimg.cc/sgWqZVpX/blender-workspaces.png)

- You should also checkout the settings window, you may find interesting
stuff inside.

> 💡 The ui is quite complete and complex, a good way to discover it is 
[blender docs](https://docs.blender.org/manual/en/latest/).

### Moving around in the viewport

There are three controls you should know of :

- Rotate with `middle click` or drag on the three axis on the top right corner of the viewport.

![Rotating blender](https://i.postimg.cc/JzZSv1YX/Kooha-12-09-2021-22-46-13.gif)

- Zoom with `mouse wheel` or drag the magnifying glass.

![Zooming blender](https://i.postimg.cc/25YgfPgK/Kooha-12-09-2021-22-47-30.gif)

- Pane with `shift` + `middle click` or drag the hand icon.

![Panning blender](https://i.postimg.cc/gkKhYvVL/Kooha-12-09-2021-22-47-58-online-video-cutter-com.gif)

More tips:

- The coordinates in blender are expressed in X, Y and Z (up) - 
It's not the case in all 3d software or graphic libraries!
- You should checkout the orthographic view. It permits you to eliminate all fov problems
and make precise modifications.

---

## Low poly modeling

### Is low poly some kind of sect ?

["Low poly"](https://en.wikipedia.org/wiki/Low_poly) is short for low polygon count.
It can be used for performances or aesthetics. 

Rendering engines will take longer to render models with high polygon count.
Thus, back in the early days of 3D games, low poly models were used as a way
to gain performances.

> 💡 In blender, polygon count (or poly count) can be seen in the bottom left
corner of the window for version < 2.9 and by checking statistics in the viewport
overlay in newer versions. 

Nowadays computers have a lot more performant cpus and gpus. Consequently,
low polygon models have lost their performance interest. It is noteworthy
that they  have had a comeback with their use in more artistic and abstract
modeling (see below).

Examples of low poly [renders](https://en.wikipedia.org/wiki/3D_rendering):

![Low poly street](https://www.designyourway.net/blog/wp-content/uploads/2019/03/sf-700x525.jpg)

![Low poly lighthouse](https://www.designyourway.net/blog/wp-content/uploads/2019/03/lighthouse-700x525.jpg)

![Low poly soldier](https://media.sketchfab.com/models/8dd47904297445cf9a628f71a3b5250a/thumbnails/174d70840b494e7b83afc82e7f864cd0/b185e2b7e1b940908d580978f4f5118d.jpeg)

![Low poly tanks](https://img1.cgtrader.com/items/2942279/93fb489591/large/set-of-low-poly-tanks-3d-model-max-obj-fbx.jpg)

> ❗ We won't go much into details about rendering since I feel it's a bit out
of the scope of this workshop. Anyway, feel free to add a camera and some lights
to your scene and a few settings later you will have a render.

You can also just search [low poly on sketchfab](https://sketchfab.com/search?q=low+poly&type=models)
(a 3d model sharing website).

### You said vertex ?

**Creating 3d objects is done using three basic atoms: _vertices_ (one _vertex_, two _vertices_), _edges_ and _faces_.**
Let's go through what they are.

- A vertex is a simple point in 3d space. Here we create 3 vertices A, B and C. They All have 3 coordinates
(x, y, z).

![Vertices](https://i.postimg.cc/bw4TvMvC/first.png)

- An edge links two vertices. We just link all our vertices with each other to form a triangle.

![Edges](https://i.postimg.cc/RCPwF8s7/second.png)

- A face links 3 or more edges.
> ❗ Be carefull, in blender you can create a face from any amout of edges, but it might
not end well ! [You can always triangulate you face after the fact anyway](https://docs.blender.org/manual/en/latest/modeling/meshes/editing/face/triangulate_faces.html).

![Face](https://i.postimg.cc/tJgPktTn/third.png)

### A bit about textures

A texture is just a normal image. The difference is we specify that one or
multiple faces of a 3d object will be mapped to some coordinates of this images.
It's just like unfolding a box!

![Texture unfolding animation](https://user-images.githubusercontent.com/33732772/147005866-28948274-638c-4b5f-a976-e4abbd7e6181.png)

### Let's Practice

> ✅ Make sure that the Z axis is upwards when modeling (check the tiny axis preview in the top right corner of the viewport)

> 💡 There are a lot of shortcuts in blender, learning them will make you a lot faster but everything can be done via the gui if that's your kink.

#### Step 1 - delete them all

> - Delete the cube and the light in the default scene

> 💡 the `C` or `B` and `X` keys could prove usefull ...

#### Step 2 - make leafs

> - Create a ico sphere of radius 1.1 with 1 subdivision
> - Move it to the coordinates (0, 0, 2)
> - Randomize it's mesh (you can play with it, but it should look like an imperfect ball in the end)

#### Step 3 - the trunk

> - Create a new cube of 0.5m sides
> - Extract it's top face to 1.5m to meet the leafs
> - Resize the face you just extracted to 80% of it's original size
> - Randomize the trunk

#### Step 4 - texturin' time

> - Download the sample texture [here](https://epitechfr-my.sharepoint.com/:i:/g/personal/arthur1_soulie_epitech_eu/EVYnZICB-Q1AgVTYd9vrL5IBwivVhSb5xuYj0qeD40nN2Q?e=BaU3l7)
> - Unwrap your two objects
> - Assign the trunck to the brown pixel and the leafs to the green pixel

#### Bonus round

> - Checkout blender render features
> - Checkout blender lighting features

## Animating models

### 3d animation concepts

[3d animation](https://en.wikipedia.org/wiki/Computer_animation) is the way you can move vertices
through time. To do so, you can specify several positions to a vertice called keyframes. The
keyframes values are then interpolated the way you want to obtain movment.

### Your first 3d animation

> ✅ Save your current blender file, you will need it later

#### Step 1 - it's cube all over again

> - Create a new blender file 
> - Remove the sun and the camera

#### Step 2 - frame it

> - Create a first keyframe
> - Move your cube
> - Create another keyframe
> - Play the animation

#### Step 3 - a matter of size

> - On the second keyframe, double the size of your cube

#### Step 4 - rotation

> - On the second keyframe, rotate the cube 180 degrees

#### Step 5 - linear is no good

> - Make sure the cube bounces to it's second size

### Intro to rigging

Up until now we have only been moving, rotating & scaling entire objects. But what
is you want to animate vertices ?
Well there are a few ways of doing just that.

#### Step 1 - the wind on the leaves

> - Use shape keys to interpolate between two randomization of the trees leaves

#### Step 2 - the wind on the entire tree

> - Create a NURBS curve
> - Link the curve with a curve modifier to your tree
> - Make it wiggle with shape keys

#### Step 3 - steve walk cycle

> - Download steve.blend and append (checkout the difference between appending and linking
external blender libraries) it to your project with the tree
> - Create an armature
> - Add bones
> - Modify weights
> - Make him walk !
