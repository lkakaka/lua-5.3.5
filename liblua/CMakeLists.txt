
add_definitions(-DLUA_BUILD_AS_DLL)
if(NOT WIN32)
add_definitions(-DLUA_USE_DLOPEN)
endif()

file(GLOB_RECURSE CURRENT_HEADERS ../src/*.h)
file(GLOB_RECURSE CURRENT_SRC ../src/*.c)

add_library(liblua SHARED ${CURRENT_HEADERS} ${CURRENT_SRC})
if(NOT WIN32)
target_link_libraries(liblua -lm dl)
endif()
