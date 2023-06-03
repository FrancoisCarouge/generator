# Copyright Lewis Baker, Corentin Jabot
# Licensed under Boost Software License 1.0

cmake_minimum_required(VERSION 3.12)

project(stdgenerator
    LANGUAGES CXX
    VERSION 0.1)

include(CMakePackageConfigHelpers)
include(CPack)
include(CTest)
include(GNUInstallDirs)

add_subdirectory("cmake")
add_subdirectory("include")
add_subdirectory("tests")
