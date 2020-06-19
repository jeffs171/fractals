# fractals

## Dependencies
1. CMake 3.17
2. GLAD
3. GLFW

## Directory
The folder structure here should follow:
```
fractals/
├── build/ 
├── cmake/
├── src/
├── third_party/
```

## Setup
1. Get GLAD from https://glad.dav1d.de/
2. Get GLFW from https://www.glfw.org/download.html
3. Place them in the third_party directory as per the instructions in third_party/README.md
4. Make a new folder called `build` 
5. `cmake ..`
6. `cmake --build ./ --target main`
7. `./src/main`