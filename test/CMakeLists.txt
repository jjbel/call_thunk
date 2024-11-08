cmake_minimum_required(VERSION 3.10)
add_executable(call_thunk_test test_call.cpp)
target_link_libraries(call_thunk_test PUBLIC call_thunk)
