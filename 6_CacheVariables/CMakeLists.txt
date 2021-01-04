cmake_minimum_required(VERSION 3.0.0)

project(Calculator_Project VERSION 1.0.0)

add_subdirectory(my_math)
add_subdirectory(my_print)

add_executable(calculator main.cpp)

target_link_libraries(calculator my_math my_print)

#set(A "123" CACHE STRING "This command sets variable A in persistent cache")
#message($CACHE{A})


#set(Name Alice CACHE STRING "The name variable")
#set(Name Bob CACHE STRING "The modified name variable" FORCE)
#message($CACHE{Name})

#message(CMAKE_VERSION=${CMAKE_VERSION})
#message(CMAKE_MAJOR_VERSION=${CMAKE_MAJOR_VERSION})
#message(CMAKE_MINOR_VERSION=${CMAKE_MINOR_VERSION})
#message(CMAKE_PATCH_VERSION=${CMAKE_PATCH_VERSION})

#message("RootLevel: CMAKE_PROJECT_NAME=${CMAKE_PROJECT_NAME}")
#message("RootLevel: PROJECT_NAME=${PROJECT_NAME} ")


