cmake_minimum_required(VERSION 3.10)
project(fs_bindings LANGUAGES CXX)
list(APPEND CMAKE_PREFIX_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake")

set(Final TRUE)
set(Experimental TRUE)

find_package(Filesystem REQUIRED)

add_library(${PROJECT_NAME} INTERFACE)
target_include_directories(${PROJECT_NAME} INTERFACE include)
target_link_libraries(${PROJECT_NAME} INTERFACE std::filesystem)
if(CXX_FILESYSTEM_IS_EXPERIMENTAL)
  target_compile_definitions(${PROJECT_NAME}
                             INTERFACE CXX_FILESYSTEM_IS_EXPERIMENTAL)
endif()
