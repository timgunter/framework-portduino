cmake_minimum_required(VERSION 3.16)
project(Portduino)

set(CMAKE_CXX_STANDARD 14)

include_directories(cores/arduino/api)
include_directories(cores/portduino)
include_directories(cores/portduino/FS)

add_executable(Portduino
        cores/arduino/api/Common.cpp
        cores/arduino/api/IPAddress.cpp
        # cores/arduino/api/PluggableUSB.cpp
        cores/arduino/api/Print.cpp
        cores/arduino/api/Stream.cpp
        cores/arduino/api/String.cpp
        cores/portduino/itoa.cpp
        cores/portduino/dtostrf.c
        cores/portduino/main.cpp
        cores/portduino/linux/millis.cpp
        cores/portduino/simulated/SimCommon.cpp
        #cores/portduino/simulated/Utility.cpp
        cores/portduino/Utility.cpp
        cores/portduino/simulated/SimHardwareSPI.cpp
        example/test.cpp
        cores/portduino/simulated/SimHardwareI2C.cpp
        cores/portduino/linux/LinuxCommon.cpp
        cores/portduino/linux/LinuxSerial.cpp

        cores/portduino/FS/FS.cpp
        cores/portduino/FS/PortduinoFS.cpp
        cores/portduino/FS/vfs_api.cpp
        cores/portduino/logging.cpp
        cores/portduino/PortduinoGPIO.cpp
        cores/portduino/linux/LinuxHardwareSPI.cpp
)
