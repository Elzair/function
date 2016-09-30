cmake_minimum_required(VERSION 3.3)

project(boost_function)

add_library(boost_function INTERFACE)

target_include_directories(boost_function BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

install(TARGETS boost_function DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::function ALIAS boost_function)
