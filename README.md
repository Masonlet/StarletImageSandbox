# Starlet Image Sandbox

[![C++20](https://img.shields.io/badge/C%2B%2B-20-blue.svg)](https://isocpp.org/std/the-standard)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

A C++ playground for experimenting with images loaded using **Starlet Serializer.**

## Features

- Supported Image Formats: **BMP**, **TGA**

- Output to **Console ASCII**

![Example](./images/skull.png)

- Output to **Coloured Console ASCII**

![Colour Example](./images/skull_colour.png)

## Usage
```bash
# Basic usage
./starlet-image-sandbox

# Specify an image file
./starlet-image-sandbox -p path/to/image

# Adjust ASCII scaling
./starlet-image-sandbox -x 8 -y 16

# Use coloured output mode
./starlet-image-sandbox -m ascii_colour

# Custom ASCII gradient
./starlet-image-sandbox -g " .:-=+*#%@"
```

### Options:
- `--help, -h` - Show help message
- `--path, -p <path>` - Image file path (default: beetle.tga)
- `--scale-x, -x <int>` - Horizontal scaling factor (default: 16)
- `--scale-y, -y <int>` - Vertical scaling factor (default: 32)
- `--gradient, -g <str>` - ASCII gradient string (default: '@%#*+=-:. ')
- `--mode, -m <mode>` - Output mode: `ascii` or `ascii_colour` (default: ascii)

## Dependencies
- [starlet-serializer](https://github.com/starlet-libs/serializer) (auto-fetched)

## Prerequisites
- C++20 compatible compiler
- One of the following Build Systems,
    - CMake 3.14+
    - Meson 1.1+

## Building the Project
```bash
git clone https://github.com/masonlet/starlet-image-sandbox.git
cd starlet-image-sandbox
```

### CMake
```bash
cmake -B build
cmake --build build
```

### Meson
```bash
meson setup build
meson compile -C build
```
