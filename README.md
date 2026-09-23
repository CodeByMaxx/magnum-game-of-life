# Magnum Game of Life

A C/C++ implementation of **Conway's Game of Life** visualized in 2D and 3D using the [Magnum](https://magnum.graphics/) graphics engine.

The project supports different computation modes, including:

* CPU serial computation
* CPU parallel computation
* GPU parallel computation

The application can be used to experiment with different grid dimensions and compare the resulting computation times.

---

## Overview

The project combines a Game of Life simulation with real-time 2D and 3D visualization.

The simulation can be executed with different dimensions and computation modes:

```text
Game of Life
     |
     +----------------------+
     |                      |
     v                      v
    2D                     3D
     |                      |
     +----------+-----------+
                |
                v
        Computation Mode
                |
       +--------+--------+
       |        |        |
       v        v        v
   CPU Serial CPU Parallel GPU Parallel
```

---

## Features

* Conway's Game of Life
* 2D simulation
* 3D simulation
* Magnum-based visualization
* CPU serial computation
* CPU parallel computation
* GPU parallel computation
* Configurable simulation dimensions
* Runtime computation measurements

---

# Screenshots

## 3D

The project contains several 3D visualizations of the simulation:

![Top Ansicht für Game of Life](Screenshot-3.png)

![Top Ansicht für Game of Life](Screenshot-1.png)

![Top Ansicht für Game of Life](Screenshot-2.png)

## 2D

The 2D version provides a separate visualization:

![Top Ansicht für Game of Life](Screenshot-4.png)

![Top Ansicht für Game of Life](Screenshot-5.png)

![Top Ansicht für Game of Life](Screenshot-6.png)

---

# Technology

The project is based primarily on:

* C/C++
* [Magnum](https://magnum.graphics/)
* [Corrade](https://magnum.graphics/corrade/)
* CMake

Magnum is used for visualization and application functionality, while Corrade provides utility functionality used by the Magnum ecosystem.

---

# Dependencies

Before building this project, **Corrade must be built before Magnum**.

The project expects the Magnum and Corrade source trees to be available locally.

A typical directory layout is:

```text
.
├── build
├── CMakeLists.txt
├── corrade -> ../../corrade/
├── magnum -> ../../magnum/
├── modules
├── README.md
└── src
```

---

# Building Dependencies

## 1. Build Corrade

Clone or otherwise provide the Corrade source tree and build it first:

```bash
cd corrade
mkdir build
cd build
cmake ..
cmake --build .
```

## 2. Build Magnum

After Corrade has been built:

```bash
cd magnum
mkdir build
cd build

cmake .. \
    -DMAGNUM_WITH_SDL2APPLICATION=ON

make
make install
```

After Magnum has been installed, the Game of Life project can be built.

---

# Build the Project

Clone the project and create a build directory:

```bash
cd magnum-game-of-life
mkdir build
cd build
```

Configure the project:

```bash
cmake ..
```

Build:

```bash
cmake --build .
```

---

# Running the Simulation

The project provides separate executables for the 3D and 2D versions.

## 3D

Example:

```bash
./bin/MagnumGameOfLife --dimension 32 --computemode 1
```

## 2D

Example:

```bash
./bin/MagnumGameOfLife2d --dimension 512 --computemode 1
```

The dimension controls the size of the simulation grid.

---

# Computation Modes

The application supports different computation modes.

| Mode | Description  |
| ---: | ------------ |
|  `1` | CPU Serial   |
|  `2` | CPU Parallel |
|  `3` | GPU Parallel |

This allows the same simulation to be executed using different processing strategies.

---

# Benchmark Results

The application reports the computation time for each iteration.

The following results are preserved from the original project.

## 3D – Dimension 32

### CPU Serial

```text
Computing took 0.00742187s with mode: CPUSerial
Computing took 0.00565313s with mode: CPUSerial
Computing took 0.00623309s with mode: CPUSerial
Computing took 0.00578718s with mode: CPUSerial
Computing took 0.00568398s with mode: CPUSerial
Computing took 0.00676035s with mode: CPUSerial
Computing took 0.00653602s with mode: CPUSerial
Computing took 0.00592304s with mode: CPUSerial
Computing took 0.00611048s with mode: CPUSerial
Computing took 0.00593799s with mode: CPUSerial
Computing took 0.00599404s with mode: CPUSerial
Computing took 0.00687863s with mode: CPUSerial
Computing took 0.00660276s with mode: CPUSerial
Computing took 0.00679046s with mode: CPUSerial
Computing took 0.00567988s with mode: CPUSerial
Computing took 0.00575742s with mode: CPUSerial
Computing took 0.00578882s with mode: CPUSerial
Computing took 0.00594202s with mode: CPUSerial
```

### CPU Parallel

```text
Computing took 0.00172155s with mode: CPUParallel
Computing took 0.00105463s with mode: CPUParallel
Computing took 0.000949706s with mode: CPUParallel
Computing took 0.00104956s with mode: CPUParallel
Computing took 0.0011585s with mode: CPUParallel
Computing took 0.000895827s with mode: CPUParallel
Computing took 0.00127591s with mode: CPUParallel
Computing took 0.000948812s with mode: CPUParallel
Computing took 0.000963206s with mode: CPUParallel
Computing took 0.00112893s with mode: CPUParallel
Computing took 0.000975872s with mode: CPUParallel
Computing took 0.000988148s with mode: CPUParallel
Computing took 0.000924745s with mode: CPUParallel
Computing took 0.000995989s with mode: CPUParallel
Computing took 0.00107612s with mode: CPUParallel
Computing took 0.00115494s with mode: CPUParallel
Computing took 0.00109494s with mode: CPUParallel
Computing took 0.000876133s with mode: CPUParallel
```

### GPU Parallel

```text
Computing took 0.0699127s with mode: GPUParallel
Computing took 0.000171408s with mode: GPUParallel
Computing took 0.000175476s with mode: GPUParallel
Computing took 0.000176083s with mode: GPUParallel
Computing took 0.000176546s with mode: GPUParallel
Computing took 0.000177566s with mode: GPUParallel
Computing took 0.000176215s with mode: GPUParallel
Computing took 0.000214109s with mode: GPUParallel
Computing took 0.000200467s with mode: GPUParallel
Computing took 0.000468735s with mode: GPUParallel
Computing took 0.000176499s with mode: GPUParallel
Computing took 0.000402352s with mode: GPUParallel
Computing took 0.000174336s with mode: GPUParallel
Computing took 0.000173134s with mode: GPUParallel
Computing took 0.000191444s with mode: GPUParallel
Computing took 0.000180986s with mode: GPUParallel
Computing took 0.000169251s with mode: GPUParallel
Computing took 0.000172731s with mode: GPUParallel
Computing took 0.000184641s with mode: GPUParallel
Computing took 0.00017047s with mode: GPUParallel
Computing took 0.000171859s with mode: GPUParallel
Computing took 0.000166565s with mode: GPUParallel
Computing took 0.00079048s with mode: GPUParallel
Computing took 0.000210384s with mode: GPUParallel
Computing took 0.000174102s with mode: GPUParallel
```

## 3D – Dimension 64

### CPU Serial

```text
Computing took 0.0555197s with mode: CPUSerial
Computing took 0.0539763s with mode: CPUSerial
Computing took 0.0545522s with mode: CPUSerial
Computing took 0.0543793s with mode: CPUSerial
Computing took 0.0544335s with mode: CPUSerial
Computing took 0.053008s with mode: CPUSerial
Computing took 0.0563637s with mode: CPUSerial
Computing took 0.0537417s with mode: CPUSerial
Computing took 0.053884s with mode: CPUSerial
Computing took 0.0531526s with mode: CPUSerial
Computing took 0.0570132s with mode: CPUSerial
Computing took 0.0548666s with mode: CPUSerial
Computing took 0.0551864s with mode: CPUSerial
Computing took 0.0569083s with mode: CPUSerial
Computing took 0.053993s with mode: CPUSerial
Computing took 0.0525571s with mode: CPUSerial
Computing took 0.0554101s with mode: CPUSerial
Computing took 0.054908s with mode: CPUSerial
Computing took 0.0529288s with mode: CPUSerial
Computing took 0.0561799s with mode: CPUSerial
```

### CPU Parallel

```text
Computing took 0.0114412s with mode: CPUParallel
Computing took 0.0126738s with mode: CPUParallel
Computing took 0.0114358s with mode: CPUParallel
Computing took 0.014497s with mode: CPUParallel
Computing took 0.0103546s with mode: CPUParallel
Computing took 0.0101551s with mode: CPUParallel
Computing took 0.0116963s with mode: CPUParallel
Computing took 0.0105105s with mode: CPUParallel
Computing took 0.0124741s with mode: CPUParallel
Computing took 0.0123243s with mode: CPUParallel
Computing took 0.0114928s with mode: CPUParallel
Computing took 0.0124942s with mode: CPUParallel
Computing took 0.0126372s with mode: CPUParallel
Computing took 0.0102884s with mode: CPUParallel
Computing took 0.0114197s with mode: CPUParallel
Computing took 0.0110162s with mode: CPUParallel
Computing took 0.012086s with mode: CPUParallel
Computing took 0.0114237s with mode: CPUParallel
Computing took 0.0121604s with mode: CPUParallel
Computing took 0.0128584s with mode: CPUParallel
```

### GPU Parallel

```text
Computing took 0.00124912s with mode: GPUParallel
Computing took 0.000543594s with mode: GPUParallel
Computing took 0.000573824s with mode: GPUParallel
Computing took 0.000461596s with mode: GPUParallel
Computing took 0.000441742s with mode: GPUParallel
Computing took 0.000460211s with mode: GPUParallel
Computing took 0.000465593s with mode: GPUParallel
Computing took 0.000603652s with mode: GPUParallel
Computing took 0.000529718s with mode: GPUParallel
Computing took 0.000520486s with mode: GPUParallel
Computing took 0.000515063s with mode: GPUParallel
Computing took 0.000519765s with mode: GPUParallel
Computing took 0.001021s with mode: GPUParallel
Computing took 0.000516255s with mode: GPUParallel
Computing took 0.000456314s with mode: GPUParallel
Computing took 0.000453337s with mode: GPUParallel
Computing took 0.000493486s with mode: GPUParallel
Computing took 0.00108582s with mode: GPUParallel
Computing took 0.000460295s with mode: GPUParallel
```

---

# 2D Benchmark

The 2D version was tested with a dimension of `512`.

## CPU Serial

```text
Computing took 0.01658s with mode: CPUSerial
Computing took 0.0160181s with mode: CPUSerial
Computing took 0.0164174s with mode: CPUSerial
Computing took 0.0161741s with mode: CPUSerial
Computing took 0.0155877s with mode: CPUSerial
Computing took 0.0159631s with mode: CPUSerial
Computing took 0.0163439s with mode: CPUSerial
```

## CPU Parallel

```text
Computing took 0.00466909s with mode: CPUParallel
Computing took 0.00490792s with mode: CPUParallel
Computing took 0.00478843s with mode: CPUParallel
Computing took 0.00498489s with mode: CPUParallel
Computing took 0.00510148s with mode: CPUParallel
Computing took 0.00550885s with mode: CPUParallel
Computing took 0.00664743s with mode: CPUParallel
Computing took 0.00769989s with mode: CPUParallel
Computing took 0.00524594s with mode: CPUParallel
Computing took 0.00553464s with mode: CPUParallel
Computing took 0.00489609s with mode: CPUParallel
Computing took 0.00455409s with mode: CPUParallel
```

## GPU Parallel

```text
Computing took 0.000853757s with mode: GPUParallel
Computing took 0.000692443s with mode: GPUParallel
Computing took 0.000889844s with mode: GPUParallel
Computing took 0.000740654s with mode: GPUParallel
Computing took 0.000690138s with mode: GPUParallel
Computing took 0.000761807s with mode: GPUParallel
Computing took 0.000784518s with mode: GPUParallel
Computing took 0.000872844s with mode: GPUParallel
Computing took 0.00136589s with mode: GPUParallel
Computing took 0.00071443s with mode: GPUParallel
Computing took 0.00096284s with mode: GPUParallel
Computing took 0.00065436s with mode: GPUParallel
Computing took 0.000755198s with mode: GPUParallel
Computing took 0.000708947s with mode: GPUParallel
```

---

# Project Structure

```text
magnum-game-of-life
├── build
├── CMakeLists.txt
├── modules
├── src
├── corrade -> ../../corrade/
├── magnum -> ../../magnum/
└── README.md
```

The `corrade` and `magnum` entries refer to the locally available dependency trees used to build the project.

---

# Purpose

This project combines a classic cellular-automaton simulation with 2D/3D rendering and different computation backends.

The main areas explored by the project are:

* Game of Life simulation
* 3D visualization
* Parallel computation
* GPU computation
* CMake-based C++ projects
* Magnum graphics programming
* Performance measurement

---

# License

See the repository for the applicable project license.

