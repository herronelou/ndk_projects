cmake_minimum_required(VERSION 3.10 FATAL_ERROR)
project(WildcardChannels)

set(CMAKE_MODULE_PATH "CMake;${CMAKE_MODULE_PATH}")

find_package(Nuke REQUIRED)


function(add_example_plugin PLUGIN_NAME)
    add_nuke_plugin(${PLUGIN_NAME} ${ARGN})
    # target_compile_definitions(${PLUGIN_NAME} PRIVATE FN_EXAMPLE_PLUGIN)
endfunction()


add_example_plugin(WildcardChannels WildcardChannels.cpp)
