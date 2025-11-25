add_library(Sop INTERFACE
    include/SOP_CPlusPlusBase.h
)

target_link_libraries(Sop
    INTERFACE
        Core
)
