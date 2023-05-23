# Imnodes
add_library(imnodes STATIC imnodes.h
    imnodes_internal.h
    imnodes.cpp)
target_include_directories(imnodes PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(imnodes PUBLIC imgui::imgui)

set_target_properties (imnodes PROPERTIES FOLDER External)
target_compile_definitions(imnodes PRIVATE IMGUI_DEFINE_MATH_OPERATORS)
