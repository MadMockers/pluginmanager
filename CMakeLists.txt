
cmake_minimum_required(VERSION 3.0)

add_library(pluginloader src/pluginloader.c)
target_include_directories(pluginloader
                           PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/includes
                           PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src)

add_library(plugin_interface INTERFACE)
target_include_directories(plugin_interface INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/includes)
