set(Hello_SRC sayHi.cpp sayHi.h)
set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS 1)
add_library(hello SHARED ${Hello_SRC})
