add_library(Top INTERFACE)

target_sources(Top
    PUBLIC
        FILE_SET pub_headers
        TYPE HEADERS
        BASE_DIRS "include"
        FILES
            include/TOP_CPlusPlusBase.h
)

target_link_libraries(Top
    INTERFACE
        Core
)

install(TARGETS Top EXPORT Top FILE_SET pub_headers COMPONENT top)
install(EXPORT Top NAMESPACE ${CMAKE_PROJECT_NAME} DESTINATION ".")
