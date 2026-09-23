# Magnum Game of Life

A configurable implementation of **Conway's Game of Life** with an interactive visualization and command-line configuration.

The project focuses on simulating cellular automata efficiently while providing different ways to configure the simulation and inspect its behavior.

## Overview

Conway's Game of Life is a cellular automaton in which each cell is either alive or dead.

Each generation is calculated from the state of the surrounding cells according to the classic Game of Life rules:

* A live cell with fewer than two neighbors dies.
* A live cell with two or three neighbors survives.
* A live cell with more than three neighbors dies.
* A dead cell with exactly three neighbors becomes alive.

Despite these simple rules, the simulation produces complex patterns and long-running structures.

---

## Features

* Conway's Game of Life simulation
* Configurable board dimensions
* Configurable simulation parameters
* Interactive visualization
* Randomized starting configurations
* Command-line configuration
* Multiple simulation examples
* Performance/benchmark measurements
* Screenshot examples

---

## Project Structure

```text
magnum-game-of-life/
│
├── bin/
│
├── ...
├── screenshots/
│
└── README.md
```

The `bin/` directory contains the generated executable/build output.

---

## Requirements

A C++ development environment and the libraries required by the project are needed to build the application.

The exact dependencies depend on the platform and graphics configuration used for the project.

---

## Build

Build the project using the build configuration included in the repository.

After building, the resulting executable is available under:

```text
./bin/
```

---

## Running the Simulation

The application can be started from the command line.

Example:

```bash
./bin/<executable>
```

The simulation supports command-line configuration for parameters such as the board dimension.

For example:

```bash
./bin/<executable> --dimension 100
```

Use:

```bash
./bin/<executable> --help
```

to inspect the available command-line options.

---

## Simulation

The simulation operates generation by generation.

A generation consists of:

1. evaluating the neighbors of each cell
2. applying the Game of Life rules
3. creating the next board state
4. updating the visualization
5. continuing with the next generation

The simulation can produce stable structures, oscillators and moving patterns depending on the initial state.

---

## Screenshots

The repository contains several screenshots demonstrating the simulation:

```text
screenshots/
```

Examples include different board states and simulation configurations.

---

## Performance

The project also contains benchmark/performance information.

Performance depends on factors such as:

* board dimensions
* number of generations
* hardware
* rendering overhead
* simulation configuration

For meaningful comparisons, benchmarks should be performed under the same configuration and hardware conditions.

---

## Command-Line Options

The application provides command-line options for configuring the simulation.

One of the main parameters is the board dimension:

```bash
--dimension <value>
```

Example:

```bash
./bin/<executable> --dimension 200
```

Run the application with `--help` to see the complete set of supported options.

---

## Why Game of Life?

Game of Life is a useful example for experimenting with:

* cellular automata
* simulation algorithms
* grid-based computation
* state transitions
* visualization
* performance optimization
* algorithmic complexity

The project is also useful for exploring how simple local rules can produce complex global behavior.

---

## Project Status

The project provides a working Game of Life simulation with visualization and configurable simulation parameters.

The repository also contains example screenshots and benchmark information.

Future improvements could include:

* additional predefined patterns
* improved rendering performance
* more benchmark automation
* configuration files
* automated tests
* additional visualization options

---

## Author

**Markus**

Simulation / C++ project.

