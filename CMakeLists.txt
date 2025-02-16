cmake_minimum_required(VERSION 3.10)
project(MyProject C)

# Set the C standard (change if needed)
set(CMAKE_C_STANDARD 99)

# Include the directory where your header files are located.
include_directories(${CMAKE_SOURCE_DIR}/serviceHeader)

# Collect all .c files from serviceSource folder
file(GLOB SERVICE_SOURCES ${CMAKE_SOURCE_DIR}/serviceSource/*.c)

# Add the executable using main.c and all service source files.
add_executable(MyExecutable main.c ${SERVICE_SOURCES})
