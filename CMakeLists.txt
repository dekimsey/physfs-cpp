cmake_minimum_required(VERSION 2.6)


project(PhysFS++)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${PROJECT_BINARY_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${PROJECT_BINARY_DIR}/lib)

option(BUILD_SHARED_LIBS "Build as shared library?" NO)

include_directories(include)
add_subdirectory(src)

install(DIRECTORY include DESTINATION .)
