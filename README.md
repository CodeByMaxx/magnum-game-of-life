# Magnum Game of Life

A C/C++ implementation of **Conway's Game of Life** with 3D and 2D visualization using the [Magnum graphics engine](https://magnum.graphics/).

The project supports multiple computation modes and visualizes the simulation in real time.

## Features

* Conway's Game of Life simulation
* 3D visualization
* 2D visualization
* CPU serial computation
* CPU parallel computation
* GPU parallel computation
* Configurable simulation dimensions
* CMake-based build system
* Magnum and Corrade as the underlying C++ framework

## Technology

* **C / C++**
* **Magnum**
* **Corrade**
* **CMake**
* CPU and GPU compute modes

The project uses Magnum for visualization and Corrade for supporting utility functionality.

## Repository Structure

```text
magnum-game-of-life/
├── modules/
├── src/
├── CMakeLists.txt
├── README.md
├── Screenshot-1.png
├── Screenshot-2.png
├── Screenshot-3.png
├── Screenshot-4.png
├── Screenshot-5.png
├── Screenshot-6.png
└── Screenshot-7.png
```

The repository currently contains seven screenshots showing different simulation results.

## Dependencies

The project is based on **Magnum** and **Corrade**.

If Magnum and Corrade are not already available on your system, build **Corrade first** and then **Magnum**.

### Build Corrade

```bash
git clone https://github.com/mosra/corrade.git
cd corrade

mkdir build
cd build

cmake ..
cmake --build .
sudo cmake --install .
```

### Build Magnum

```bash
git clone https://github.com/mosra/magnum.git
cd magnum

mkdir build
cd build

cmake .. \
  -DMAGNUM_WITH_SDL2APPLICATION=ON

cmake --build .
sudo cmake --install .
```

The original project documentation also specifies building Corrade before Magnum.

## Build the Project

Clone the repository and create a build directory:

```bash
git clone https://github.com/CodeByMaxx/magnum-game-of-life.git
cd magnum-game-of-life

mkdir build
cd build

cmake ..
cmake --build .
```

The generated executables are located in the project's `bin` directory.

## Computation Modes

The application supports different computation modes:

| Mode | Description  |
| ---: | ------------ |
|  `1` | CPU Serial   |
|  `2` | CPU Parallel |
|  `3` | GPU Parallel |

The README contains benchmark output for all three modes and for both 2D and 3D simulations.

## 3D Game of Life

The 3D version can be executed with a configurable simulation dimension.

### CPU Serial

```bash
./bin/MagnumGameOfLife --dimension 32 --computemode 1
```

### CPU Parallel

```bash
./bin/MagnumGameOfLife --dimension 32 --computemode 2
```

### GPU Parallel

```bash
./bin/MagnumGameOfLife --dimension 32 --computemode 3
```

Larger dimensions can also be used, for example:

```bash
./bin/MagnumGameOfLife --dimension 64 --computemode 1
./bin/MagnumGameOfLife --dimension 64 --computemode 2
./bin/MagnumGameOfLife --dimension 64 --computemode 3
```

The existing benchmark results document measurements for dimensions `32` and `64`.

## 2D Game of Life

The project also contains a 2D version.

Example:

```bash
./bin/MagnumGameOfLife2d --dimension 512 --computemode 1
```

CPU parallel:

```bash
./bin/MagnumGameOfLife2d --dimension 512 --computemode 2
```

GPU parallel:

```bash
./bin/MagnumGameOfLife2d --dimension 512 --computemode 3
```

The current README documents benchmark results for the 2D version with a dimension of `512`.

## Screenshots

### 3D Visualization

![Game of Life 3D](Screenshot-1.png)

![Game of Life 3D](Screenshot-2.png)

![Game of Life 3D](Screenshot-3.png)

![Game of Life 3D](Screenshot-4.png)

### Additional Results

![Game of Life](Screenshot-5.png)

![Game of Life](Screenshot-6.png)

![Game of Life](Screenshot-7.png)

All seven referenced screenshot files are currently present in the repository.

## Benchmarking

The application prints computation times for the selected computation mode.

Example output:

```text
Computing took 0.00742187s with mode: CPUSerial
Computing took 0.00565313s with mode: CPUSerial
Computing took 0.00172155s with mode: CPUParallel
```

The exact execution times depend on the hardware and runtime environment. The values above are examples from the project's existing benchmark output.

## Project Structure

The project is organized around:

* `src/` — application and simulation source code
* `modules/` — project modules
* `CMakeLists.txt` — CMake build configuration
* `Screenshot-*.png` — example visualizations
* `README.md` — project documentation

## About the Project

This project was created to explore **Conway's Game of Life** in a 3D environment while comparing different approaches to computing the simulation.

The combination of Magnum visualization with serial CPU, parallel CPU, and GPU computation makes it possible to experiment with both graphical rendering and simulation performance.

## License

No license file is currently listed in the repository root. If this project is intended to be reused as open-source software, add an appropriate `LICENSE` file to the repository.

