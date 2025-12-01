cmake_minimum_required(VERSION 3.5)

project(cpp_project_template LANGUAGES CXX)

find_package(fmt CONFIG REQUIRED)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(cpp_project_template src/main.cpp)

target_link_libraries(cpp_project_template PRIVATE fmt::fmt)

install(TARGETS cpp_project_template
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR})

# Testing setup
enable_testing()
add_executable(IntegrationTests test/integration_test_driver.cpp)
get_target_property(LIBS cpp_project_template LINK_LIBRARIES)
target_link_libraries(IntegrationTests PRIVATE ${LINK_LIBRARIES})
add_test(NAME IntegrationTests COMMAND IntegrationTests)
