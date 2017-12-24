add_library(boost_system STATIC
    libs/system/src/error_code.cpp
)
target_include_directories(boost_system PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_compile_definitions(boost_system PUBLIC BOOST_ALL_NO_LIB)
add_library(boost_filesystem STATIC
    libs/filesystem/src/codecvt_error_category.cpp
    libs/filesystem/src/operations.cpp
    libs/filesystem/src/path.cpp
    libs/filesystem/src/path_traits.cpp
    libs/filesystem/src/portability.cpp
    libs/filesystem/src/unique_path.cpp
    libs/filesystem/src/utf8_codecvt_facet.cpp
    libs/filesystem/src/windows_file_codecvt.cpp
)
target_include_directories(boost_filesystem PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(boost_filesystem PUBLIC boost_system)
target_compile_definitions(boost_filesystem PUBLIC BOOST_ALL_NO_LIB)
