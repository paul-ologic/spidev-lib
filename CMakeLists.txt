cmake_minimum_required(VERSION 3.0)
project(spidev-lib)

include_directories(src/)

add_library(spidev-lib STATIC src/spidev_lib.c)
add_library(spidev-lib++ STATIC src/spidev_lib++.cc)

set_target_properties(spidev-lib PROPERTIES VERSION 0.0.1 SOVERSION 0.0.1)
set_target_properties(spidev-lib++ PROPERTIES VERSION 0.0.1 SOVERSION 0.0.1)

install(TARGETS spidev-lib DESTINATION lib)
install(TARGETS spidev-lib++ DESTINATION lib)
INSTALL( FILES src/spidev_lib.h DESTINATION include)
INSTALL( FILES src/spidev_lib++.h src/spidev_lib.h DESTINATION include)

