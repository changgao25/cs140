cmake_minimum_required(VERSION 3.22)

project(EX01-HelloWorld)

set(EXEC_NAME "HelloWorld")
set(TEST_EXEC_NAME "helloworld_unittest")
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_FLAGS "-Wall -Wextra -Werror -pedantic")

add_executable(
        ${EXEC_NAME}
        src/main.cc
)

# from https://github.com/google/googletest/tree/main/googletest#incorporating-into-an-existing-cmake-project
# and https://google.github.io/googletest/quickstart-cmake.html
include(FetchContent)
FetchContent_Declare(
        googletest
        # Specify the commit you depend on and update it regularly.
        URL https://github.com/google/googletest/archive/5376968f6948923e2411081fd9372e71a59d8e77.zip
)
# For Windows: Prevent overriding the parent project's compiler/linker settings
set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)
FetchContent_MakeAvailable(googletest)

enable_testing()

add_executable(
        ${TEST_EXEC_NAME}
        src/${TEST_EXEC_NAME}.cc  # sort of a hack to have fewer things to change between projects.
)
add_dependencies(
        ${TEST_EXEC_NAME}
        ${EXEC_NAME}
)
target_link_libraries(
        ${TEST_EXEC_NAME}
        GTest::gtest_main
)

include(GoogleTest)
gtest_discover_tests(${TEST_EXEC_NAME})
