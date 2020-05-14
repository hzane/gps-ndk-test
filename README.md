# GPS tester for Android ROMs

This program uses Android's HAL functionality to completely bypass Java Framework layer and directly connect to GPS satelites and then outputs received information into the terminal.

## Configure VS Code

- Have the Android source code
- add Android Kit
- add compiler configurations in c_cpp_properties.json
- add cmake configurations in settings.json

## Make Standalone Android Toolchain

## Download Android Source Code

## How to use

* Install Android Standalone Toolchain and set VARIABLE TOOLCHAIN=<directory of the ndk toolchain>

```shell
mkdir build && cd build
.../cmake-build
adb push gps-test /data/local/tmp
adb shell /data/local/tmp/gps-test

```
