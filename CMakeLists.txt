cmake_minimum_required(VERSION 3.16)

# Pull in SDK (must be before project)
include(pico_sdk_import.cmake)

project(PicoTemplate C CXX ASM)
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

pico_sdk_init()

add_executable(PicoTemplate main.c)

# Link with the pico stdlib
# hardware_clocks hardware_i2c hardware_pio hardware_interp hardware_rtc hardware_uart hardware_irq hardware_resets
# pico_unique_id
# tinyusb_host tinyusb_device tinyusb_board
target_link_libraries(PicoTemplate pico_stdlib hardware_adc)

# Create map/bin/hex/uf2 files
pico_add_extra_outputs(PicoTemplate)

# Enable USB serial
# pico_enable_stdio_usb(PicoTemplate 1)
# pico_enable_stdio_uart(PicoTemplate 0)
