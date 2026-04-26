## Overview
The provided project is a simple implementation of the Pythagoras Tree using C programming. The tree is rendered in an interactive window, allowing users to observe its structure and properties.

## Features
- **Pythagoras Tree Rendering**: The core functionality involves rendering a fractal tree using geometric principles.
- **Interactive Window**: The application runs in a graphical window, allowing for real-time interaction with the rendered tree.
- **Performance Metrics**: Displays the time taken for rendering and the number of iterations performed.

## Project Structure
The project consists of several files and directories as follows:

### Prerequisites
- **C/C++ Compiler**: GCC is required for both Linux and Windows builds. For WebAssembly, Emscripten is used.
- **Make Utility**: To build the project, Make is essential.
- **Development Tools**: Standard development tools such as text editors or IDEs (like Visual Studio Code) are recommended.

## Build & Run
### Building the Project

#### Linux
To build the project on a Linux system, use the following commands:
```sh
cd <Project>
make -f Makefile.linux all
```

#### Windows
For Windows, the process is similar:
```sh
cd <Project>
make -f Makefile.windows all
```

#### Wine (Cross-compile for Windows)
To cross-compile the project for Windows using Wine on Linux, use these commands:
```sh
cd <Project>
make -f Makefile.wine all
```

#### WebAssembly
For building a WebAssembly version using Emscripten, run:
```sh
cd <Project>
make -f Makefile.web all
```
To execute the WebAssembly build in a local server, use:
```sh
make -f Makefile.web exe
```

### Executing the Project

- After a successful build, the executable can be found in the `build/` directory.
- To run the application, simply execute the file from the command line. For example:
  ```sh
  ./build/Main.exe  # For Windows or Linux
  ```
  ```sh
  emrun --no_browser --port 8080 build/index.html  # For WebAssembly
  ```

- The project can be rebuilt with additional options such as debugging information using `make -f Makefile.(os) alldebug` and running the debugger with `make -f Makefile.(os) debug`.