cmake_minimum_required (VERSION 2.8)


# Custom modules
set (CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_CURRENT_SOURCE_DIR}/platform/cmake")


# Platform
include (platform)
initialize_platform ()


# Install
include (platform/install)


# Tests
include (platform/tests)
add_project_tests_main_target ()


# Documentation
include (platform/doxygen)
add_project_documentation_main_target ()


# 3rdparty
add_subdirectory (platform)
add_subdirectory (brolly)
add_subdirectory (efc)
add_subdirectory (lvfs)
