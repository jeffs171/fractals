cmake_minimum_required(VERSION 3.17)

# include(CMakePrintHelpers)
# cmake_print_properties(TARGETS glfw PROPERTIES LINK_INTERFACE_LIBRARIES )

file(GLOB_RECURSE SOURCES "${CMAKE_CURRENT_SOURCE_DIR}/*.cpp")
file(GLOB_RECURSE HEADERS "${CMAKE_CURRENT_SOURCE_DIR}/*.h" "${CMAKE_CURRENT_SOURCE_DIR}/*.hpp")

file(GLOB IMGUI_SOURCES "${EXTERNAL}/imgui/*.cpp" "${EXTERNAL}/imgui/examples/imgui_impl_glfw.cpp" "${EXTERNAL}/imgui/examples/imgui_impl_opengl3.cpp")
file(GLOB IMGUI_HEADERS "${EXTERNAL}/imgui/*.h" "${EXTERNAL}/imgui/examples/imgui_impl_glfw.h" "${EXTERNAL}/imgui/examples/imgui_impl_opengl3.h")

add_executable(main ${SOURCES} ${HEADERS} ${IMGUI_SOURCES} ${IMGUI_HEADERS})

target_link_libraries(
    main
    PRIVATE
    glad
    glfw
)
target_include_directories(
	main
	PRIVATE
	${EXTERNAL}/imgui
	${EXTERNAL}/imgui/examples
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
