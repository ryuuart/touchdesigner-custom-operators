add_library(Top INTERFACE
    include/TOP_CPlusPlusBase.h
)

target_link_libraries(Top
    INTERFACE
        Core
)
