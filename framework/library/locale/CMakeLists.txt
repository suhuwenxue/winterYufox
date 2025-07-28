cmake_minimum_required(VERSION 3.21)

project(winterYufox_FrameworkLib_Locale
  VERSION 0.0.1
  DESCRIPTION "winterYufox_FrameworkLib_Locale"
  LANGUAGES CXX
)

# find_package(fmt CONFIG REQUIRED)
# find_package(CLI11 CONFIG REQUIRED)
# find_package(spdlog CONFIG REQUIRED)
# find_package(indicators CONFIG REQUIRED)
# find_package(date CONFIG REQUIRED)

add_library(winteryufox.locale STATIC
  src/library.cpp


  include/winteryufox.locale/library.h
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

target_include_directories(winteryufox.locale PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
    $<INSTALL_INTERFACE:include>
)
