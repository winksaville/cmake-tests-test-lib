# Define "a-library" as a staic and shared library
add_library(a-library-static STATIC src/a-library.c)
add_library(a-library-shared SHARED src/a-library.c)

# Include a -DUSING-A-LIBRARY when compling or using this library.
# If this was PRIVATE it would only be seen when compiling the library
# if it was INTERFACE it would not be defined here but would be by users
# use target_link_
target_compile_definitions(a-library-static PUBLIC USING-A-LIBRARY)
target_compile_definitions(a-library-shared PUBLIC USING-A-LIBRARY)

# Have a "-I" for our include/ when compiling or using this library
# PRIVATE and INTERFACE behave as indicated above
target_include_directories(a-library-shared PUBLIC "include")
target_include_directories(a-library-static PUBLIC "include")

