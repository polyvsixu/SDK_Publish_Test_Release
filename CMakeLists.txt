cmake_minimum_required(VERSION 3.12)
project(SDK_Publish)

set(SDK_PUBLISH_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/include)

if(WIN32)
    if(CMAKE_SIZEOF_VOID_P EQUAL 8)
        set(PLATFORM x64)
    else()
        set(PLATFORM x86)
    endif()
    set(SDK_PUBLISH_LIB ${CMAKE_CURRENT_SOURCE_DIR}/lib/Win/${PLATFORM}/SDK_Publish.lib)
    set(SDK_PUBLISH_DLL ${CMAKE_CURRENT_SOURCE_DIR}/lib/Win/${PLATFORM}/SDK_Publish.dll)
else(__APPLE__)
    set(SDK_PUBLISH_LIB ${CMAKE_CURRENT_SOURCE_DIR}/lib/macOS/SDK_Publish.dylib)
endif()

# TODO: download shared lib
# set(WIN_SDK_X86_URL http://xxx.xxx.xxx/download/WIN_SDK_X86.zip)
# set(WIN_SDK_X64_URL http://xxx.xxx.xxx/download/WIN_SDK_X64.zip)
# set(MAC_SDK_URL http://xxx.xxx.xxx/download/MAC_SDK.zip)

add_subdirectory(demo)
