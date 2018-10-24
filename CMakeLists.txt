cmake_minimum_required(VERSION 2.6)

# Locate GTest 
find_package(GTest REQUIRED)
include_directories(${GTEST_INCLUDE_DIRS})

# Link GTest, Pthread library
add_executable(runTest exercices/string_all_unique_char.cpp)
target_link_libraries(runTest ${GTEST_LIBRARIES} pthread)
