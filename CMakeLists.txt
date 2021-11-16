
cmake_minimum_required(VERSION 3.5)

project(GitZeroTrust)

include(conanbuildinfo.cmake)

conan_basic_setup()

set (CMAKE_LIBRARY_OUTPUT_DIRECTORY $(PROJECT_BINARY_DIR)/bin)

add_executable(gzt
	src/main.cpp
)

target_include_directories(gzt PRIVATE include/)

target_link_libraries(gzt PRIVATE ${CONAN_LIBS})

