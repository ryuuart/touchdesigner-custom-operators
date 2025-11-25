add_library(Dat INTERFACE
    include/DAT_CPlusPlusBase.h
)

target_link_libraries(Dat
    INTERFACE
        Core
)
