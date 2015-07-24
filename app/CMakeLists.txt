# The executable name "test-lib"
add_executable(test-lib src/main.c)

# Include a "-I" for our include library but only for ourselves
target_include_directories(test-lib PRIVATE "include")

# We link to "a-library and will get any compile time -D and -I
target_link_libraries(test-lib a-library-static)

