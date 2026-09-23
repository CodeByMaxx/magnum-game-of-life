# Magnum Game of Life

A Conway's Game of Life implementation written in C++ using the Magnum graphics engine.

The project combines a cellular automaton with real-time visualization and interactive controls.

## Features

* Conway's Game of Life
* C++ implementation
* Magnum graphics engine
* Real-time visualization
* Configurable simulation dimensions
* Interactive simulation
* CMake build system

## Game of Life

Conway's Game of Life is a cellular automaton based on a simple set of rules.

Each cell can be either:

* **Alive**
* **Dead**

The state of each cell is determined by its neighbouring cells.

The standard rules are:

1. A live cell with fewer than two live neighbours dies.
2. A live cell with two or three live neighbours survives.
3. A live cell with more than three live neighbours dies.
4. A dead cell with exactly three live neighbours becomes alive.

Despite these simple rules, complex patterns can emerge from the simulation.

## Technology Stack

* **C++**
* **Magnum**
* **CMake**

## Project Structure

```text id="x1j5n8"
magnum-game-of-life/
├── modules/
├── src/
├── CMakeLists.txt
└── README.md
```

## Build

Create a build directory:

```bash id="k1j7r4"
mkdir build
cd build
```

Configure the project with CMake:

```bash id="h3m8y6"
cmake ..
```

Build the application:

```bash id="v7p2q9"
cmake --build .
```

## Run

After building the project, start the executable:

```bash id="m4c8z1"
./bin/MagnumGameOfLife
```

The simulation can be started with a configurable dimension.

Example:

```bash id="r9d3k5"
./bin/MagnumGameOfLife --dimension 32
```

## Simulation

The simulation updates the state of the cellular grid continuously.

Each iteration calculates the number of living neighbours for every cell and applies the Game of Life rules.

```text id="n6w2p4"
Current Grid
     │
     ▼
Count Neighbours
     │
     ▼
Apply Game of Life Rules
     │
     ▼
Generate Next Grid
     │
     ▼
Render
     │
     └──────► Next Iteration
```

## Results

The following screenshots show the rendered Game of Life simulation at different stages.

### Result 1

![Game of Life Result 1](frame_00050.png)

### Result 2

![Game of Life Result 2](frame_01000.png)

### Result 3

![Game of Life Result 3](frame_04000.png)

### Result 4

![Game of Life Result 4](frame_05000.png)

## Screenshots

Additional screenshots from the project are included in the repository and demonstrate the visual output of the Magnum application.

## Configuration

The simulation dimension can be configured when starting the application.

For example:

```bash id="c5m7q2"
./bin/MagnumGameOfLife --dimension 32
```

This allows different grid sizes to be tested without changing the source code.

## Magnum

The project uses the Magnum graphics engine to render the simulation.

Magnum provides the graphics and application framework required to display the cellular automaton in real time.

## Possible Improvements

Possible future extensions include:

* Additional simulation patterns
* Adjustable simulation speed
* Pause and resume controls
* Interactive cell editing
* Different Game of Life rule sets
* Larger configurable grids
* Additional visualisation options

## Project Purpose

The project demonstrates how a relatively simple cellular automaton can be implemented in C++ and visualized using a modern graphics framework.

It combines algorithmic logic with real-time ren

