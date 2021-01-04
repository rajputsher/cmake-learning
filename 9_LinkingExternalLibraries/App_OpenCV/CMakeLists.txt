cmake_minimum_required(VERSION 3.0.0)
project(DisplayImage)

find_package(OpenCV REQUIRED)   # REQUIRED keyword tells that this package is mandatory and not an optional one.

add_executable(DisplayImage main.cpp)

#OpenCV package provides various libraries and thes are not in the form of a .a or .so file format.
#Rather, they are stored in a variable and that variable is set in the OpenCV-config.cmake file.

#Commonly followed practice in the communities
#Package Name : XYZ 
#Libraries will be in variables: XYZ_LIBRARIES, XYZ_LIBS, ...
#Include Directories: XYZ_INCLUDES, XYZ_INCLUDE_DIRS,...



target_include_directories(DisplayImage PRIVATE ${OpenCV_INCLUDE_DIRS})
target_link_libraries(DisplayImage PRIVATE ${OpenCV_LIBS})

message("OpenCV Include Directories: " ${OpenCV_INCLUDE_DIRS})
message("OpenCV Libraries: " ${OpenCV_LIBS})
