cmake_minimum_required(VERSION 3.0)
project(spidev-lib)

include_directories(src/)

add_library(spidev-lib SHARED src/spidev_lib.c)
add_library(spidev-lib++ SHARED src/spidev_lib++.cc)

install(TARGETS spidev-lib DESTINATION lib)
install(TARGETS spidev-lib++ DESTINATION lib)
INSTALL( FILES src/spidev_lib.h DESTINATION include)
INSTALL( FILES src/spidev_lib++.h src/spidev_lib.h DESTINATION include)

