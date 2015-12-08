# cmake_FindCUDA
Fix for cmake FindCUDA.cmake for compilation with cufft_static

## Usage:


set(CMAKE_MODULE_PATH "${/../cmake_FindCUDA/cmake/Modules" ${CMAKE_MODULE_PATH})

find_package(CUDA REQUIRED)

set(CUDA_USE_STATIC_CUDA_RUNTIME ON)

set(CUDA_SEPARABLE_COMPILATION ON)

set(CUDA_BUILD_WITH_CUFFT_STATIC ON)
