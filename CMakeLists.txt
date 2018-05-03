cmake_minimum_required(VERSION 3.6)

project(experimental)

set(CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/cmake/modules)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)
#set(CMAKE_VERBOSE_MAKEFILE ON)

find_package(ClangTools)
if(CLANG_TIDY_FOUND)
    set(CMAKE_CXX_CLANG_TIDY "${CLANG_TIDY_BIN};-checks=*, -fuchsia*, -google*")
else(CLANG_TIDY_FOUND)
    message(STATUS "${Red}clang-tidy not found. Static analysis won't be done.${ColourReset}")
endif(CLANG_TIDY_FOUND)

add_subdirectory(third_party)

