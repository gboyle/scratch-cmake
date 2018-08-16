
add_executable(
    project-test
    test.cpp
    test.hpp
)

target_link_libraries(project-test PRIVATE project-lib)


