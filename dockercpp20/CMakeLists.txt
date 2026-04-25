cmake_minimum_required(VERSION 3.25)
project(AP)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

find_package(GTest REQUIRED)

include_directories(include/)

add_executable(main
    src/main.cpp
)

target_compile_options(main PRIVATE -fmodules-ts)

target_link_libraries(main
    GTest::GTest
    GTest::Main
)

