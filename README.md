# Jetson-Orin-Nano-Super-Initial-Setup-and-Configuration-Guide

## First Time Setup
### 1. What to prepare
- [ ] Jetson Orin Nano
- [ ] microSD card (Optional: 2 microSD card)
### 2. Boot jetpack 5.1.3 microSD card
* Download the [Jetpack 5.1.3](https://drive.google.com/file/d/1eJxOd_xCs6vfatTCkspKZYgP3k-lr752/view?usp=sharing)
* Unzip the jetpack
* Reflash microSD card using jetpack 5.1.3 using BalenaEtcher
* Run the jetpack until the bootloader/firmware update pop ups (Restart if there is no update pop ups)
* Run the update
* Reboot jetson
### 3. Firmware check
* Open terminal and run:
  ```
  sudo nvbootctrl dump-slots-info
  ```
* If Current Version indicating 36.0 skip to Step 4.
  ```
  Current version: 35.5.0
  Capsule update status: 0
  Current bootloader slot: A
  Active bootloader slot: A
  num_slots: 2
  slot: 0,             status: normal
  slot: 1,             status: normal
  ```
* If the Current Version indicating 35.5.0, open terminal and run:
  ```
  sudo apt-get install nvidia-l4t-jetson-orin-nano-qspi-updater
  ```
* After all the installation finishes, reboot the Jetson.
* The Jetson will be stuck on black screen to update the firmware.
* In a few of minutes, shut down the jetson by disconnect the power supply
### 4.  Boot jetpack 6.1 microSD card
* Download the [Jetpack 6.1](https://drive.google.com/file/d/1oV6lLSeT3fV0EQwfajTa5lkm-dYVGndh/view?usp=sharing)
* Unzip the jetpack
* Reflash microSD card using jetpack 6.1 using BalenaEtcher
* Run the jetpack until the bootloader/firmware update pop ups (Restart if there is no update pop ups)
* Run the update
* Reboot jetson
### 5. Unlock MAXN Super
