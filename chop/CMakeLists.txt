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

add_library(${CMAKE_PROJECT_NAME}::Chop ALIAS Chop)

install(TARGETS Chop EXPORT FILE_SET pub_headers COMPONENT Chop)
