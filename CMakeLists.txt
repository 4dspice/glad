cmake_minimum_required(VERSION 3.12)
project(glad LANGUAGES C)

set(GLADFILES 
		src/glad.c 
		include/glad/glad.h
)

add_library(glad ${GLADFILES})

target_include_directories(glad PUBLIC include/)
target_link_libraries(glad PUBLIC ${CMAKE_DL_LIBS})
