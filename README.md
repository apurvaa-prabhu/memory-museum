# Memory Museumm

Memory Museum is an interactive web-based visual project that presents personal memories in a 360-degree circular gallery. Images are arranged in a rotating ring that users can spin, explore, and interact with. Clicking on an image opens a lightbox view that displays the photo along with a short description or story.

This project focuses on immersive visual interaction using Three.js, custom GLSL shaders, and smooth mouse-based controls.
![IMG_1620](https://github.com/user-attachments/assets/463ce06e-a7ca-4ece-8e31-9d419794b4fc)

![PNG image](https://github.com/user-attachments/assets/2c8a1948-b663-4d7a-b8a2-b4279423f971)

![IMG_6495](https://github.com/user-attachments/assets/a17c6ba0-6c75-45dd-beb3-f568c6d7d33b)



## Features

- 360-degree rotating image gallery
- Drag-to-rotate interaction with momentum
- Clickable images that open a lightbox with text
- Animated particle background using GLSL shaders
- Mouse-responsive visual effects
- Keyboard navigation support
- Responsive layout for desktop and mobile


## Technologies Used

- HTML5  
- CSS3  
- JavaScript (ES6)  
- Three.js  
- WebGL  
- GLSL Shaders  


## Project Structure

```text
museum/
├── index.html
├── README.md
├── img1.jpg
├── img2.jpg
├── img3.JPG
├── img4.jpg
├── img5.JPG
├── img6.JPG
├── img7.JPG
├── img8.JPG
├── img9.JPG
├── img10.JPG
├── img11.PNG
└── img12.JPG

--All logic, styling, shaders, and interactions are contained inside index.html.



## How to Run (Local Server Required):

This project cannot be opened directly by double-clicking index.html.
It must be accessed through a local HTTP server.

Start the Local Server
From the project root directory, run:
python3 -m http.server 8000
(If python3 is not available, try python -m http.server 8000.)
Access the Project
Open a browser and go to:
http://localhost:8000/museum/



## Controls & Interaction:

Mouse / Touch

Click and drag to rotate the gallery
Fast drag applies momentum
Click or tap an image to open its memory

Keyboard

Left Arrow → Rotate gallery left
Right Arrow → Rotate gallery right
ESC → Close the lightbox



## Visual System Overview:

Particle Background

The background consists of two animated particle layers rendered using custom vertex and fragment shaders. Particle motion is driven by sine and cosine functions and reacts dynamically to mouse movement, creating a smooth and immersive visual effect.

Image Gallery

Images are arranged evenly in a circular layout and always face the camera. Each image includes a subtle white glow frame to ensure visibility against the animated background.

Lightbox

When an image is selected, a lightbox opens displaying the full image along with its title and description. The lightbox can be closed by clicking outside the panel or pressing the ESC key.



## Memory Data:

Memory images and descriptions are defined in the MEMORIES array inside index.html.
const MEMORIES = [
  {
    src: "img1.jpg",
    title: "Memory 1",
    story: "Dinner with roommates!"
  }
];

To add a new memory:

Place the image file inside the museum folder
Add a new object to the MEMORIES array



## License:

This project was created for educational purposes.
All images belong to their respective owners.



## Acknowledgments:

Three.js for 3D rendering
Open-source WebGL and shader resources
Inspiration from wndr wall and insta nonsense from the wndr museum.



## Sources & Code Validation:

The implementation and techniques used in Memory Museum are based on well-documented, industry-standard web graphics practices. The following sources validate the correctness and legitimacy of the code structure, APIs, and interaction patterns used in this project.


Three.js Official Documentation
https://threejs.org/docs/
Used for scene creation, cameras, meshes, materials, raycasting, texture loading, and rendering.

Three.js Examples
https://threejs.org/examples/
Confirms best practices for particle systems, interactive scenes, and object picking.

MDN Web Docs – WebGL API
https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API
Validates use of WebGL contexts, GPU rendering, and shader-based graphics.

MDN Web Docs – <canvas> Element
https://developer.mozilla.org/en-US/docs/Web/HTML/Element/canvas
Supports the use of a canvas-based rendering pipeline.


Khronos Group – OpenGL ES Shading Language
https://www.khronos.org/opengl/wiki/Core_Language_(GLSL) 
To confirm correctness of vertex and fragment shader structure and syntax.


Three.js Raycaster Documentation
https://threejs.org/docs/#api/en/core/Raycaster 
Validates click and touch-based object selection used to open the lightbox.

MDN Web Docs – Pointer & Mouse Events
https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent
Confirms correct handling of mouse, touch, and keyboard input.


WNDR Museum – WNDR Wall Installation
https://www.wndrmuseum.com/location/boston#location-installations-gallery 
The animated particle motion in the background is inspired by the flowing, reactive light movement seen in the WNDR Wall installation.
The circular photo gallery layout is inspired by the Insta-Nonsense picture wall, translating a physical immersive display into an interactive digital space.
