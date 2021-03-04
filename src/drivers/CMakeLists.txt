cmake_minimum_required(VERSION 3.10)
project(target-drivers LANGUAGES CXX)

add_library(
  drivers STATIC
  Cst816s.cpp
  DebugPins.cpp
  Hrs3300.cpp
  InternalFlash.cpp
  Spi.cpp
  SpiMaster.cpp
  SpiNorFlash.cpp
  St7789.cpp
  TwiMaster.cpp
  Watchdog.cpp)

target_include_directories(drivers INTERFACE .)

target_link_libraries(drivers PRIVATE system)
