add_subdirectory(glad)
add_subdirectory(glfw)

# ImGui
set(IMGUI ${EXTERNAL}/imgui)
add_library(
    imgui
    ${IMGUI}/imgui.cpp
    ${IMGUI}/imgui_draw.cpp
    ${IMGUI}/imgui_widgets.cpp
    ${IMGUI}/examples/imgui_impl_opengl3.cpp
    ${IMGUI}/examples/imgui_impl_glfw.cpp
)

target_include_directories(
    imgui
    PUBLIC
    "${IMGUI}"
    "${IMGUI}/examples"
)

target_link_libraries(
    imgui
    PRIVATE
    glad
    glfw
)

