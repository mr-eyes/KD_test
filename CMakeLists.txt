cmake_minimum_required (VERSION 3.4)
project (KD_Test C CXX)

set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++14 -fopenmp")

add_subdirectory(kmerDecoder)
add_subdirectory(genericDecoder)

add_executable (kdtest ${CMAKE_CURRENT_SOURCE_DIR}/main.cpp)

target_link_libraries(kdtest kmerDecoder)
target_link_libraries(kdtest genericDecoder)
