cmake_minimum_required(VERSION 3.24.0)

project(stb)

add_library(stb STATIC)

target_include_directories(stb
  PUBLIC
    "${CMAKE_CURRENT_SOURCE_DIR}/include"
)

target_sources(stb
  PUBLIC
    include/stb_image.h
    include/stb_truetype.h
  PRIVATE
    src/stb_image.c
    src/stb_truetype.c
)

target_compile_definitions(stb
  PUBLIC
    STBI_NO_STDIO
)
