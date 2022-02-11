cmake_minimum_required (VERSION 3.13)

project (magents
  VERSION 0.1.0
  DESCRIPTION "Managed secure agents."
  HOMEPAGE_URL "https://github.com/xyrise/magents"
  LANGUAGES C
)

set (CMAKE_C_STANDARD 99)

add_executable (magents "")

target_include_directories (magents
  PRIVATE
    "./include/magents"
)

add_subdirectory ("./include")
add_subdirectory ("./src")

install (
  TARGETS
    magents
  DESTINATION
    bin
)
