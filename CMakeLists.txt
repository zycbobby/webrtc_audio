cmake_minimum_required(VERSION 3.5)
project(webrtc_audio C)

add_definitions(-DWEBRTC_POSIX)

SET(BASEPATH "${CMAKE_SOURCE_DIR}")
include_directories("${BASEPATH}")

file(GLOB SOURCE_FILES "webrtc/common_audio/vad/*.c" "webrtc/common_audio/signal_processing/*.c")

add_library(webrtcaudio SHARED ${SOURCE_FILES})
TARGET_LINK_LIBRARIES(webrtcaudio pthread)
install(TARGETS webrtcaudio DESTINATION /usr/local/lib/)
