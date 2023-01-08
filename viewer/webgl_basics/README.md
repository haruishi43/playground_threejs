# WebGL


Steps:

1. Basics
2. Objects (Mesh and Geometry)
3. Camera


## Da basics:

> Three.js uses the concept of _display list_. It means that all objects are stored in the list and then drawn to the screen.

What is a __display list__?

- All objects are stored in the list and then drawn to the screen
    - `THREE.Scene` object
- Add anything you want to be drawn on the `Scene`
- You can have multiple `Scene` objects, but one renderer can draw only one scene at once

The `Renderer`:

- Simply draws everything from the scene to the WebGL canvas
- Supports drawing on SVG or 2D Canvas -> but the focus is WebGL

### Notes:

- Antialias to true means that edges of objects are smootha dn not jagged
- 


## The Cube!

Goal: add something to be drawn:

In Three.js, the objects that are being drawn on the screen are called __meches__.
Each mesh has to have its own __geometry__ and __material__.

Geometry:

- A set of points that need to be connected in order to create the object.

Material:

- _The Paint_, that will cover the object.

### Notes:

- `CubeGeometry(height, width, depth)`
- `MeshLambertMaterial({color: HEX})`
- `THREE.Mesh(Geometry, Matrial)`


## Camera!

> To render something, first we need to add the camera to the scene so that the renderer knows from which point of view it should render stuff.

There are few types of cameras:

[Shown in this documentation](https://threejs.org/docs/#api/en/cameras/Camera)


Here we use `THREE.PerspectiveCamera`.


## Lights!

The cube turns out to be black...
This is because there are no lights on the scene (pretty much like a black room).


## Action!

To make the cube animate, we have to add the render loop to our app. This can be achieved using the renderAnimationFrame function, which was created specially for that purpose. It's supported in most of the major browsers, and for those which doesn't support it, Three.js comes with its own polyfill. 



## Graph overview:

- Scene
    - Canvas
    - Light
    - Mesh
        - Geometry
        - Material
            - Texture
            - Texture...