# Magnum Game of Life

A C++ implementation of Conway's Game of Life using the Magnum graphics engine.

The project combines the rules of a cellular automaton with real-time graphical rendering.

## Features

* Conway's Game of Life
* C++ implementation
* Magnum graphics engine
* Real-time visualization
* Configurable simulation dimensions
* CMake build system
* Visual simulation results

## About Conway's Game of Life

Conway's Game of Life is a cellular automaton in which cells on a grid are either alive or dead.

The state of each cell is determined by its neighbouring cells.

The standard rules are:

1. A live cell with fewer than two live neighbours dies.
2. A live cell with two or three live neighbours survives.
3. A live cell with more than three live neighbours dies.
4. A dead cell with exactly three live neighbours becomes alive.

Simple rules can produce complex and evolving patterns.

## Technology Stack

* **C++**
* **Magnum**
* **CMake**

## Project Structure

```text
magnum-game-of-life/
├── modules/
├── src/
├── CMakeLists.txt
└── README.md
```

## Build

Create a build directory:

```bash
mkdir build
cd build
```

Configure the project:

```bash
cmake ..
```

Build the application:

```bash
cmake --build .
```

## Run

After building the project, start the executable:

```bash
./bin/MagnumGameOfLife
```

The simulation dimension can be configured using the `--dimension` option:

```bash
./bin/MagnumGameOfLife --dimension 32
```

## Simulation

The simulation repeatedly calculates the next generation of the cellular grid.

```text
Current Generation
        │
        ▼
Count Neighbours
        │
        ▼
Apply Game of Life Rules
        │
        ▼
Next Generation
        │
        ▼
Render
        │
        └──────────► Repeat
```

## Results

The repository contains several screenshots showing the visual result of the simulation at different stages.

These images are part of the project presentation and demonstrate the evolution of the Game of Life.

## Screenshots

The available project screenshots are kept in the repository and should be viewed together with the simulation.

![Game of Life Result](Screenshot-1.png)

Additional screenshots stored in the repository can be added here using their relative filenames.

## Configuration

The simulation grid can be configured when starting the application.

For example:

```bash
./bin/MagnumGameOfLife --dimension 32
```

Changing the dimension allows different grid sizes to be tested.

## Magnum

The project uses the **Magnum** graphics engine for rendering the cellular automaton.

Magnum provides the application and graphics functionality required to visualize the simulation.

## Possible Improvements

Possible future extensions include:

* Adjustable simulation speed
* Pause and resume functionality
* Interactive cell editing
* Additional starting patterns
* Different Game of Life rule sets
* Larger configurable grids
* Additional visualization modes

## Project Purpose

The project demonstrates how a classic cellular automaton can be implemented in C++ and visualized using a graphics framework.

It combines algorithmic logic with real-time rendering and provides a visual representation of how the cellular system evolves over time.

## Author

**Markus**

