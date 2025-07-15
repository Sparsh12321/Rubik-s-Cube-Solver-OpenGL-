# 🧊 Rubik's Cube Solver - OpenGL

![C++](https://img.shields.io/badge/C%2B%2B-OpenGL-blue?logo=c%2B%2B&logoColor=white)
![License](https://img.shields.io/github/license/Sparsh12321/Rubik-s-Cube-Solver-OpenGL)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-lightgrey)

A 3D interactive Rubik’s Cube visualizer and solver built using **OpenGL** and **C++**, capable of solving any scrambled cube using the **Breadth-First Search (BFS)** algorithm. This project combines the logic of cube solving with real-time rendering and animation.

---

## ✨ Features

- 🎮 Interactive 3D Rubik’s Cube using **OpenGL**
- 🤖 Automatic solver using **Breadth-First Search (BFS)**
- 🔀 Random scrambler with valid move sequences
- 🎞️ Smooth cube rotation and layer-turn animations
- 🧠 Solves from **any valid cube state**
- 🪟 Simple keyboard/mouse controls

---

## 📸 Demo
![IMG-20250715-WA0009](https://github.com/user-attachments/assets/90660782-58d6-43e3-b9ea-270aacea86c9)
![IMG-20250715-WA0007](https://github.com/user-attachments/assets/df58663b-c8fd-4cda-a497-2887a8c4840a)
![IMG-20250715-WA0006](https://github.com/user-attachments/assets/3036a46e-0312-408d-8e50-dc4d71393898)
![IMG-20250715-WA0008](https://github.com/user-attachments/assets/62633c5b-3ebc-465b-8680-367424c5aaf7)

---

## 🧠 Algorithm - BFS Explained

This project uses **Breadth-First Search (BFS)** to solve the Rubik's Cube:

- Treats the cube as a **state-space tree**, where each node represents a cube state.
- Each edge corresponds to a **valid move** (e.g., U, R', F2).
- Performs a level-order traversal starting from the scrambled state.
- Stores visited states using a **hash map** or cube string representation to avoid revisiting.
- The goal is the **solved state**, and the first match guarantees the shortest move sequence.

Though BFS is not optimal for speed or memory in large-depth searches, it's sufficient for short scrambles and guarantees the **shortest path** in terms of moves.

---

## 🛠️ Tech Stack

- **Language:** C++
- **Graphics API:** OpenGL
- **Math:** GLM (optional), custom matrix logic
- **Platform:** Windows / Linux

---

## 🚀 Getting Started

### 🔧 Requirements

- C++ Compiler (e.g., g++, clang++)
- OpenGL
- GLUT or FreeGLUT
- CMake (optional)

### 🔨 Build & Run

```bash
# Clone the repository
git clone https://github.com/Sparsh12321/Rubik-s-Cube-Solver-OpenGL.git
cd Rubik-s-Cube-Solver-OpenGL

# Compile (example using g++)
g++ main.cpp -o cube_solver -lGL -lGLU -lglut

# Run the executable
./cube_solver
