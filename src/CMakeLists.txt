add_executable(test test.cpp) 
add_dependencies(test roaring)
target_link_libraries(test roaring) 
