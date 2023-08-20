project(YOUR_PROJECT_NAME VERSION 1.0 LANGUAGES C)
include(cmake/xplm.cmake)

find_xplane_sdk("SDK/dir/here" 401)
add_xplane_plugin(PLUGIN_NAME src/example.c ...)
target_link_libraries(PLUGIN_NAME xplm)
