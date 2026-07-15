# Programming nRF91 Series DK firmware

You can program the nRF91 Series DK firmware application and network core firmware over USB.

You can follow this procedure to update the firmware on nRF91 Series DKs using the latest application and modem firmware from the from the [Nordic Semiconductor website](https://www.nordicsemi.com/):

- [nRF9151 DK Downloads](https://www.nordicsemi.com/Products/Development-hardware/nRF9151-DK/Download?lang=en#infotabs)
- [nRF9151 SMA DK Downloads](https://www.nordicsemi.com/Products/Development-hardware/nRF9151-SMA-DK/Download?lang=en#infotabs)
- [nRF9161 DK Downloads](https://www.nordicsemi.com/Products/Development-hardware/nRF9161-DK/Download?lang=en#infotabs)
- [nRF9160 DK Downloads](https://www.nordicsemi.com/Products/Development-hardware/nRF9160-DK/Download#infotabs)

See the `CONTENTS.txt` in the downloaded ZIP archive for the description of the firmware files and their usage.

To program the nRF91 Series DK, you will also need the following USB cables:

* nRF91x1 DK - USB-C cable
* nRF9160 DK - micro-USB cable

!!! tip "Tip"

    If you experience any problems during the process, press `Ctrl+R` (`command+R` on macOS) to restart the Programmer app and try again.

## nRF91x1 DK

To update the modem firmware, application firmware, or NTN firmware, complete the following steps:

1. Open the Programmer app.
2. Connect the DK to the computer with a USB cable, and then turn the DK on.
3. Click **SELECT DEVICE** and select the DK from the drop-down list.<br/>

    ![Programmer - Select device (nRF9151 DK shown)](./screenshots/programmer_select_device_nrf9151.png "Programmer - Select device (nRF9151 DK shown)")

    The drop-down text changes to the type of the selected device, with its SEGGER ID below the name.
    The **Device memory layout** section also changes its name to the device name, and indicates that the device is connected.
    If the **Auto read memory** option is selected in the **J-LINK SETTINGS** section of the side panel, the memory layout will update.
    If it is not selected and you wish to see the memory layout, click **Read** in the **DEVICE** section of the side panel.

4. Click **Add file** in the **FILE** section, and select **Browse**.
5. Navigate to where you extracted the firmware.
6. Check the `CONTENTS.txt` file in the extracted archive for information on which file you need.
7. Select the file to program and click **Open**.
8. Write the firmware to the device. Depending on the firmware type:

    === "Modem and NTN firmware"

        a. Click **Write** in the **DEVICE** section of the side panel.

           ![Programmer - Write (nRF9151 DK shown)](./screenshots/programmer_hex_write_nrf9151.png "Programmer - Write (nRF9151 DK shown)")

           The **Modem DFU** window appears.<br/>

           ![Modem DFU window (nRF9151 DK shown)](./screenshots/programmerapp_modemdfu_nrf9151.png "Modem DFU window (nRF9151 DK shown)")

        b. Click the **Write** button in the **Modem DFU** window to update the firmware.
           Do not unplug or turn off the device during this process.

        When the update is complete, you see a success message.

        !!! note "Note"

            If you experience problems updating the modem firmware, click **Erase all** in the **DEVICE** section of the side panel and try updating again.

    === "Application firmware"

        Click the **Erase & write** button in the **DEVICE** section to program the DK.
        Do not unplug or turn off the DK during this process.<br/>

        ![Programmer - Erase & write (nRF9151 DK shown)](./screenshots/programmer_erasewrite_nrf9151dk.png "Programmer - Erase & write (nRF9151 DK shown)")

## nRF9160 DK

To update the modem or application firmware, complete the following steps:

1. Open the Programmer app.
2. Make sure the **PROG/DEBUG SW10** switch on the nRF9160 DK is set to **nRF91**.
   On DK v0.9.0 and earlier, this is the **SW5** switch.

    For application firmware, set to **nRF91** or **nRF52** as appropriate for the application or sample you are programming.<br/>
    See the [Device programming section in the nRF9160 DK User Guide](https://docs.nordicsemi.com/bundle/ug_nrf9160_dk/page/UG/nrf91_DK/operating_modes/mcu_device_programming.html) for more information.<br/>

    For the [AT Client](https://docs.nordicsemi.com/bundle/ncs-latest/page/nrf/samples/cellular/at_client/README.html) sample, the switch must be set to **nRF91**.

3. Connect the DK to the computer with a USB cable, and then turn the DK on.
4. Click **SELECT DEVICE** and select the DK from the drop-down list.<br/>

    ![Programmer - Select device](./screenshots/programmer_selectdevice_nrf9160.png "Programmer - Select device")

    The drop-down text changes to the type of the selected device, with its SEGGER ID below the name.
    The **Device memory layout** section also changes its name to the device name, and indicates that the device is connected.
    If the **Auto read memory** option is selected in the **J-LINK SETTINGS** section of the side panel, the memory layout will update.
    If it is not selected and you wish to see the memory layout, click **Read** in the **DEVICE** section of the side panel.

5. Click **Add file** in the **FILE** section, and select **Browse**.
6. Navigate to where you extracted the firmware.
7. Check the `CONTENTS.txt` file in the extracted archive for information on which file you need.
8. Select the file to program and click **Open**.
9. Write the firmware to the device. Depending on the firmware type:

    === "Modem firmware"

        a. Click **Write** in the **DEVICE** section of the side panel.<br/>

           ![Programmer - Write](./screenshots/programmer_write_nrf9160dk.png "Programmer - Write")

           The **Modem DFU** window appears.<br/>

           ![Modem DFU window](./screenshots/programmerapp_modemdfu.png "Modem DFU window")

        b. Click the **Write** button in the **Modem DFU** window to update the firmware.
           Do not unplug or turn off the device during this process.

        When the update is complete, you see a success message.

        !!! note "Note"

            If you experience problems updating the modem firmware, click **Erase all** in the **DEVICE** section of the side panel and try updating again.

    === "Application firmware"

        Click the **Erase & write** button in the **DEVICE** section to program the DK.
        Do not unplug or turn off the DK during this process.<br/>

        ![Programmer - Erase & write](./screenshots/programmer_erasewrite_nrf9160dk.png "Programmer - Erase & write")
