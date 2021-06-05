project(SLAM)
cmake_minimum_required(VERSION 2.8)
MESSAGE(STATUS "This is BINART dir" ${PROJECT_BINARY_DIR})
MESSAGE(STATUS "This is SOURCE dir" ${PROJECT_SOURCE_DIR})

add_library(hello SHARED 
src/hello.cpp
)

include_directories(${PROJECT_SOURCE_DIR}/include)

add_executable(say_hello src/useHello.cpp)

target_link_libraries(say_hello hello)
