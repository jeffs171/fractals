add_subdirectory(${EXTERNAL}/glad)
add_subdirectory(${EXTERNAL}/glfw)

# Uncomment if you want a dedicated imgui project
# project(imgui)
# set(IMGUI_ROOT ${CMAKE_CURRENT_SOURCE_DIR}/imgui )
# set(IMGUI_SOURCES "${IMGUI_ROOT}/*.cpp"; "${IMGUI_ROOT}/examples/imgui_impl_glfw.cpp"; "${IMGUI_ROOT}/examples/imgui_impl_opengl3.cpp" CACHE INTERNAL "ImGui Source List")
# set(IMGUI_HEADERS "${IMGUI_ROOT}/*.h"; "${IMGUI_ROOT}/examples/imgui_impl_glfw.h"; "${IMGUI_ROOT}/examples/imgui_impl_opengl3.h" CACHE INTERNAL "ImGui Header List")
# file(GLOB SOURCES "${IMGUI_SOURCES}")
# file(GLOB HEADERS "${IMGUI_HEADERS}")
# add_library(imgui ${SOURCES} ${HEADERS})
