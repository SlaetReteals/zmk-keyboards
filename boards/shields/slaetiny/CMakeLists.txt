# SPDX-License-Identifier: Apache-2.0

zephyr_library()
zephyr_library_sources_ifdef(CONFIG_DISPLAY_MCUX_ELCDIF	display_mcux_elcdif.c)
zephyr_library_sources_ifdef(CONFIG_DISPLAY_NRF_LED_MATRIX display_nrf_led_matrix.c)
zephyr_library_sources_ifdef(CONFIG_DUMMY_DISPLAY	display_dummy.c)

zephyr_library_sources_ifdef(CONFIG_SSD1306		ssd1306.c)

if (CONFIG_SDL_DISPLAY)
	zephyr_library_sources(display_sdl.c)
	if (CONFIG_NATIVE_APPLICATION)
		zephyr_library_sources(display_sdl_bottom.c)
	else()
		target_sources(native_simulator INTERFACE display_sdl_bottom.c)
	endif()
endif()
