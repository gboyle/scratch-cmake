
add_executable(
    project-tool
    main.cpp
)

target_link_libraries(project-tool PRIVATE project-lib)