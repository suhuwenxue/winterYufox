cmake_minimum_required(VERSION 3.21)

project(winterYufox_FrameworkCLI
  VERSION 0.0.1
  DESCRIPTION "winterYufox_FrameworkCLI"
  LANGUAGES CXX
)

# find_package(fmt CONFIG REQUIRED)
# find_package(CLI11 CONFIG REQUIRED)
# find_package(spdlog CONFIG REQUIRED)
# find_package(indicators CONFIG REQUIRED)
# find_package(date CONFIG REQUIRED)

add_executable(wfox
  src/main.cpp
  # src/command.cpp
  # src/commands/build.cpp
  # src/commands/dev.cpp
  # src/commands/bundle.cpp
  # src/commands/android.cpp
  # src/commands/ios.cpp
  # src/commands/icon.cpp
  # src/commands/init.cpp
  include/wfox/main.h
  # include/wfox/command.h
  # include/wfox/commands/android.h
  # include/wfox/commands/build.h
  # include/wfox/commands/bundle.h
  # include/wfox/commands/dev.h
  # include/wfox/commands/icon.h
  # include/wfox/commands/ios.h
  # include/wfox/commands/init.h
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

target_include_directories(wfox PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
    $<INSTALL_INTERFACE:include>
)
