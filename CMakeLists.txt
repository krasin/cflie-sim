cmake_minimum_required (VERSION 2.8.9)
project(cflie-sim)

include(ExternalProject)

ExternalProject_Add(qemu
  PREFIX qemu
  GIT_REPOSITORY git@github.com:krasin/qemu_stm32.git
  CONFIGURE_COMMAND <SOURCE_DIR>/configure --target-list=arm-softmmu
  INSTALL_COMMAND ""
  )
