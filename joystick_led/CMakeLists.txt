cmake_minimum_required(VERSION 3.13)
include(pico_sdk_import.cmake)

project(joystick C CXX ASM)
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

pico_sdk_init()

add_executable(joystick joystick.c)

# Linka com a biblioteca padrão e bibliotecas de hardware necessárias
target_link_libraries(joystick pico_stdlib hardware_adc hardware_pwm)

pico_add_extra_outputs(joystick)
