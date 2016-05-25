include_directories(include)
file(GLOB INCLUDES "include/**/*.h")
file(GLOB SOURCES "src/**/*.c" "src/**/*.cpp")

add_library(spine-c STATIC ${SOURCES})
target_include_directories(spine-c PUBLIC include)
install(TARGETS spine-c DESTINATION dist/lib)
install(FILES ${INCLUDES} DESTINATION dist/include)