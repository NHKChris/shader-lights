#PROJECT NAME
project(shader-lights)
cmake_minimum_required(VERSION 2.8)

#EXTERNAL PACKAGES (IRRLICHT)
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/Modules/")
find_package(Irrlicht REQUIRED)

#INCLUDES & SRC FILES
include_directories(
    ${PROJECT_SOURCE_DIR}/include
)

file(GLOB SRCS src/*.cpp)
file(GLOB HDRS include/*.h)

#LINKING AND EXECUTABLE
add_executable(${PROJECT_NAME} ${SRCS} ${HDRS})
target_link_libraries(${PROJECT_NAME} ${IRRLICHT_LIBRARIES})
