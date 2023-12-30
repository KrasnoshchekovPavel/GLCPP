cmake_minimum_required(VERSION 3.13 FATAL_ERROR)

project(GLCPP)

add_executable(glcpp main.cpp)

#GLFW предустанавливаем параметры
set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw) #в этой папке ищется cmakelists и импортируется сюда
target_link_libraries(glcpp glfw) #glfw - создан с помощью add_library в glfw/cmakelists.txt




