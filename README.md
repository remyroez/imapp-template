# imapp-template

A CMake template project and example for standalone application using [Dear ImGui](https://github.com/ocornut/imgui) and [imapp](https://github.com/remyroez/imapp).

## Building

### Basic

```sh
mkdir build
cd build
cmake ..
make
./imapp_example
```

### Select Platfrom/Renderer(+OpenGL Loader)

```sh
cmake .. -DIMAPP_PLATFORM=SDL2 -DIMAPP_RENDERER=OpenGL3 -DIMAPP_OPENGL_LOADER=GLEW
```

Several CMake options(case-insensitive) are provided:

- `IMAPP_PLATFORM`
    - `SDL2` (default)
    - `glfw`
- `IMAPP_RENDERER`
    - `OpenGL3` (default)
    - `OpenGL2`
    - `Vulkan`
- `IMAPP_OPENGL_LOADER`
    - `GLEW` (default)
    - `GL3W`
    - `GLAD` (not tested)
    - `glbinding2`
    - `glbinding3` (not tested)

### Emscripten

```sh
mkdir build_emscripten
cd build_emscripten
emcmake cmake ..
emmake make
python3 -m http.server
```

The platform is fixed to SDL2 and the renderer is fixed to OpenGL3.

## Third party

- [Dear ImGui](https://github.com/ocornut/imgui)
- [SDL2 CMake modules](https://github.com/aminosbh/sdl2-cmake-modules)
- [imapp](https://github.com/remyroez/imapp) (base repo)

## License

MIT License
