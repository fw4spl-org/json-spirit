set(JSON_TEST_SRCS
json_spirit_reader_test.cpp json_spirit_reader_test.h
json_spirit_stream_reader_test.cpp json_spirit_stream_reader_test.h
json_spirit_utils_test.cpp json_spirit_utils_test.h
json_spirit_value_test.cpp json_spirit_value_test.h
json_spirit_writer_test.cpp json_spirit_writer_test.h
utils_test.cpp utils_test.h
json_test.cpp)

find_package(Boost 1.34 REQUIRED)
include_directories(${Boost_INCLUDE_DIR})

add_executable(json_test ${JSON_TEST_SRCS})
target_link_libraries(json_test json_spirit)

