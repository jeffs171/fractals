cmake_minimum_required(VERSION 3.17)

add_executable(main main.cpp)

target_link_libraries(
    main
    PRIVATE
    glad
    glfw
    imgui
)

if (APPLE)
    target_link_libraries(
        main
        PRIVATE
        apple
    )
elseif (WIN32)
    target_link_libraries(
        main
        PRIVATE
        windows
    )
endif()
