cmake_minimum_required(VERSION 3.11)

project(project VERSION 0.0.1)

if (MSVC)
    # Microsoft prepoluates settings making it painful to change
    string (REGEX REPLACE "/W[0-4]" "" CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}")
endif()

if(MSVC)
	set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /W4")
else(MSVC)
	set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -Wpedantic -Werror -std=c++14")
endif(MSVC)



add_subdirectory(project-lib)
add_subdirectory(project-test)
add_subdirectory(project-tool)

enable_testing()
add_test(NAME tester42 COMMAND project-test)