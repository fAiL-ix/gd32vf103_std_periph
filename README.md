# GD32VF103 Standard Peripheral Firmware Lib

This is a standalone CMake library version of the [GD32VF103_standard_peripheral firmware](http://www.gd32mcu.com/en/download/7?kw=GD32VF1) provided by Gigadevice.

This library is based on the 1.1.0 version of the Gigadevice library.

## Cloning

This project includes the [GD32VF103 Firmware Lib](https://github.com/fAiL-ix/gd32vf103) as a submodul. To clone this repository with the submodules use the following command:

`git clone --recurse-submodules https://github.com/fAiL-ix/gd32vf103_std_periph.git`

If you already cloned the repository you can use these two commands to download the submodule:

`git submodule init`

`git submodule update`

## Using this Library

To use this library in your project, clone this repository somewhere into your project. Then add the library as a subdirectory and link target in your projects `CMakeLists.txt`.

`add_subdirectory(path/to/this/lib)` [CMake Doc](https://cmake.org/cmake/help/latest/command/add_subdirectory.html)

`target_link_libraries(<your target> gd32vf103 gd32vf103_std_periph)` [CMake Doc](https://cmake.org/cmake/help/latest/command/target_link_libraries.html)

You also have to define your target board type which is done by defining one of those variables:
- `GD32VF103C_START`
- `GD32VF103R_START`
- `GD32VF103T_START`
- `GD32VF103V_EVAL`

To define it you can add `target_compile_definitions` to your project.

`target_compile_definitions(gd32vf103 PUBLIC GD32VF103V_EVAL)` [CMake Doc](https://cmake.org/cmake/help/latest/command/target_compile_definitions.html)
