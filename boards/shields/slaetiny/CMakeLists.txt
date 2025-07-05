# SPDX-License-Identifier: Apache-2.0

zephyr_library()

zephyr_library_sources(${ZEPHYR_BASE}/misc/empty_file.c)
zephyr_library_include_directories(${ZEPHYR_LVGL_MODULE_DIR})
zephyr_library_include_directories(${ZEPHYR_BASE}/lib/gui/lvgl/)
zephyr_library_include_directories(${ZEPHYR_BASE}/drivers)
zephyr_library_include_directories(${CMAKE_SOURCE_DIR}/include)

zephyr_library_sources(widgets/battery_status.c)

zephyr_library_sources(widgets/layer_status.c)
zephyr_library_sources(widgets/modifiers.c)
zephyr_library_sources(widgets/modifiers_sym.c)
zephyr_library_sources(widgets/output_status.c)
zephyr_library_sources(widgets/output_status_sym.c)

zephyr_library_sources(display/sd1306.c)
