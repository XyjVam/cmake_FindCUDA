project(MyProject)
cmake_minimum_required (VERSION 2.8)

set(CUDA_TOOLKIT_ROOT_DIR "/usr/local/cuda/")

set(CMAKE_MODULE_PATH "${PROJECT_SOURCE_DIR}/cmake_FindCUDA/cmake/Modules" ${CMAKE_MODULE_PATH})
find_package(CUDA)
set(CUDA_USE_STATIC_CUDA_RUNTIME ON)
set(CUDA_SEPARABLE_COMPILATION ON)
set(CUDA_BUILD_WITH_CUFFT_STATIC ON)
#include_directories(${PROJECT_SOURCE_DIR}/../../../NVIDIA_CUDA-7.0_Samples/common/inc)
#message("-- CUDA_LIBRARIES: ${CUDA_LIBRARIES}")
CUDA_ADD_EXECUTABLE(
  ${CMAKE_PROJECT_NAME}
  file1.cu
  file2.cu
  )
