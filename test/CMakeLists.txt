project(test)

add_subdirectory(google_test)
include_directories(${gtest_SOURCE_DIR}/include ${gtest_SOURCE_DIR})

add_executable(google_test_run list_test.cpp avl_tree_test.cpp utility_test.cpp)
target_include_directories(google_test_run PRIVATE ../include)
target_link_libraries(google_test_run gtest gtest_main)
target_compile_options(google_test_run PRIVATE -Wthread-safety)

add_test(Test google_test_run)
enable_testing()