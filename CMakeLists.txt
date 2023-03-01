cmake_minimum_required(VERSION 3.10)

set_property(GLOBAL PROPERTY USE_FOLDERS ON)

set(PROJECT_NAME "stb")

project(${PROJECT_NAME} CXX)

set(SOURCES
    "stb_image_write.h"
    "stb_image.h"
    "stb_sprintf.h"
    "dummy.cpp"
)


add_library(${PROJECT_NAME} STATIC
    ${SOURCES}
)

target_include_directories(${PROJECT_NAME}
    PUBLIC
        "${CMAKE_CURRENT_SOURCE_DIR}"
)

EASE_configure_library(${PROJECT_NAME} "")

