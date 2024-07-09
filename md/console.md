# Create and configure a console account

There are many helium consoles available, and we will use [console.helium-iot](https://console.helium-iot.xyz)

## Create an account

1. Go to https://console.helium-iot.xyz/front/login
2. Click on `No Account? Signup!`
3. Fill in the required fields and click on `Register`

## Configure device profile

Ensure you're logged in to the console.

1. Navigate to `Device Profiles` in the left-hand menu.
2. Click on `Add Device Profile`.
3. Fill in the required fields (no need to change anything here). See the image below.
4. Click on `Submit`.

![alt text](/images/device_profile.png)

## Add a device

Ensure that you have the `DEV EUI`, `App EUI`, and `App Key` from the device(s) that you intend to use at hand.

1. Navigate to `Applications` in the left-hand menu.
2. Create an application by clicking on `Add Application`.
3. Fill in the required fields and click on `Submit`.
4. Click on `Add Device`.
5. Fill in the required fields. `Name`, `DEV EUI`, `App EUI`, and the `Device Profile` previously created are required.
6. Click on `Submit`.
7. Fill in the `App Key` and click on `Submit`. You will be redirected to the device overview page.
8. Click on `LoRaWAN frames` to see the frames sent by the device.
9. Activate the LoRaWAN Sensor and you will soon see the frames sent by the device.
