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

add_library(${CMAKE_PROJECT_NAME}::Top ALIAS Top)

install(TARGETS Top EXPORT FILE_SET pub_headers COMPONENT Top)
