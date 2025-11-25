add_library(Dat INTERFACE)

target_sources(Dat
    PUBLIC
        FILE_SET pub_headers
        TYPE HEADERS
        BASE_DIRS "include"
        FILES
            include/DAT_CPlusPlusBase.h
)

target_link_libraries(Dat
    INTERFACE
        Core
)

install(TARGETS Dat EXPORT Dat FILE_SET pub_headers COMPONENT dat)
install(EXPORT Dat NAMESPACE ${CMAKE_PROJECT_NAME} DESTINATION ".")
