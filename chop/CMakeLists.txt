add_library(Chop INTERFACE
    include/CHOP_CPlusPlusBase.h
)

target_link_libraries(Chop
    INTERFACE
        Core
)
