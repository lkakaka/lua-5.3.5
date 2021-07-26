
add_definitions(-DLUA_BUILD_AS_DLL -DLUA_USE_DLOPEN)

file(GLOB_RECURSE CURRENT_HEADERS ../src/*.h)
file(GLOB_RECURSE CURRENT_SRC ../src/*.c)

add_library(liblua SHARED ${CURRENT_HEADERS} ${CURRENT_SRC})
target_link_libraries(liblua -lm dl)
