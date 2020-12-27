# gd32vf103_std_periph CMakeLists.txt
# Author: fAiLix

cmake_minimum_required(VERSION 3.19)

add_library(
    gd32vf103_std_periph
    OBJECT
        "${CMAKE_CURRENT_SOURCE_DIR}/src/system/system_gd32vf103.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_adc.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_bkp.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_can.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_crc.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_dac.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_dbg.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_dma.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_eclic.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_exmc.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_exti.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_fmc.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_fwdgt.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_gpio.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_i2c.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_pmu.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_rcu.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_rtc.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_spi.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_timer.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_usart.c"
        "${CMAKE_CURRENT_SOURCE_DIR}/src/peripheral/gd32vf103_wwdgt.c"
    )

target_include_directories(
    gd32vf103_std_periph
    PUBLIC
        "${CMAKE_CURRENT_SOURCE_DIR}/include/peripheral"
    PRIVATE
        "${CMAKE_CURRENT_SOURCE_DIR}/src/system"
)

add_subdirectory("${CMAKE_CURRENT_SOURCE_DIR}/extern/gd32vf103")

target_link_libraries(gd32vf103_std_periph gd32vf103)
