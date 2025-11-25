add_library(Core INTERFACE)

target_sources(Core
    PUBLIC
        FILE_SET pub_headers
        TYPE HEADERS
        BASE_DIRS "include"
        FILES
            include/CPlusPlus_Common.h
)

add_library(${CMAKE_PROJECT_NAME}::Core ALIAS Core)

install(TARGETS Core EXPORT FILE_SET pub_headers COMPONENT Core)
