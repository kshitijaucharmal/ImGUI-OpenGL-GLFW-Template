cmake_minimum_required(VERSION 3.10)
project(ProjectName)

set(CMAKE_CXX_STANDARD 17)

# Define asset directories (Comment if not used)
add_compile_definitions(ASSET_DIR="${PROJECT_SOURCE_DIR}/assets")

# Finding installed packages
find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)

# Build glad
add_library(glad STATIC external/glad/src/glad.c)
target_include_directories(glad PUBLIC external/glad/include)

# Build ImGui
add_library(imgui
    external/imgui/imgui.cpp
    external/imgui/imgui_demo.cpp
    external/imgui/imgui_draw.cpp
    external/imgui/imgui_tables.cpp
    external/imgui/imgui_widgets.cpp
    external/imgui/backends/imgui_impl_glfw.cpp
    external/imgui/backends/imgui_impl_opengl3.cpp
)
target_include_directories(imgui PUBLIC external/imgui external/imgui/backends external/glad/include)

# Main executable
add_executable(${PROJECT_NAME} src/main.cpp)
target_include_directories(${PROJECT_NAME} PUBLIC external/glad/include)

# Link everything
target_link_libraries(${PROJECT_NAME} imgui glad glfw OpenGL::GL)

