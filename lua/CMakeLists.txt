
include_directories(../src)
link_directories(../lib/build)
add_executable(lua lua.c)
target_link_libraries(lua liblua)

