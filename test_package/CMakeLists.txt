cmake_minimum_required(VERSION 3.12)
project(test_package CXX)

find_package(eve REQUIRED CONFIG)

add_executable(${PROJECT_NAME} test_package.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE eve::eve)
target_compile_features(${PROJECT_NAME} PRIVATE cxx_std_20)