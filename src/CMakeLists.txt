cmake_minimum_required(VERSION 3.17)

# include(CMakePrintHelpers)
# cmake_print_properties(TARGETS glfw PROPERTIES LINK_INTERFACE_LIBRARIES )
add_executable(main main.cpp)
target_link_libraries(
    main
    PRIVATE
    glad
    glfw
)

if (APPLE)
    target_link_libraries(
        main
        PRIVATE
        apple
    )
endif()