add_library(physfs++ physfs.cpp)
target_link_libraries(physfs++ physfs)
set_target_properties(physfs++ PROPERTIES DEBUG_POSTFIX -dbg)
install(
  TARGETS physfs++
  LIBRARY DESTINATION lib${LIB_SUFFIX}
  ARCHIVE DESTINATION lib${LIB_SUFFIX})
