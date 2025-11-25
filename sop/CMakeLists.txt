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

install(TARGETS Sop EXPORT Sop FILE_SET pub_headers COMPONENT Sop)
install(EXPORT Sop NAMESPACE ${CMAKE_PROJECT_NAME} DESTINATION ".")
