cmake_minimum_required(VERSION 2.8.3)
project(asr_rapidxml)

include_directories(include)

find_package(catkin)

catkin_package(
  INCLUDE_DIRS include 
  LIBRARIES ${PROJECT_NAME}
)

add_library(${PROJECT_NAME} STATIC     
    include/rapidxml.hpp
    include/rapidxml_iterators.hpp
    include/rapidxml_print.hpp
    include/rapidxml_print.hpp)
set_target_properties(${PROJECT_NAME} PROPERTIES LINKER_LANGUAGE CXX)
