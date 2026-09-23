# Game of Life with Magnum

A real-time implementation of **Conway's Game of Life** built with **C++** and the **Magnum graphics engine**.

The project combines a cellular automaton with real-time rendering to visualize the evolution of a grid-based simulation.

---

## Features

* 🧬 Conway's Game of Life
* 🎨 Real-time rendering with Magnum
* ⚡ Real-time simulation
* 🔄 Continuous generation updates
* 🖥️ Interactive visualization
* 📊 Simulation and rendering benchmarks

---

## Screenshots

![Screenshot 1](Screenshot-1.png)
![Screenshot 2](Screenshot-2.png)
![Screenshot 3](Screenshot-3.png)
![Screenshot 4](Screenshot-4.png)
![Screenshot 5](Screenshot-5.png)
![Screenshot 6](Screenshot-6.png)
![Screenshot 7](Screenshot-7.png)

---

## Conway's Game of Life

Conway's Game of Life is a cellular automaton based on four simple rules.

For each generation, every cell examines its neighboring cells.

### Survival

A living cell survives when it has **two or three living neighbors**.

### Death

A living cell dies when:

* It has fewer than two neighbors — underpopulation
* It has more than three neighbors — overpopulation

### Birth

A dead cell becomes alive when it has **exactly three living neighbors**.

Despite the simplicity of these rules, the simulation can produce complex and evolving structures.

---

## Technologies

| Technology | Purpose                             |
| ---------- | ----------------------------------- |
| **C++**    | Simulation logic                    |
| **Magnum** | Rendering and application framework |
| **OpenGL** | Graphics rendering                  |
| **CMake**  | Build system                        |

---

## Simulation

The simulation operates on a two-dimensional grid.

Each generation follows this process:

```text id="u2j5yq"
Current Generation
        │
        ▼
Count Neighbors
        │
        ▼
Apply Game of Life Rules
        │
        ▼
Next Generation
        │
        └──────────────► Repeat
```

The next generation is calculated from the current generation so that updates do not influence other cells during the same simulation step.

---

## Rendering

Magnum is used to visualize the current state of the cellular automaton.

Each cell can be represented visually according to its state:

```text id="3k3g9b"
Alive   →  ■
Dead    →  □
```

The renderer updates continuously as the simulation progresses.

---

## Building

### Requirements

* C++ compiler
* CMake
* Magnum
* OpenGL-compatible graphics environment

Clone the repository:

```bash id="q5d9x1"
git clone https://github.com/CodeByMaxx/magnum-game-of-life.git
cd magnum-game-of-life
```

Create a build directory:

```bash id="4p0x7c"
mkdir build
cd build
```

Configure:

```bash id="1b6c4s"
cmake ..
```

Build:

```bash id="x8y4pn"
cmake --build .
```

---

## Benchmarking

The project also includes benchmark functionality for evaluating simulation performance.

This makes it possible to investigate the cost of updating the cellular automaton and compare different implementations or simulation configurations.

---

## Project Goals

The project was created to explore:

* Cellular automata
* C++ application development
* Real-time rendering
* Magnum
* OpenGL
* Simulation performance
* Benchmarking

---

## Future Improvements

Possible improvements include:

* [ ] Interactive cell editing
* [ ] Pause and resume controls
* [ ] Configurable simulation speed
* [ ] Load predefined patterns
* [ ] Additional benchmark scenarios
* [ ] Rendering optimizations
* [ ] GPU-based simulation

---

## License

This project is licensed under the **MIT License**.

