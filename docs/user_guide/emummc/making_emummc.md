# Making the Emummc, getting keys, and making essential backups 

&nbsp;

### Making the emuMMC

!!!warning "Before you start"
    If you don't plan on using the internet on your emuMMC, it is recommended to boot your switch normally and delete all the wifi networks. You can add them back to your sysnand after completing this guide.

!!!tip ""
    1. Enter RCM and inject the Hekate payload
    2. Use the touch screen to navigate to `emuMMC`
    3. Tap on `Create emuMMC`, then select `SD Partition`
    4. Tap on `Part 1`. It will start making the emuMMC now. After it's done return to the emuMMC menu using the `Close` buttons
    5. Tap on `Change emuMMC`, then `SD RAW 1`
    6. Go back to the main menu

!!!warning "After making the emummc"
    Beware that sysMMC and emuMMC don't use the same Nintendo folder! Once you created your emuMMC, copy the `Nintendo` folder from the root of the sd card to the `emummc/RAW1/` folder.

-----

### Making a NAND backup


!!! danger "Important"
    A NAND backup is crucial. They can be used to restore the device to a working state in case of emergencies.

	Once the backup is finished, **keep it somewhere safe.** The best backup is the one you have but never need, and the worst backup is the one you need but never made. To save space, it's recommended to compress the end-result with a `.zip` file or something similar.

	It's highly recommended that you use an SD card that is formatted to FAT32 and has at least 32 gigabytes of space free. This will still work on smaller cards, but it's not ideal.

### Instructions

!!! tip ""
    1. Enter RCM and inject the Hekate payload
    2. Use the touch screen to navigate to `Tools` and then `Backup eMMC`
    3. Tap on `eMMC BOOT0 & BOOT1`
       - This should only take a few seconds, but if your SD card is very slow, it may take around a minute.
    4. Tap on `Close` to continue, then tap on `eMMC RAW GPP`
       - This will take a long time. Expect it to take between 10 minutes to an hour (or more, if your SD card is very slow).
       - On FAT32 SD cards or cards that have less than 32 gigabytes of space available, the NAND will be split into 1 or 2 gigabyte parts.
          - Hekate will stop producing these parts when it runs out of space. When this happens, do the following:
          - Power off your system
          - Insert your SD card into your PC
          - Move all files from the `backup` folder on your SD card to a safe location on your PC
          - Insert your SD card into your Switch
          - Enter RCM again, inject Hekate again, and continue the backup by tapping on `Tools` > `Backup eMMC` > `eMMC RAW GPP`
          - Repeat the process until the NAND is completely dumped
    5. Press `Close` > `Home` > `Power Off`
    6. Insert your SD card into your PC
    7. Copy the `backup` folder on your SD card to a safe location on your PC

&nbsp;

-----

### Getting your Console's Unique Keys

!!! danger "Important"
    These keys are critical to have. In an extreme emergency, they can be used in conjunction with your NAND backup and other tools to restore your console to a working state.

!!!tip ""
    1. Enter RCM and inject the Hekate payload.
    2. Tap the `Payloads` option, then press Lockpick_RCM.bin.
    3. If Lockpick_RCM asks you to select between SysNAND or EmuNAND, choose SysNAND by navigating with the volume buttons and pressing the power button. If not, continue with step 4.
    4. Lockpick_RCM should now inform you that your keys have been saved to `/switch/prod.keys` on the SD card.
    5. Press any button to return to the main menu.
    6. Navigate to 'Power off' with the volume buttons and select it with the power button.
    7. Insert your SD card into your PC.
    8. Copy `prod.keys` from the `switch` folder on your SD card to a safe location on your PC (it is suggested to copy it to the same place that you copied your NAND backup to).

&nbsp;

#### [Continue to Launching CFW <i class="fa fa-arrow-circle-right fa-lg"></i>](launching_cfw.md)
