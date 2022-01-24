cmake_minimum_required(VERSION 3.0.0)
project(tmma_projet01 VERSION 0.1.0)

set(CMAKE_CXX_STANDARD 20)


include_directories("./includes")

FILE(GLOB mainSources *.cpp)
FILE(GLOB cppSources cpp/*.cpp)

add_executable (tmma_projet01
        ${mainSources}
        ${cppSources}
)

target_include_directories(tmma_projet01 PUBLIC
        "${PROJECT_SOURCE_DIR}/includes")
        

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
