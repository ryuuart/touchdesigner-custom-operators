add_library(Core INTERFACE
    include/CPlusPlus_Common.h
)

target_include_directories(Core
    INTERFACE
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)
