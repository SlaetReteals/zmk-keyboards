# SPDX-License-Identifier: Apache-2.0

zephyr_library()

zephyr_library_include_directories(${ZEPHYR_LVGL_MODULE_DIR})
zephyr_library_include_directories(${ZEPHYR_BASE}/lib/gui/lvgl/)
zephyr_library_include_directories(${ZEPHYR_BASE}/drivers)
zephyr_library_include_directories(${CMAKE_SOURCE_DIR}/include)
