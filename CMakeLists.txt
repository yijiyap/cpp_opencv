cmake_minimum_required(VERSION 3.10)
project(example)

set(CMAKE_CXX_STANDARD 17)
set(EXPORT_COMPILE_COMMANDS ON)

# Include OpenCV
set(OpenCV_DIR "/Users/yj/developer/build_opencv")
find_package(OpenCV 4 REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(main main.cpp)
target_link_libraries(main ${OpenCV_LIBS})