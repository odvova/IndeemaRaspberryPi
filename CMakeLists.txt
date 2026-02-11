cmake_minimum_required(VERSION 3.10.0)
project(IndeemaRaspberryPi VERSION 0.1.0 LANGUAGES C CXX)

# add_subdirectory: "Go into that folder and learn how to build the common target."
add_subdirectory(common)

# tells the linker to "bake" the code from common into app.
add_executable(IndeemaRaspberryPi main.cpp)

target_link_libraries(IndeemaRaspberryPi PRIVATE common)

target_include_directories(IndeemaRaspberryPi PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/common/include)



