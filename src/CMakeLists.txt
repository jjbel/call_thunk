cmake_minimum_required(VERSION 3.10)

project(call_thunk VERSION 1.0.0 LANGUAGES CXX)

add_library(call_thunk call_thunk.h call_thunk.cpp)
target_compile_features(call_thunk PRIVATE cxx_std_11)

# TODO needed?
target_include_directories(call_thunk PUBLIC "${CMAKE_CURRENT_LIST_DIR}")

install(
    TARGETS call_thunk
    RUNTIME DESTINATION bin
    LIBRARY DESTINATION lib
    ARCHIVE DESTINATION lib
)

install(
    DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/call_thunk" # source directory
    DESTINATION "include" # target directory
    FILES_MATCHING # install only matched files
    PATTERN "*.h" # select header files
)
