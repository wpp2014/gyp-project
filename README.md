# GYP Sample
使用GYP整理工程的测试

## Install `depot_tools`
下载`depot_tools`
```shell
git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git
```

配置环境变量
```shell
export PATH="$PATH:/path/to/depot_tools"
```

## Get the code
```shell
mkdir project
cd project
gclient config --name=src git@github.com:wpp2014/gyp-project.git
gclient sync
```

## example
```shell
cd src
./build/gyp_chromium example/hello.gyp
ninja -C out/Release hello
./out/Release/hello
```
