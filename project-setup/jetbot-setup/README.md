# Jetbot Setup

### Burning image onto SD card

To setup the environment follow the steps [here](https://jetbot.org/master/software\_setup/sd\_card.html), image used should be Jetson-Nano-4gb. Follow the steps to burn the image onto the SD card.

### Connecting to internet

Eduroam uses special WPA2 802.1X enterprise which requires certificate. There should be a method to connect to it however we did not make it successful.

You can directly connect to your wifi if you are doing the project at your own site; or, start a hotspot using your mobile phone or WINDOWS machine. Mac does not support sharing wifi through wifi connection. Remember to change your hotspot name and password to simple combination of digits and characters to avoid wierd thing happens in the terminal.

Some basic command are shown below

```
// to scan aviliable wifi
nmcli dev wifi

// to connect to specific wifi
nmcli device wifi connect WIFI_NAME passowrd PASSWORD

// to check mac address, ip address, etc.
ifconfig
```

Another possible solution is to connect to Berkeley-IoT, you will need to go to the [website](https://portal.berkeley.edu/people/wifi\_access) and register the mac address of the device (wlan0).

### Bug Fix

After succesfully setting up the image, you will be able to see some messages displayed on i2c. For now the eth0 and wlan0 will be shown as None, and there will be little space left as shown in Mem: xxxx/xxxx >90%.

To fix this, follow the instruction [here](https://github.com/NVIDIA-AI-IOT/jetbot/issues/461). In the terminal run following commands line by line

```
cd ~/jetcard
git pull
./scripts/jetson_install_nvresizefs_service.sh
```

After doing that, reboot the device by "sudo reboot now" and you should be able to see the space has been freed on i2c or by typing

```
df -h
```

### Setup Python

If you encounter issue that python cannot import any packages, try following

```
cd jetbot
python3 setup.py  // python setup.py
```

You might also need to do so in your conda environment

```
conda activate YOUR_ENV_NAME
cd jetbot
python setup.py
```
