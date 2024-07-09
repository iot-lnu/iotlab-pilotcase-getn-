# DLOS8 Firmware update

To update the firmware on the Dragino DLOS8N Outdoor LoRaWAN Gateway, follow these steps:

1. Power on the gateway and connect to the AP it expose (`dragino-xxxxxx`). Password is `dragino+dragino`.
2. Once connected, visit the Gateway home page at `10.130.1.1`.
3. Download the latest firmware from the [Dragino Download Server](https://www.dragino.com/downloads/index.php?dir=LoRa_Gateway/DLOS8/).
4. Extract the firmware file (**lgw--build--vX.X** found under firmware/release).
5. From `10.130.1.1`, navigate to `System->Firmware Upgrade`
6. Click on `Choose file` and select the firmware file you downloaded and click `Upload`.
7. Wait for the file to be uploaded. In the meantime, you will see some checksums being calculated and displayed. See image below.
8. Finally, click `Proceed` to start the firmware update.
9. Wait for the firmware to be updated. You will disconnect from the gateway during the update process. Wait for the gateway to reboot and reconnect to the AP.

![alt text](/images/fw_upgrade.png)
