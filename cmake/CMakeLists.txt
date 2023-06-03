configure_package_config_file(
  "stdgenerator-config.cmake.in" "stdgenerator-config.cmake"
  INSTALL_DESTINATION "${CMAKE_INSTALL_DATADIR}/stdgenerator/cmake"
  NO_SET_AND_CHECK_MACRO NO_CHECK_REQUIRED_COMPONENTS_MACRO)

write_basic_package_version_file(
  "stdgenerator-config-version.cmake" COMPATIBILITY SameMajorVersion ARCH_INDEPENDENT)

install(
  EXPORT "stdgenerator-target"
  NAMESPACE "stdgenerator::"
  DESTINATION "${CMAKE_INSTALL_DATADIR}/stdgenerator/cmake")

install(FILES "${CMAKE_CURRENT_BINARY_DIR}/stdgenerator-config.cmake"
              "${CMAKE_CURRENT_BINARY_DIR}/stdgenerator-config-version.cmake"
        DESTINATION "${CMAKE_INSTALL_DATADIR}/stdgenerator/cmake")
