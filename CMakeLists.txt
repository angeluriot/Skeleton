cmake_minimum_required(VERSION 3.10)

# Project
project(App)

# Sources
file(GLOB_RECURSE SOURCES sources/*.cpp)
file(GLOB_RECURSE HEADERS includes/*.hpp includes/*.h)

# Executable
add_executable(${PROJECT_NAME} ${SOURCES} ${HEADERS})

# C++ 17
set_target_properties(${PROJECT_NAME} PROPERTIES CXX_STANDARD 17 CXX_STANDARD_REQUIRED ON)

# Includes
target_include_directories(${PROJECT_NAME} PUBLIC includes)

# Set VS properties
if(MSVC)
	target_compile_options(${PROJECT_NAME} PUBLIC "/Zc:__cplusplus")
	set_target_properties(${PROJECT_NAME} PROPERTIES VS_DEBUGGER_WORKING_DIRECTORY "${CMAKE_SOURCE_DIR}")
	set_property(DIRECTORY ${CMAKE_CURRENT_BINARY_DIR} PROPERTY VS_STARTUP_PROJECT ${PROJECT_NAME})
endif()
