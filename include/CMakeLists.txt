add_library(stdgenerator INTERFACE)
target_compile_features(stdgenerator INTERFACE cxx_std_20)
target_sources(
  stdgenerator
    INTERFACE FILE_SET
              "stdgenerator_headers"
              TYPE
              "HEADERS"
              FILES
              "__generator.hpp"
              "generator")

include(GNUInstallDirs)

install(
  TARGETS stdgenerator
  EXPORT "stdgenerator-target"
  FILE_SET "stdgenerator_headers")

if(NOT TARGET stdgenerator::stdgenerator)
  add_library(stdgenerator::stdgenerator ALIAS stdgenerator)
endif()
