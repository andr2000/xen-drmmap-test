cmake_minimum_required(VERSION 3.0)

set(PROJECT_NAME "xen-drmmap-test")

project(${PROJECT_NAME})

set(SOURCES
	modeset.c
)

include_directories(
	src
	/usr/include/libdrm
)

add_executable(${PROJECT_NAME} ${SOURCES})

target_link_libraries(${PROJECT_NAME}
	drm
)
