cmake_minimum_required(VERSION 3.10)

project(HelloWorld CXX)

# Genera el ejecutable a partir del código fuente
add_executable(hello_world main.cpp)

# En Linux generamos un ejecutable estático
if(UNIX AND NOT APPLE)
    target_link_options(hello_world PRIVATE -static)
endif()
