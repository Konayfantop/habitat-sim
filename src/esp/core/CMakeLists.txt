file(GLOB_RECURSE core_SOURCES "*.cpp")

find_package(Corrade REQUIRED Utility)

add_library(core STATIC ${core_SOURCES})

target_link_libraries(core
  PUBLIC
    Corrade::Utility
    glog
)
