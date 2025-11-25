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

add_library(${CMAKE_PROJECT_NAME}::Dat ALIAS Dat)

install(TARGETS Dat EXPORT FILE_SET pub_headers COMPONENT Dat)
