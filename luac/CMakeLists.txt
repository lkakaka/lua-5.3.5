include_directories(../src)
link_directories(../liblua/build)
file(GLOB_RECURSE CURRENT_HEADERS ../src/*.h)
file(GLOB_RECURSE CURRENT_SRC ../src/*.c)
add_executable(luac luac.c ${CURRENT_HEADERS} ${CURRENT_SRC})
target_link_libraries(luac liblua)
