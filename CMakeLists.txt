cmake_minimum_required(VERSION 3.31.0)
project(touchdesigner C CXX)

set(CMAKE_CXX_STANDARD 20)

add_subdirectory(core)
add_subdirectory(top)
add_subdirectory(sop)
add_subdirectory(dat)
add_subdirectory(chop)

install(
    EXPORT TouchDesignerTargets
    FILE touchdesignerConfig.cmake
    NAMESPACE touchdesigner::
    DESTINATION "lib/cmake/touchdesigner"
)
