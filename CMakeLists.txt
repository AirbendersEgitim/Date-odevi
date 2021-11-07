cmake_minimum_required(VERSION 3.0)
project(Date)

if(MSVC)
  add_compile_options(/W4 /WX)
else()
  add_compile_options(-Wall -Wextra -pedantic -Werror)
endif()

include_directories(${CMAKE_CURRENT_SOURCE_DIR})

add_executable(test_date "test_date.cpp" "Date.cpp")
target_link_libraries(test_date)
