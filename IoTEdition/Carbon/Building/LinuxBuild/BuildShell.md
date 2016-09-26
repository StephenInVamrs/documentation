## How to build the Shell Zephyr application from source - Linux Host

These instructions will show how to build a sample Zephyr application using a Linux Host machine as a development environment.

***

- **Step 0**: Download and setup Zephyr
- **Step 1**: Build a sample application in Zephyr
- **Step 2**: Proceed to Installation page for flashing instructions

***

####**Step 0**: Download and setup Zephyr
- Download and setup the Zephyr development environment from https://www.zephyrproject.org. You can find more information about installing the Zephyr SDK at https://www.zephyrproject.org/doc/getting_started/getting_started.html
- Since Carbon support is not yet available in upstream Zephyr, download Zephyr from https://github.com/linaro/zephyr:

```shell
$ git clone https://github.com/linaro/zephyr
```

####**Step 1**: Build the Zephyr shell application

- Build the sample shell application as follows:
```shell
$ cd zephyr
$ git remote add linaro https://github.com/linaro/zephyr
$ git remote update
$ git checkout -t linaro/carbon 
$ source zephyr-env.sh
$ make -C samples/shell BOARD=96b_carbon
```

The application will be available at ```samples/shell/outdir/96b_carbon/zephyr.bin```.

#### **Step 2**: Proceed to Installation page for flashing instructions

Proceed to flash the Zephyr application binary over USB-UART or USB-DFU. Host machine specific flashing instructions can be found on the "Installation" page, link found below.

- [Installation Page](../../Installation/README.md)