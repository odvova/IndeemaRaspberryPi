# create static library 'common'
add_library(common STATIC
    src/logger.cpp
    )

# define the header search path
target_include_directories(common
    PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)

