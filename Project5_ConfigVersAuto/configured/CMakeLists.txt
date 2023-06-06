configure_file(
    "config.hpp.in"
    "${CMAKE_BINARY_DIR}/configured_files/include/config.hpp" ESCAPE_QUOTES   # CMAKE_BINARY_DIR - absolutely path for build dir
)
