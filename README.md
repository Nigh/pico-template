# pico-template
rpi pico template

## prepare

### Get pico SDK

```shell
git clone https://gitee.com/xianii/pico-sdk
cd pico-sdk
git submodule update --init

## Add pico-sdk Path to your environment
echo export PICO_SDK_PATH=$PWD >> ~/.profile
```

### Install dependencies

```shell
sudo apt update && sudo apt install -y cmake make ninja-build gcc g++ openssl libssl-dev cmake gcc-arm-none-eabi libnewlib-arm-none-eabi libstdc++-arm-none-eabi-newlib
```

## Compile

```shell
make
```
