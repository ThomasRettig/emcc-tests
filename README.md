# EMCC tests
The code here is an experiment which uses the [Simple DirectMedia Layer](https://www.libsdl.org/) API to interact with the HTML `<canvas>` element via WebAssembly. The C++ source code comes from the official [Emscripten repo](https://github.com/emscripten-core/emscripten/blob/main/tests/hello_world_sdl.cpp) with some minor modifications, such as the removal of console logs.

View the live website here: https://emscripten.netlify.app/

## Building
If you’ve modified the C++ source code, please follow the steps below in order to generate the WASM binary and Javascript glue code. You need to have Emscripten installed on your machine. Visit the [official docs](https://emscripten.org/docs/getting_started/downloads.html) for more details.
```shell
$ emcc -oz canvas.cpp -o canvas.wasm
$ emcc -oz canvas.cpp -o canvas.js
```
