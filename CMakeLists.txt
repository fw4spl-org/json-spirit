cmake_minimum_required(VERSION 2.6)

project(json_spirit)

option(BUILD_LIB  "Build json-spirit library" OFF)
option(BUILD_DEMO "Build json-spirit demo"    OFF)
option(BUILD_TEST "Build json-spirit test"    OFF)

include_directories(json_spirit)

if(BUILD_LIB)
    add_subdirectory(json_spirit)
endif()

if(BUILD_TEST)
    add_subdirectory(json_test)
endif()

if(BUILD_DEMO)
    add_subdirectory(json_demo)
    add_subdirectory(json_headers_only_demo)
    add_subdirectory(json_map_demo)
endif()

install(
  FILES
  ${CMAKE_SOURCE_DIR}/json_spirit/json_spirit.h
  ${CMAKE_SOURCE_DIR}/json_spirit/json_spirit_error_position.h
  ${CMAKE_SOURCE_DIR}/json_spirit/json_spirit_reader.h
  ${CMAKE_SOURCE_DIR}/json_spirit/json_spirit_reader_template.h
  ${CMAKE_SOURCE_DIR}/json_spirit/json_spirit_stream_reader.h
  ${CMAKE_SOURCE_DIR}/json_spirit/json_spirit_utils.h
  ${CMAKE_SOURCE_DIR}/json_spirit/json_spirit_value.h
  ${CMAKE_SOURCE_DIR}/json_spirit/json_spirit_writer.h
  ${CMAKE_SOURCE_DIR}/json_spirit/json_spirit_writer_template.h
  ${CMAKE_SOURCE_DIR}/json_spirit/json_spirit_writer_options.h
  DESTINATION include/json_spirit)

