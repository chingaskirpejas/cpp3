cmake_minimum_required(VERSION 3.26)
project(zuba)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -static-libstdc++ -static-libgcc")
add_executable(zuba
        main.cpp
        functions.cpp
        read_from_file.cpp
        file_generator.cpp
        list_test.cpp
)

target_include_directories(zuba PRIVATE
        ${CMAKE_CURRENT_SOURCE_DIR}
)

# O1 optimizacijos lygis
target_compile_options(zuba PRIVATE -O3)