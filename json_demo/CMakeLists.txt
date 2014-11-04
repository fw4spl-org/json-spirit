set(JSON_DEMO_SRCS
json_demo.cpp)

find_package(Boost 1.34 REQUIRED)
include_directories(${Boost_INCLUDE_DIR})

add_executable(json_demo ${JSON_DEMO_SRCS})
target_link_libraries(json_demo json_spirit)

