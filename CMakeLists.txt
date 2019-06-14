cmake_minimum_required(VERSION 3.1 FATAL_ERROR)
project(mnist)

set(Torch_DIR C:/Users/krshr/Downloads/libtorch/libtorch/share/cmake/Torch/)
set(CMAKE_PREFIX_PATH C:/Users/krshr/Downloads/libtorch/libtorch)
find_package(Torch REQUIRED)

add_executable(mnist main.cpp)
target_compile_features(mnist PUBLIC cxx_range_for)
target_link_libraries(mnist ${TORCH_LIBRARIES})
