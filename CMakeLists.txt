cmake_minimum_required(VERSION 3.10)

project(imgui)
message(STATUS "Build imgui")

# Добавляем файлы исходного кода ImGui
set(IMGUI_SRC
    imgui.cpp
    imgui_draw.cpp
    imgui_tables.cpp
    imgui_widgets.cpp
    imgui_demo.cpp
)

# Создаём статическую библиотеку
add_library(imgui STATIC ${IMGUI_SRC})

# Указываем директорию с заголовочными файлами
target_include_directories(imgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
