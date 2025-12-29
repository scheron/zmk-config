## Step 1: Preparing the firmware
Synchronize your fork with the main ZMK repository to get the latest updates. After that, build (compile) the firmware and download the resulting *.uf2 files: one for the left and right halves, and one for the Qube dongle.


Additionally, you will need a reset firmware (settings_reset-ergohaven-zmk.uf2). Usually, it can be found in the same place as the main firmware, or in our keymap_hub.

![image](https://journey.ergohaven.xyz/images/qube/keymap_hub.png)

## Step 2: Full reset
This step is necessary for a “clean” installation and to avoid conflicts between the old and new firmware. We will sequentially install the reset firmware on all three devices.

Turn off the power on both halves of the keyboard. Use the physical switches on the bottom of the case for this.
![image](https://journey.ergohaven.xyz/images/qube/buttons.png)

Flash the Reset firmware. Connect each of the three devices (left half, right half, Qube) to the computer one by one. After connecting, quickly double-press the Reset button on the back of the device to put it into bootloader mode. The device will appear in the system as a removable USB drive. Drag and drop the Reset firmware file (settings_reset-ergohaven-zmk.uf2) onto this drive. After copying, the device will automatically reboot.
It is normal to see a warning about a file transfer error or an improper device ejection after copying the firmware. The file has been transferred successfully, but the drive disconnects before the operating system can register the completion of the transfer.

## Step 3: Flashing
Now that all devices are reset, you can install the main firmware. The order here is important!

- Flash Qube. Connect the dongle to the computer, put it into bootloader mode, and copy the corresponding firmware file (op36_qube-ergohaven-zmk.uf2 or similar) to it.
Disconnect Qube from the computer.

- Flash the left half. Connect the left half of the keyboard, put it into bootloader mode, and copy the firmware file for the left side (op36_left_qube-ergohaven-zmk.uf2) to it.
To flash the left half, exclusively use the firmware file named left_qube-ergohaven-zmk.uf2. The exception is the Velvet UI, which uses ui_left-ergohaven-zmk.uf2 for the left half and ui_right_qube-ergohaven-zmk.uf2 for the right half.
Disconnect the left half from the computer.

- Flash the right half. Connect the right half, put it into bootloader mode, and copy its firmware file (op36_right-ergohaven-zmk.uf2) to it.

## Step 4: First power-up and synchronization
All components are flashed. Now they have to be started correctly.

Using a Type-C cable, connect Ergohaven’s Qube to the PC. It will act as a receiver.
Turn on the power on the left half of the keyboard. It should automatically connect to Qube.
Turn on the power on the right half. It will connect to the Qube, completing the setup.
Wait a few seconds. Try typing something. If everything is done correctly, your keyboard is ready to use!

