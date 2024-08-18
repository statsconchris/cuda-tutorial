# cuda-tutorial

If you require to install nvcc in your environment, then once you activate a conda environment, proceed as follows:

```
conda install nvidia/label/cuda-12.3.0::cuda-nvcc
conda install nvidia/label/cuda-12.3.0::cuda-cudart-dev
conda install nvidia/label/cuda-12.3.0::cuda-toolkit
```
(in this example the CUDA version is 12.4)

Verify that it was properly installed. type `conda list cuda`

*All cuda packages should be 12.3. If one is higher, you may run into issues.

Typical error: 
`nvlink fatal   : Input file '/usr/lib64/libcudadevrt.a:cuda_device_runtime.o' newer than toolkit`

If versions are fine, proceed as follows:

`git clone https://github.com/NVIDIA/cuda-samples.git`

This folder has the `Common` subdirectory that contains proper helper functions.

Compile your code:

`nvcc -Icuda-samples/Common -o gpu_specs.out gpu_specs.cpp`

Run your code:

`./gpu_specs.out`

`gpu_specs.cpp` does not exist in this repo. You can use any hello-world code. For a proper example refer to the subdirectory `julia`
