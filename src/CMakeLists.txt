set(SOURCE_FILES main.cpp)
include_directories(${CMAKE_SOURCE_DIR}/lib)
add_executable(cmakeLibrary ${SOURCE_FILES})
target_link_libraries(cmakeLibrary hello)