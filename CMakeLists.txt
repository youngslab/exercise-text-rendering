
cmake_minimum_required(VERSION 3.10)

project(exercise-text-rendering)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_CURRENT_BINARY_DIR}
  ${CMAKE_CURRENT_SOURCE_DIR}/cmake)

find_package(glm REQUIRED)
find_package(glfw REQUIRED)
find_package(glad REQUIRED)
find_package(freetype REQUIRED)

add_executable(${CMAKE_PROJECT_NAME}
	src/main.cpp)

target_link_libraries(${CMAKE_PROJECT_NAME}
	glm::glm
	glfw::glfw
	glad::glad
	freetype::freetype)
