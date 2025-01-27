cmake_minimum_required(VERSION 3.13)

set(PROGRAM_NAME "your_project_name")
set(PICO_BOARD pico_w) # Board type

include(pico_sdk_import.cmake)

project(${PROGRAM_NAME})

pico_sdk_init()

add_executable(${PROGRAM_NAME}
    main.c
)

target_include_directories(${PROGRAM_NAME}
    PRIVATE ${CMAKE_CURRENT_LIST_DIR}
)

# Add pico_stdlib library, add more if used
target_link_libraries(${PROGRAM_NAME}
    pico_stdlib
)

# enable UART output, disable USB output
pico_enable_stdio_usb(${PROGRAM_NAME} 0)
pico_enable_stdio_uart(${PROGRAM_NAME} 1)

# Generate UF2 and ELF files
pico_add_extra_outputs(${PROGRAM_NAME})
