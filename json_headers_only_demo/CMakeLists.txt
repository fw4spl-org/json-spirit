set(JSON_HEADERS_ONLY_DEMO_SRCS
json_headers_only_demo.cpp)

find_package(Boost 1.34 REQUIRED)
include_directories(${Boost_INCLUDE_DIR})

add_executable(json_headers_only_demo ${JSON_HEADERS_ONLY_DEMO_SRCS})
target_link_libraries(json_headers_only_demo json_spirit)

