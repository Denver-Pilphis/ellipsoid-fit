CMAKE_MINIMUM_REQUIRED(VERSION 3.0.0)

PROJECT(ellipsoid-fit)

find_package(EIGEN3 REQUIRED)
include_directories(
    ${EIGEN3_INCLUDE_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}/include/ellipsoid_fit
)

add_definitions(-D_USE_MATH_DEFINES)

file(GLOB SRC_LIST "src/ellipsoid_fit/*.cpp")
add_library(ellipsoid-fit SHARED ${SRC_LIST})