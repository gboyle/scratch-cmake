
add_library(
    project-lib
    lib.cpp
    lib.hpp
)

target_include_directories(project-lib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})


