# Pinnacle 100 Sample Applications Manifest Repo

## Cloning Firmware

This is a Zephyr `west` manifest repository. To learn more about `west` see [here](https://docs.zephyrproject.org/latest/guides/west/index.html).

To clone this repository properly use the `west` tool. To install `west` you will first need Python3.

Install `west` using `pip3`:

```
pip3 install --user -U west
```

Once `west` is installed, clone this repository using `west init` and `west update`:

```
# Checkout the latest manifest on main
west init -m https://github.com/LairdCP/Pinnacle_100_Sample_Applications_Manifest.git

# Now, pull all the source described in the manifest
west update
```

## Preparing to Build

If this is your first time working with a Zephyr project on your computer you should follow the [Zephyr getting started guide](https://docs.zephyrproject.org/latest/develop/getting_started/index.html) to install all the tools.

The sample apps use Zephyr 3.1.99, so the [Zephyr SDK v 0.14.2](https://github.com/zephyrproject-rtos/sdk-ng/releases/tag/v0.14.2) is recommended.

## Building the Firmware

From the directory where you issued the `west init` and `west update` commands you can use the following command to build the firmware:

```
west build -p auto -b pinnacle_100_dvk -d Pinnacle_100_Sample_Applications/build/[app_name] Pinnacle_100_Sample_Applications/apps/[app_name]
```
