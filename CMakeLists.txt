cmake_minimum_required(VERSION 3.12)
project(Siv3DTemplate CXX)

if (NOT CMAKE_CONFIGURATION_TYPES AND 
    NOT CMAKE_NO_BUILD_TYPE AND
    NOT CMAKE_BUILD_TYPE AND
    CMAKE_SOURCE_DIR STREQUAL CMAKE_CURRENT_SOURCE_DIR)
    message(STATUS "[!] Setting build type to 'Release' as none was specified.")
    set(CMAKE_BUILD_TYPE Release)
endif()
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/App")

find_package(Siv3D REQUIRED)

add_executable(Siv3DTemplate Main.cpp)
target_compile_features(Siv3DTemplate PUBLIC cxx_std_20)

target_link_libraries(Siv3DTemplate PUBLIC Siv3D::Siv3D)

if (NOT CMAKE_BUILD_TYPE STREQUAL "Release")
    set_target_properties(
        Siv3DTemplate
        PROPERTIES SUFFIX "_${CMAKE_BUILD_TYPE}"
    )
endif()
