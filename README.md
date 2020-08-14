# Pinnacle 100 Sample Applications Manifest Repo

## Cloning Firmware

This is a Zephyr `west` manifest repository. To learn more about `west` see [here](https://docs.zephyrproject.org/latest/guides/west/index.html).

To clone this repository properly use the `west` tool. To install `west` you will first need Python3.

Install `west` using `pip3`:

```
# Linux
pip3 install --user -U west

# macOS (Terminal) and Windows (cmd.exe)
pip3 install -U west
```

Once `west` is installed, clone this repository using `west init` and `west update`:

```
# Checkout the latest manifest on master
west init -m https://github.com/LairdCP/Pinnacle_100_Sample_Applications_Manifest.git

# Now, pull all the source described in the manifest
west update
```

## Preparing to Build

If this is your first time working with a Zephyr project on your computer you should follow the [Zephyr getting started guide](https://docs.zephyrproject.org/latest/getting_started/index.html#) to install all the tools.

The OOB demo uses zephyr 2.3.x, so GCC 9 is recommended.
[GNU Arm Embedded Toolchain: 9-2019-q4-major](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads) is recommended.

See here to [setup the GNU ARM Embedded tools](https://docs.zephyrproject.org/1.14.1/getting_started/toolchain_3rd_party_x_compilers.html)

## Building the Firmware

From the directory where you issued the `west init` and `west update` commands you can use the following command to build the firmware:

```
# Windows
west build -b pinnacle_100_dvk -d pinnacle_100_sample_applications\build[app_name] pinnacle_100_sample_applications\apps[app_name]

# Linux and macOS
west build -b pinnacle_100_dvk -d pinnacle_100_sample_applications/build[app_name] pinnacle_100_sample_applications/apps[app_name]

```
