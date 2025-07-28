cmake_minimum_required(VERSION 3.21)

project(winterYufox_FrameworkLib_Core
  VERSION 0.0.1
  DESCRIPTION "winterYufox_FrameworkLib_Core"
  LANGUAGES CXX
)

# SHARED | STATIC
add_library(winteryufox.core STATIC
  src/library.cpp


  include/winteryufox.core/library.h
)

# if(WIN32)
#   set(RC_FILE ${CMAKE_CURRENT_SOURCE_DIR}/resources/resource.rc)
#   target_sources(wfox PRIVATE ${RC_FILE})
#   set_source_files_properties(${RC_FILE} PROPERTIES LANGUAGE RC)
# endif()

# target_link_libraries(wfox
#   PRIVATE
#     fmt::fmt
#     CLI11::CLI11
#     spdlog::spdlog
#     indicators::indicators
#     date::date
#     date::date-tz
# )

target_include_directories(winteryufox.core PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
    $<INSTALL_INTERFACE:include>
)
