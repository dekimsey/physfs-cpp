add_library(physfs++ physfs.cpp)
find_package(PhysFS REQUIRED)
target_link_libraries(physfs++ ${PHYSFS_LIBRARY})
set_property(TARGET physfs++ APPEND PROPERTY INCLUDE_DIRECTORIES ${PHYSFS_INCLUDE_DIR})
set_target_properties(physfs++ PROPERTIES DEBUG_POSTFIX -dbg)
install(
  TARGETS physfs++
  LIBRARY DESTINATION lib${LIB_SUFFIX}
  ARCHIVE DESTINATION lib${LIB_SUFFIX}
  RUNTIME DESTINATION bin)
