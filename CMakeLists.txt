cmake_minimum_required(VERSION 3.5)

project(cpp_project_template LANGUAGES CXX)

find_package(fmt CONFIG REQUIRED)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(cpp_project_template src/main.cpp)

target_link_libraries(cpp_project_template PRIVATE fmt::fmt)

install(TARGETS cpp_project_template
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR})
