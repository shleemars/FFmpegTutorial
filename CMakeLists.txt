cmake_minimum_required(VERSION 3.10)
project(FFmpegExample C)

set(CMAKE_C_STANDARD 99)

add_executable(tutorial01 tutorial01.c)
target_link_libraries(tutorial01 avcodec avformat swscale)

add_executable(tutorial02 tutorial02.c)
target_link_libraries(tutorial02 avcodec avformat swscale SDL2)

add_executable(tutorial03 tutorial03.c)
target_link_libraries(tutorial03 avcodec avformat swscale SDL2)