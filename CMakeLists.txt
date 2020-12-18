cmake_minimum_required(VERSION 3.8)

project(test_ffmpeg)

# 找到ffmpeg的位置
# 设置头文件查找目录
include_directories("/usr/local/Cellar/ffmpeg/4.2.1_1/include")

# 设置库文件查找目录
link_directories("/usr/local/Cellar/ffmpeg/4.2.1_1/lib")

add_executable(hello_ffmpeg src/hello_ffmpeg.cpp)

target_link_libraries(hello_ffmpeg avutil avcodec avfilter  avdevice avformat postproc swresample)