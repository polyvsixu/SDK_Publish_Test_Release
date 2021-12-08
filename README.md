# SDK_NAME

## 简介

`SDK_NAME` 为 xxx SDK，下称为 SDK

`sdk_publish_test_release` 为 `SDK_NAME` 的 demo 项目，下称为 demo

* GitHub: [sdk_publish_test_release](https://github.com/[organization]/[project])
* Gitee: [sdk_publish_test_release](https://gitee.com/[organization]/[project])

## SDK 功能

* 功能 1
* 功能 2

## SDK 下载

1. 下载 Windows 版本

    [WIN_SDK_X86.zip](http://xxx.xxx.xxx/download/WIN_SDK_X86.zip)

    [WIN_SDK_X64.zip](http://xxx.xxx.xxx/download/WIN_SDK_X64.zip)

1. 下载 Mac 版本

    [MAC_SDK.zip](http://xxx.xxx.xxx/download/MAC_SDK.zip)

## SDK 更新日志

[CHANGELOG.md](CHANGELOG.md)

## 集成

### 集成 Windows 版本

SDK 基于 Visual Studio 16 2019 环境编译，提供 32 位，64 位 SDK

依赖 xxx，已于 SDK 的 `third-party` 目录下提供相关依赖环境

demo 使用 CMake（[CMake.org](https://cmake.org/)） 进行构建，
用于生成不同 IDE 平台下的工程。
CMake 提供 GUI 和 命令行 两种交互方式，
这里以命令行为例来生成项目。

```bat
mkdir build
cd build

cmake .. -G"Visual Studio 16 2019"
REM 生成 64 位 demo 的 VS 工程

start *.sln
REM 打开 VS 工程
```

### 集成 Mac 版本

SDK 基于 Xcode 12.4 环境编译，支持系统最低版本为 macOS Mojave （10.14）

依赖 xxx，通过 homebrew 提供依赖，可使用如下命令安装依赖

```bash
brew install curl
brew install openssl@1.1
```

demo 使用 CMake（[CMake.org](https://cmake.org/)） 进行构建，
用于生成不同 IDE 平台下的工程。
CMake 提供 GUI 和 命令行 两种交互方式，
这里以命令行为例来生成项目。

```bash
mkdir build
cd build

cmake .. -G"XCode"
# 生成 demo 的 XCode 工程

open *.xcodeproj
# 打开 XCode 工程
```

## API 文档

[API 文档](https://xxx.xxx.xxx/doc/latest/index.html)
