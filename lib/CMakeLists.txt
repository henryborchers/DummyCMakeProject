set(HelloLibrary_SRC sayHi.cpp sayHi.h)
set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS 1)
add_library(HelloLibrary SHARED ${HelloLibrary_SRC})
install(TARGETS HelloLibrary
        DESTINATION lib
        INCLUDES DESTINATION include
        )