cmake_minimum_required(VERSION 3.14)

project(gps-test)

include(CheckPIESupported)
check_pie_supported()

set(ASOP /one.d/ws.c/mstar/m938 CACHE PATH "Android Source Directory")

include_directories(
    ${ASOP}/hardware/libhardware/include
    ${ASOP}/system/core/include
)
link_directories(${CMAKE_SOURCE_DIR}/system/lib)

set(CMAKE_EXE_LINKER_FLAGS -Wl,--hash-style=both)

add_executable(gps-test gps_test.cpp)
target_link_libraries(gps-test PRIVATE hardware )
