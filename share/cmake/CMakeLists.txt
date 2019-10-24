configure_file(myapp4triqs-config.cmake.in myapp4triqs-config.cmake @ONLY)
configure_file(myapp4triqs-config-version.cmake.in myapp4triqs-config-version.cmake @ONLY)
install(
  FILES
    ${CMAKE_CURRENT_BINARY_DIR}/myapp4triqs-config.cmake
    ${CMAKE_CURRENT_BINARY_DIR}/myapp4triqs-config-version.cmake
  DESTINATION lib/cmake/myapp4triqs
)

install(EXPORT myapp4triqs-targets NAMESPACE myapp4triqs:: DESTINATION lib/cmake/myapp4triqs)
