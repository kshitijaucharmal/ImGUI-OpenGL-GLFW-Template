# ImGUI + OpenGL + GLFW Template

This repository provides a clean and minimal C++ project template to get started with **Dear ImGui**, **OpenGL**, and **GLFW**. It's ideal for prototyping tools, UIs, and graphical applications with immediate mode GUI and modern OpenGL rendering.

---

## Features

- **Dear ImGui** (included locally, no submodule fuss)
- **OpenGL** for hardware-accelerated rendering
- **GLFW** for window/context creation and input handling
- Minimal CMake-based setup
- Easy to extend for your own apps and UIs

---

## Requirements

Make sure the following dependencies are installed on your system **before building**:

- **OpenGL** (system drivers)
- **GLFW** development libraries (e.g., `libglfw3-dev` on Ubuntu)
- **CMake** (version ≥ 3.10)
- **C++ compiler** with C++11 or newer support

---

## Building the Project

```bash
# Clone the repository
git clone https://github.com/kshitijaucharmal/ImGUI-OpenGL-GLFW-Template.git
cd ImGUI-OpenGL-GLFW-Template
# Rename ProjectName at the top of CMakeLists.txt

# Create and enter the build directory
mkdir build && cd build

# Generate Makefiles with CMake
cmake ..

# Build the project
make
````

---

## Running the Demo

After building, you should see an executable in the `build` directory:

```bash
./ProjectName
```

A window will open with a basic ImGui interface and OpenGL context — your playground starts here!

---

## Folder Structure

```
ImGUI-OpenGL-GLFW-Template/
├── CMakeLists.txt
├── main.cpp
├── external/
│   └── imgui/          # Dear ImGui source files (locally included)
│   └── glad/           # glad source files (locally included, replace these with your own if do no work)
```

---

## Adding Your Code

* Extend `main.cpp` with your own ImGui windows, widgets, and rendering logic.
* Use the existing OpenGL context for rendering anything from 2D UI overlays to 3D scenes.
* Add custom CMake targets or external libraries as needed.

---

## License

This template is provided under the MIT License. Dear ImGui retains its own MIT license within the `external/imgui` folder.

---

## Credits

* [Dear ImGui](https://github.com/ocornut/imgui) by Omar Cornut
* [GLFW](https://www.glfw.org/) — Multi-platform library for OpenGL
* OpenGL — Industry-standard graphics API

---

## Questions or Suggestions?

Feel free to open an [Issue](https://github.com/kshitijaucharmal/ImGUI-OpenGL-GLFW-Template/issues) or submit a [Pull Request](https://github.com/kshitijaucharmal/ImGUI-OpenGL-GLFW-Template/pulls)!

---

