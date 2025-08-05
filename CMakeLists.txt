cmake_minimum_required(VERSION 3.21)

#if(NOT DEFINED ENV{LLVM_HOME})
#    message(FATAL_ERROR "LLVM_HOME environment variable not set!")
#endif()
#if(NOT DEFINED ENV{VCPKG_HOME})
#  message(FATAL_ERROR "VCPKG_HOME environment variable not set!")
#endif()
# set(CMAKE_C_COMPILER    $ENV{LLVM_HOME}/bin/clang)
# set(CMAKE_CXX_COMPILER  $ENV{LLVM_HOME}/bin/clang++)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# 设置 可执行程序输出目录
set(target_bin_debug 			${CMAKE_CURRENT_SOURCE_DIR}/target/debug)
set(target_bin_release 		${CMAKE_CURRENT_SOURCE_DIR}/target/release)
# 设置库文件输出目录
set(target_lib_debug 			${CMAKE_CURRENT_SOURCE_DIR}/target/debug/lib)
set(target_lib_release 		${CMAKE_CURRENT_SOURCE_DIR}/target/release/lib)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_DEBUG 	   ${target_bin_debug})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_RELEASE 	 ${target_bin_release})
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY_DEBUG 	   ${target_lib_debug})
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY_RELEASE 	 ${target_lib_release})

if(NOT CMAKE_CXX_COMPILER)
  if(WIN32)
    find_program(CMAKE_CXX_COMPILER NAMES clang++ g++ cl.exe)
  else()
    find_program(CMAKE_CXX_COMPILER NAMES clang++ g++)
  endif()
endif()

project(winterYufox
  VERSION 0.0.1
  DESCRIPTION "A framework for winterYufox"
  LANGUAGES CXX
)

#option(BUILD_WINTERYUFOX_FRAMEWORKCLI_PROJECT   "Build winterYufox Framework Cli Project" ON)
#option(BUILD_WINTERYUFOX_FRAMEWORKLIB_CORE      "Build winterYufox Framework Lib Core" ON)
#option(BUILD_WINTERYUFOX_FRAMEWORKLIB_LOCALE    "Build winterYufox Framework Lib LOCALE" ON)
#option(BUILD_WINTERYUFOX_FRAMEWORKLIB_PLUGINS   "Build winterYufox Framework Lib Plugins" ON)
#option(BUILD_WINTERYUFOX_FRAMEWORKLIB_UPDATER   "Build winterYufox Framework Lib Updater" ON)
#
#if(BUILD_WINTERYUFOX_FRAMEWORKCLI_PROJECT)
#  add_subdirectory(winteryuufox/framework/tools/wfox)
#endif()
#
#if(BUILD_WINTERYUFOX_FRAMEWORKLIB_CORE)
#  add_subdirectory(winteryuufox/framework/library/core)
#endif()
#
#if(BUILD_WINTERYUFOX_FRAMEWORKLIB_LOCALE)
#  add_subdirectory(winteryuufox/framework/library/locale)
#endif()
#
#if(BUILD_WINTERYUFOX_FRAMEWORKLIB_PLUGINS)
#  add_subdirectory(winteryuufox/framework/library/plugins)
#endif()
#
#if(BUILD_WINTERYUFOX_FRAMEWORKLIB_UPDATER)
#  add_subdirectory(winteryuufox/framework/library/updater)
#endif()


