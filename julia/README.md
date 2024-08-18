# How to run the julia file

Access your node:

- `import module nvidia`
- `nvcc --version`

Verify that nvcc is installed.

Compile the code:

`nvcc -o julia_gpu.out julia_gpu.cu  -lGLEW -lglut -lGLU -lGL`

If you are in a cluster and need permission to access a GPU, then, e.g., create an interactive job (OpenGL should be installed to see the graphics) and run the code, e.g., `./julia_gpu.out`
