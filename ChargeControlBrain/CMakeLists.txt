
cmake_minimum_required(VERSION 3.13.1)

list(APPEND ZEPHYR_EXTRA_MODULES
  "${CMAKE_CURRENT_SOURCE_DIR}/../../modules/wavenumber/rt_config"
)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})

zephyr_library_compile_options(-fdiagnostics-color=always)

project(ChargeControlBrain)
target_sources(app PRIVATE src/main.c)
