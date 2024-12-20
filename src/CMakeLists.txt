# The Flutter tooling requires that developers have CMake 3.10 or later
# installed. You should not increase this version, as doing so will cause
# the plugin to fail to compile for some customers of the plugin.
cmake_minimum_required(VERSION 3.10)

project(google_ffi_dart_tutorial_library VERSION 0.0.1 LANGUAGES C)

add_library(google_ffi_dart_tutorial SHARED
  "google_ffi_dart_tutorial.c"
)

set_target_properties(google_ffi_dart_tutorial PROPERTIES
  PUBLIC_HEADER google_ffi_dart_tutorial.h
  OUTPUT_NAME "google_ffi_dart_tutorial"
)

target_compile_definitions(google_ffi_dart_tutorial PUBLIC DART_SHARED_LIB)
