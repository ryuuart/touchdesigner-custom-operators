add_library(Core INTERFACE)

target_sources(Core
    PUBLIC
        FILE_SET pub_headers
        TYPE HEADERS
        BASE_DIRS "include"
        FILES
            include/CPlusPlus_Common.h
)

install(TARGETS Core
    EXPORT TouchDesignerTargets FILE_SET pub_headers COMPONENT core)
