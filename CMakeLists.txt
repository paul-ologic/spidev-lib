cmake_minimum_required(VERSION 3.0)
project(spidev-lib)

include_directories(src/)

add_library(spidev-lib src/spidev_lib.c)
target_link_libraries( spi-testc spidev-lib)

add_library(spidev-lib++ src/spidev_lib++.cc)
target_link_libraries( spi-testcpp spidev-lib++ )


install(TARGETS spidev_lib spidev_lib++ DESTINATION lib)
INSTALL( FILES src/spidev_lib.h DESTINATION include)
INSTALL( FILES src/spidev_lib++.h src/spidev_lib.h DESTINATION include)

