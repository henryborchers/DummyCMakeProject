cmake_minimum_required(VERSION 3.6)
project(cmakeLibrary)

set(CMAKE_CXX_STANDARD 11)

set(HelloLibrary_MAJOR_VERSION 0)
set(HelloLibrary_MINOR_VERSION 1)
set(HelloLibrary_PATCH_VERSION 0)
set(HelloLibrary_VERSION
  ${HelloLibrary_MAJOR_VERSION}.${HELLO_MINOR_VERSION}.${HELLO_PATCH_VERSION})

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib")
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib")

set(INSTALL_LIB_DIR lib CACHE PATH "Installation directory for libraries")
set(INSTALL_BIN_DIR bin CACHE PATH "Installation directory for executables")


add_subdirectory(lib)
add_subdirectory(src)



export(TARGETS HelloLibrary
  FILE "${PROJECT_BINARY_DIR}/HelloTargets.cmake")

export(PACKAGE HelloLibrary)
