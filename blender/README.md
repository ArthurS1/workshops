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

## Installation

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

- Blender has a modular interface composed of multiple windows. They can be resized, reordered, added and deleted.
![Windows](https://i.postimg.cc/PqpWqxZ3/image.png)

- They are themself arranged within workspaces in the top bar.
![Workspaces bar](https://i.postimg.cc/sgWqZVpX/blender-workspaces.png)

- You should also checkout the pannel settings,
you might find interesting stuff inside 😉.

> 💡 The ui is quite complete and complex, a good way to discover it is 
[blender docs](https://docs.blender.org/manual/en/latest/).

### Moving around in the viewport

There are three controls you should know of :

- Rotate `middle click` or drag on the three axis on the top right corner of the viewport.

![Rotating blender](https://i.postimg.cc/JzZSv1YX/Kooha-12-09-2021-22-46-13.gif)

- Zoom `mouse wheel` or drag the magnifying glass.

![Zooming blender](https://i.postimg.cc/25YgfPgK/Kooha-12-09-2021-22-47-30.gif)

- Pane `shift` + `middle click` or drag the hand icon.

![Panning blender](https://i.postimg.cc/gkffgwsd/Kooha-12-09-2021-22-47-58.gif)

More tips:

- The coordinates in blender are expressed in X, Y and Z (up) - 
It's not the case in all software !
- You should checkout orthographic and normal view, can be usefull sometimes.

---

## Low poly modeling

### Is low poly some kind of sect ?

["Low poly"](https://fr.wikipedia.org/wiki/Low_poly) is short for low polygon count. It can be described from an aesthetic point or performance point of view :

- In video games, game engines will take longer to render models with high polygon count. Thus, back in the early days of 3D games, low poly models were used as a way to gain performances.
- Nowadays computers have munch beeffier cpus and even gpu. Consequently, low polygon models have lost their performance upperhand but have had a comeback with their use in more artistic and abstract games.

Example of low poly [renders](https://en.wikipedia.org/wiki/3D_rendering):

![Low poly street](https://www.designyourway.net/blog/wp-content/uploads/2019/03/sf-700x525.jpg)

![Low poly lighthouse](https://www.designyourway.net/blog/wp-content/uploads/2019/03/lighthouse-700x525.jpg)

![Low poly soldier](https://media.sketchfab.com/models/8dd47904297445cf9a628f71a3b5250a/thumbnails/174d70840b494e7b83afc82e7f864cd0/b185e2b7e1b940908d580978f4f5118d.jpeg)

![Low poly tanks](https://img1.cgtrader.com/items/2942279/93fb489591/large/set-of-low-poly-tanks-3d-model-max-obj-fbx.jpg)

You can also just search [low poly on sketchfab](https://sketchfab.com/search?q=low+poly&type=models) (a 3d model sharing website).

### You said vertex ?

3d modeling is based on atoms: vertices (one **vertex**, two **vertices**), edges and faces.

- A vertex is a simple point in 3d space. Here we create 3 vertices A, B and C. They All have 3 coordinates since we are in 3d space (x, y, z).

![Vertices](https://i.postimg.cc/bw4TvMvC/first.png)

- An edge links two vertices. We just link all our vertices with each other to form a triangle.

![Edges](https://i.postimg.cc/RCPwF8s7/second.png)

- A face links 3 or more edges.
> ❗ Be carefull, in blender you can create a face from any amout of edges, but it might not end well ! [You can always triangulate you face after the fact anyway](https://docs.blender.org/manual/en/latest/modeling/meshes/editing/face/triangulate_faces.html).

![Face](https://i.postimg.cc/tJgPktTn/third.png)

### Let's Practice

#### Step 1 - delete them all

> - Delete the cube and the sun in the default scene

#### Step 2 - make leafs

> - Create a ico sphere of radius 1.1 with 1 subdivision
> - Move it to the coordinates (0, 0, 2)
> - Randomize it's mesh

#### Step 3 - the trunk

> - Create a new cube of 0.5m sides
> - Extract it's top face to 1.5m to meet the leafs
> - Resize the face you just extracted to 80% of it's original size
> - Randomize the trunk 

#### Step 4 - texturin' time

> - Download the sample texture [here](https://epitechfr-my.sharepoint.com/:i:/g/personal/arthur1_soulie_epitech_eu/EVYnZICB-Q1AgVTYd9vrL5IBwivVhSb5xuYj0qeD40nN2Q?e=BaU3l7)
> - Unwrap your two objects
> - Assign the trunck to the brown pixel and the leafs to the green pixel

## Animating models
