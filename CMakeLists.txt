cmake_minimum_required(VERSION 3.15)
set(CMAKE_OSX_DEPLOYMENT_TARGET "10.9" CACHE STRING "Minimum OS X deployment target")
set(CMAKE_CXX_STANDARD 17)
project(ChowDSPPlugins VERSION 1.0.0)

add_subdirectory(AnalogTapeModel/Plugin)
add_subdirectory(ChowMatrix)
add_subdirectory(KlonCentaur)
add_subdirectory(ChowKick)
