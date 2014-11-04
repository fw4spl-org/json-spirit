SET(JSON_MAP_DEMO_SRCS
json_map_demo.cpp)

find_package(Boost 1.34 REQUIRED)
include_directories(${Boost_INCLUDE_DIR})

add_executable(json_map_demo ${JSON_MAP_DEMO_SRCS})
target_link_libraries(json_map_demo json_spirit)

