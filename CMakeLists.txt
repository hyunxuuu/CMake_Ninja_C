cmake_minimum_required(VERSION 3.10)

set(CMAKE_C_COMPILER gcc)

project(CMake_Ninja_C)

file(GLOB SRC_FILES
    "${CMAKE_CURRENT_SOURCE_DIR}/main.c"
)

add_executable(${PROJECT_NAME}
    ${SRC_FILES}
)

target_include_directories(${PROJECT_NAME} PRIVATE
    "${CMAKE_CURRENT_SOURCE_DIR}"
)
