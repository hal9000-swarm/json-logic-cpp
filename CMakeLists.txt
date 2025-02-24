cmake_minimum_required(VERSION 3.18)
project(jsonlogic VERSION 0.1 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)

include_directories(
        lib/json/single_include/nlohmann

        src
)

add_library(
        ${PROJECT_NAME}

        src/json_logic.cpp

        src/operations/array/all.cpp
        src/operations/array/filter.cpp
        src/operations/array/in.cpp
        src/operations/array/map.cpp
        src/operations/array/merge.cpp
        src/operations/array/none.cpp
        src/operations/array/reduce.cpp
        src/operations/array/some.cpp
        src/operations/data/missing.cpp
        src/operations/data/missing_some.cpp
        src/operations/data/var.cpp
        src/operations/logic/and.cpp
        src/operations/logic/different.cpp
        src/operations/logic/equal.cpp
        src/operations/logic/if.cpp
        src/operations/logic/not.cpp
        src/operations/logic/or.cpp
        src/operations/logic/truthy.cpp
        src/operations/misc/log.cpp
        src/operations/numeric/addition.cpp
        src/operations/numeric/division.cpp
        src/operations/numeric/gt.cpp
        src/operations/numeric/gte.cpp
        src/operations/numeric/lt.cpp
        src/operations/numeric/lte.cpp
        src/operations/numeric/max.cpp
        src/operations/numeric/min.cpp
        src/operations/numeric/modulo.cpp
        src/operations/numeric/multiplication.cpp
        src/operations/numeric/subtraction.cpp
        src/operations/string/cat.cpp
        src/operations/string/substr.cpp
)

add_subdirectory(test)
