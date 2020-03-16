cmake_minimum_required (VERSION 3.1)
project (bs4kass)
file(GLOB CORE_FILES ${PROJECT_SOURCE_DIR}/*.c)
add_executable(bs4kass ${CORE_FILES})
set (CMAKE_C_STANDARD 99)
set_property(TARGET bs4kass PROPERTY C_STANDARD 99)

add_definitions(-DXML_STATIC)
add_definitions(-D_CRT_SECURE_NO_WARNINGS)
include_directories(vendor/include)
target_link_libraries(bs4kass 
  ${PROJECT_SOURCE_DIR}/vendor/lib-msvc-x64/libavcodec.a
  ${PROJECT_SOURCE_DIR}/vendor/lib-msvc-x64/libavformat.a
  ${PROJECT_SOURCE_DIR}/vendor/lib-msvc-x64/libavutil.a
  ${PROJECT_SOURCE_DIR}/vendor/lib-msvc-x64/libexpat.lib
  bcrypt.lib
)
