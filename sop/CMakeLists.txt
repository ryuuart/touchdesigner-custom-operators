add_library(Sop INTERFACE)

target_sources(Sop
    PUBLIC
        FILE_SET pub_headers
        TYPE HEADERS
        BASE_DIRS "include"
        FILES
            include/SOP_CPlusPlusBase.h
)

target_link_libraries(Sop
    INTERFACE
        Core
)

install(TARGETS Sop
    EXPORT TouchDesignerTargets FILE_SET pub_headers COMPONENT sop)
