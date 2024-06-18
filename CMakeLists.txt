# Minimum version can be no higher than 3.5 as Ubuntu package management uses this version.
cmake_minimum_required(VERSION 3.5)

project (EX01-HelloWorld)

set(SOURCE_PREFIX "helloworld")
set(EXEC_NAME "HelloWorld")
set(CMAKE_CXX_STANDARD 11)

if(EXISTS ${CMAKE_HOME_DIRECTORY}/csv30-lib/CMakeLists.txt)
    include(csv30-lib/CMakeLists.txt)
    add_dependencies(${EXEC_NAME}_GTest ${EXEC_NAME})
elseif(EXISTS /usr/local/csv30-lib/CMakeLists.txt)
    include(/usr/local/csv30-lib/CMakeLists.txt)
    add_dependencies(${EXEC_NAME}_GTest ${EXEC_NAME})
else()
    add_custom_target(add-submodules ALL git clone https://github.com/vc-csv30/csv30-lib.git)
endif()