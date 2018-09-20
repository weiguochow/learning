right click source file, add new item - kernel.cu
right click the project, build dependencies - build costomizations. check CUDA
right click kernel.cu, properties - general - item type - CUDA C/C++
project - properties - linker - input - additional dependencies - add cudart_static.lib
