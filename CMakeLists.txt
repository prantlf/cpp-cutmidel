cmake_minimum_required(VERSION 3.10)

project(cutmidel VERSION 1.0.0)

set(default_build_type "Release")

include_directories(${CMAKE_BINARY_DIR})
add_executable(${CMAKE_PROJECT_NAME} ${CMAKE_PROJECT_NAME}.cc)
if(MSVC)
  target_compile_options(${CMAKE_PROJECT_NAME} PUBLIC /MT)
  target_link_options(${CMAKE_PROJECT_NAME} PUBLIC /INCREMENTAL:NO /NODEFAULTLIB:MSVCRT)
elseif(NOT APPLE)
  target_link_libraries(${CMAKE_PROJECT_NAME} -static)
endif()

set_property(TARGET ${CMAKE_PROJECT_NAME} PROPERTY ADDITIONAL_CLEAN_FILES
  ${CMAKE_PROJECT_NAME}.dSYM)
