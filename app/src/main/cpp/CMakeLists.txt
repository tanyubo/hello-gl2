cmake_minimum_required(VERSION 3.4.1)

# now build app's shared lib
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++17 -Wall")


include_directories( ./include ./include/glm)

add_library(gl2jni SHARED
            gl_code.cpp)


# add lib dependencies
target_link_libraries(gl2jni
                      log
                      EGL
                      GLESv3)

