add_library(Chop INTERFACE)

target_sources(Chop
    PUBLIC
        FILE_SET pub_headers
        TYPE HEADERS
        BASE_DIRS "include"
        FILES
            include/CHOP_CPlusPlusBase.h
)

target_link_libraries(Chop
    INTERFACE
        Core
)

install(TARGETS Chop EXPORT Chop FILE_SET pub_headers COMPONENT Chop)
install(EXPORT Chop NAMESPACE ${CMAKE_PROJECT_NAME} DESTINATION ".")
