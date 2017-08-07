Cloud4RPi Examples for [Next Thing Co. C.H.I.P.](https://getchip.com/pages/chip)
==============================================================================

[![Build Status](https://travis-ci.org/cloud4rpi/cloud4rpi-chip-python.svg?branch=master)](https://travis-ci.org/cloud4rpi/cloud4rpi-chip-python)

## Running the Sample Code

1. Update your system and make sure you have the latest versions of all required software:
    ```sh
    sudo apt update && sudo apt upgrade -y
    sudo apt install python python-pip git -y
    sudo pip install --upgrade setuptools
    ```
2. If you are going to use GPIO, install the **CHIP_IO** library using the instructions from the [CHIP_IO repository](https://github.com/xtacocorex/CHIP_IO).
2. Install the Cloud4RPi client library:
    ```sh
    sudo pip install cloud4rpi
    ```
3. Clone this repository:
    ```sh
    git clone https://github.com/cloud4rpi/cloud4rpi-chip-python.git && cd cloud4rpi-chip-python
    ```
4. [Log into your Cloud4RPi account](https://cloud4rpi.io/auth) or [create a new one](https://cloud4rpi.io/auth/signup).
5. Copy the **Device Token** of [your device](https://cloud4rpi.io/devices). If you have no devices yet, create one on the [Devices](https://cloud4rpi.io/devices) page and copy its **Device Token**.
6. Replace the `__YOUR_DEVICE_TOKEN__` string in the [control.py](https://github.com/cloud4rpi/cloud4rpi-chip-python/blob/master/control.py) file with your device token using any text editor (**nano**, **vim**, **sed** or other):
    ```sh
    sed -i 's/__YOUR_DEVICE_TOKEN__/replace-this-text-with-your-real-device-token/' control.py
    ```
7. Run the `control.py` example:
    ```sh
    sudo python control.py
    ```
8. Notice that the [device](https://cloud4rpi.io/devices) went online and starts sending data.
9. Go to the [Control Panels](https://cloud4rpi.io/control-panels/) page and add a new control panel.
10. Add a new **Gauge** widget and bind it to the `CPU Temp` variable.
10. Add a new **Switch** widget and bind it to the `LED On` variable.
11. Add a new **Text** widget and bind it to the `STATUS` variable. Configure different colors for **"IDLE"**, **"RING"** and **"BOOM!"** strings.
12. If you have [DS18B20 sensor connected to your C.H.I.P.](https://cloud4rpi.github.io/docs/howto/#connect-ds18b20-temperature-sensor), add a new **Chart** widget and bind it to the `Room Temp` variable.

You can use this control panel to monitor variables and control a logical state on a hardware pin.

![](https://github.com/cloud4rpi/docs/raw/master/example-img/panel.png)



## See Also

* [Examples for Raspberry Pi](https://github.com/cloud4rpi/cloud4rpi-raspberrypi-python)
* [Examples for Onion Omega2](https://github.com/cloud4rpi/cloud4rpi-omega2-python)
* [Client Library](https://github.com/cloud4rpi/cloud4rpi)
* [Documentation Repository](https://github.com/cloud4rpi/docs)
