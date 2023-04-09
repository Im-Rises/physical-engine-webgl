# physical-engine-webgl

<p align="center">
      <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" alt="cppLogo" style="height:60px;"/>
      <img src="https://img.shields.io/badge/OpenGL-FFFFFF?style=for-the-badge&logo=opengl" alt="openglLogo" style="height:60px;"/>
      <img src="https://user-images.githubusercontent.com/59691442/183268126-b3d19e66-8f2d-463a-805e-ae6ef7cc6c01.png" alt="cmakeLogo" style="height:60px;"/>
      <img src="https://user-images.githubusercontent.com/59691442/226524871-c73aa62f-d191-42d3-a1b9-ebbfc216a7bb.png" alt="webglLogo" style="height:60px;"/>
      <img src="https://user-images.githubusercontent.com/59691442/190315147-ec9dc33f-0090-4f0d-98ab-514eb1463e01.png" alt="glfwLogo" style="height:60px;"/>
</p>

## Description

This is a simple physics engine written in C++ using Glad, GLFW, OpenGl3 and Dear ImGui.

This repository is a port of the [PhysicalEngine](https://github.com/Im-Rises/physical-engine-webgl) project to WebGL2.

## 🚀🚀 [You can test it online here](https://im-rises.github.io/physical-engine-webgl/) 🚀🚀

> **Note**  
> The project is made as an educational project to learn more about physics and game engine development.

## Features

### Physics features

- [x] Basic object types (Sphere, Cube, Cylinder, Plane)
- [x] Particle and Rigid Body Physics
- [x] Collision Detection
- [x] Forces (Gravity, Drag, Spring, Buoyancy)
- [x] Torque forces (Angular Drag, Angular Spring)
- [x] Different types of constraints

### User Interface features

- [x] Camera Controls
- [x] GameObjects Inspector
- [x] Scene Hierarchy

### Other features

- [x] Basic ECS (Entity Component System)
- [x] Component Oriented Programming
- [x] Fixed Framerate
- [x] GameObject's speed Graph visualization

## Images

![RigidBodyImage](https://user-images.githubusercontent.com/59691442/204342827-5407dc9f-c05e-4a26-b513-b37ce5ab7d14.png)

![screenshot2](https://user-images.githubusercontent.com/59691442/206077820-3edaff06-8d5e-4187-a575-251b4acec8d3.png)

<!--
![preview_screenshot](https://user-images.githubusercontent.com/59691442/196303021-781cf236-4bab-4523-9f08-2a85c7dd491c.png)
![image1](https://user-images.githubusercontent.com/59691442/192190493-f1191715-268e-43e4-8f27-5ed0c2823dfa.png)
![image2](https://user-images.githubusercontent.com/59691442/192190499-457463ae-7a34-432a-bb0b-063771021275.png)
-->

<!--
## Report

You can find a journal log [here](report/development_log_phase1_REBOUL_CLAVEL_MOREL.pdf).  
It is also located in the `report` folder.
-->

## Building

To build the project, you need to use a UNIX system, like Ubuntu or if you're on Windows you can use WSL.
Then you have to install Emscripten. You can find
instructions on how to install Emscripten here:  
<https://emscripten.org/docs/getting_started/downloads.html>

You also need to have CMake and make installed. You can find instructions on how to
install CMake here:  
<https://cmake.org/install/>

Make can be installed by running this command in the terminal:

```bash
sudo apt install make
```

Once you have Emscripten and CMake installed run this command in the project root directory:

```bash
emcmake cmake .
```

Then run this command in the same directory:

```bash
emmake make
```

## To test the website locally

To test the website locally, you need to have Python installed. You can find instructions on how to install Python here:

<https://www.python.org/downloads/>

Once you have Python installed, run this command in the project build directory:

```bash
python -m http.server
```

Then open your browser and go to this address:

<http://localhost:8000/>

## Controls

### Game controls

To modify the speed value, you can use the ImGui window named `Speed handler`.

| Action                 | Key |
|------------------------|-----|
| Add speed to the left  | ←   |
| Add speed to the right | →   |
| Add speed forwardly    | ↑   |
| Add speed rearward     | ↓   |

### User controls

| Action                        | Key                                   |
|-------------------------------|---------------------------------------|
| Toggle fullscreen             | F11                                   |
| Camera zoom                   | Mouse wheel                           |
| Translate camera to the left  | Right Mouse Button + Mouse ← movement |
| Translate camera to the right | Right Mouse Button + Mouse → movement |
| Translate camera upwards      | Right Mouse Button + Mouse ↑ movement |
| Translate camera downwards    | Right Mouse Button + Mouse ↓ movement |
| Exit app                      | ESC                                   |

## Dependencies

- C++ 14
- CMake
- Emscripten (2.0.29)
- GLFW (3.3.8)
- OpenGl (3.3)
- Glad (0.1.36)
- Dear ImGui (1.89.4)
- glm (0.9.8)

## Run tests

The project has unit tests to check come common classes. You can find them in the `test` folder.

## GitHub Actions

This project uses GitHub Actions to build the project and deploy it to GitHub

[![CodeQL](https://github.com/Im-Rises/physical-engine-webgl/actions/workflows/codeql.yml/badge.svg?branch=main)](https://github.com/Im-Rises/physical-engine-webgl/actions/workflows/codeql.yml)
[![CMake](https://github.com/Im-Rises/physical-engine-webgl/actions/workflows/cmake.yml/badge.svg?branch=main)](https://github.com/Im-Rises/physical-engine-webgl/actions/workflows/cmake.yml)
[![flawfinder](https://github.com/Im-Rises/physical-engine-webgl/actions/workflows/flawfinder.yml/badge.svg?branch=main)](https://github.com/Im-Rises/physical-engine-webgl/actions/workflows/flawfinder.yml)
[![cpp-linter](https://github.com/Im-Rises/physical-engine-webgl/actions/workflows/cpp-linter.yml/badge.svg?branch=main)](https://github.com/Im-Rises/physical-engine-webgl/actions/workflows/cpp-linter.yml)
[![Emscripten-CMake](https://github.com/Im-Rises/physical-engine-webgl/actions/workflows/emscripten-cmake.yml/badge.svg)](https://github.com/Im-Rises/physical-engine-webgl/actions/workflows/emscripten-cmake.yml)
[![Emscripten-Publish](https://github.com/Im-Rises/physical-engine-webgl/actions/workflows/emscripten-publish.yml/badge.svg)](https://github.com/Im-Rises/physical-engine-webgl/actions/workflows/emscripten-publish.yml)

The project is set with a set of different scripts:

- CodeQL: This script is used to check the code for security issues.
- CMake: This script is used to build the project.
- Cpp Cmake Publish: This script is used to publish the project on GitHub.
- Flawfinder: This script is used to check the code for security issues.
- Microsoft C++ Code Analysis: This script is used to check the code for security issues.
- Cpp Linter: This script is used to check the code for security issues.
- Emscripten CMake: This script is used to test build of the project using Emscripten toolchain.
- Emscripten-Publish: This script build to webgl and publish the project on GitHub Pages.

## Documentations

OpenGL:  
<https://www.khronos.org/registry/OpenGL-Refpages/gl4/>

OpenGL loading library:  
<https://www.khronos.org/opengl/wiki/OpenGL_Loading_Library>

GLFW:  
<https://www.glfw.org/docs/latest/>

Dear ImGui:  
<https://github.com/ocornut/imgui>

GLAD:  
<https://glad.dav1d.de/>

GLM:  
<https://glm.g-truc.net/0.9.8/index.html>

STB:  
<https://github.com/nothings/stb>

ImPlot:  
<https://github.com/epezent/implot>

Learn OpenGL:  
<https://learnopengl.com/Getting-started/Hello-Triangle>

Developpez Learn OpenGL (Translated in French):  
<https://opengl.developpez.com/tutoriels/apprendre-opengl/?page=creer-une-fenetre#L4-5>  
<https://opengl.developpez.com/tutoriels/opengl-tutorial/>

Sphere OpenGL:  
<http://www.songho.ca/opengl/gl_sphere.html>

unrealistic.dev (Change CMake working directory):  
<https://unrealistic.dev/posts/setting-debug-parameters-with-cmake-tools-for-visual-studio>

## Contributors on the WebGL port

Quentin MOREL:

- @Im-Rises
- <https://github.com/Im-Rises>

[![GitHub contributors](https://contrib.rocks/image?repo=Im-Rises/physical-engine-webgl)](https://github.com/Im-Rises/physical-engine-webgl/graphs/contributors)

## Contributors on the original project

Quentin MOREL:

- @Im-Rises
- <https://github.com/Im-Rises>

Gabriel REBOUL:

- @spiryti
- <https://github.com/spiryti>

Clémence CLAVEL:

- @clemos38
- <https://github.com/clemos38>

[![GitHub contributors](https://contrib.rocks/image?repo=Im-Rises/PhysicalEngine)](https://github.com/Im-Rises/PhysicalEngine/graphs/contributors)