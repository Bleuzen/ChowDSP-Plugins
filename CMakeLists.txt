cmake_minimum_required(VERSION 3.15)
project(ChowDSP-Plugins VERSION 2.0.0)

# This should fix the build target conflicts
set(ALLOW_DUPLICATE_CUSTOM_TARGETS TRUE)

option(BUILD_CHOWTAPE "Build the ChowTape plugin" ON)
if(BUILD_CHOWTAPE)
    message(STATUS "Configuring build for ChowTape")
    add_subdirectory(AnalogTapeModel/Plugin EXCLUDE_FROM_ALL)
endif()

option(BUILD_CHOWMATRIX "Build the ChowMatrix plugin" ON)
if(BUILD_CHOWMATRIX)
    message(STATUS "Configuring build for ChowMatrix")
    add_subdirectory(ChowMatrix EXCLUDE_FROM_ALL)
endif()

option(BUILD_CHOWCENTAUR "Build the KlonCentaur plugin" ON)
if(BUILD_CHOWCENTAUR)
    message(STATUS "Configuring build for KlonCentaur")
    add_subdirectory(KlonCentaur EXCLUDE_FROM_ALL)
endif()

option(BUILD_CHOWKICK "Build the ChowKick plugin" ON)
if(BUILD_CHOWKICK)
    message(STATUS "Configuring build for ChowKick")
    add_subdirectory(ChowKick EXCLUDE_FROM_ALL)
endif()
