# iotlab-pilotcase-getno

- [iotlab-pilotcase-getno](#iotlab-pilotcase-getno)
  - [LoRaWAN Gateway](#lorawan-gateway)
  - [LoRaWAN Sensors](#lorawan-sensors)
    - [Electricity meters](#electricity-meters)
  - [Getting started](#getting-started)
  - [Maintenance](#maintenance)
    - [Keep DC balance above 0](#keep-dc-balance-above-0)

## LoRaWAN Gateway

The gateway we will use in the pilot case is the Dragino DLOS8N Outdoor LoRaWAN Gateway (8 channels). The gateway is IP65-rated and can be mounted on a pole or wall.

| <img src="images/lorawan_gateway.png" width="145" height="100"> | Dragino DLOS8N Outdoor LoRaWAN Gateway | [€297.38 - Dragino DLOS8N Outdoor LoRaWAN Gateway](https://iot-shop.de/en/shop/dragino-dlos8n-outdoor-lorawan-gateway-5841?category=7&search=LoRaWAN+Gateway#attr=17051,20022,6145,20023,14699) |
| --------------------------------------------------------------- | -------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

## LoRaWAN Sensor(s)

| Image                                                 | Product Name                             | Description                                                             | Price and Link                                                                                                                                                                                         |
| ----------------------------------------------------- | ---------------------------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <img src="images/EM300.png" width="145" height="100"> | Milesight EM300-DI LoRaWAN Pulse Counter | LoRaWAN sensor that counts pulses and measures temperature and humidity | [€58.90 - Milesight EM300-DI LoRaWAN Pulse Counter](https://iot-shop.de/en/shop/mil-em300-di-milesight-em300-di-lorawan-pulse-counter-6132#attr=22806,19024,19025,19019,19020,19021,19022,19653,14871) |

### Electricity meters

The following table lists all 12 electricity meters with their respective meter numbers, meter types, and status.

| NR. | Cottage         | Brand and model | Status: | Note: |
| --- | --------------- | --------------- | ------- | ----- |
| 3   | Gäddstugan      | Garo GMN3D      | ok      |       |
| 4   | Fågelstugan     | Garo GMN3D      | ok      |       |
| 5   | Abborrestugan   | Garo GMN3D      | ok      |       |
| 8   | Hönshuset       | Garo GMN3D      | ok      |       |
| 12  | Rättarebostaden | ABB OD4165      | ok      |       |
| 13  | Grytet          | ABB 0D4165      | ok      |       |
| 14  | Älgen           | Garo GMN3D      | ok      |       |
| 15  | Rådjuret        | Garo GMN3D      | ok      |       |
| 16  | Räven           | Garo GMN3D      | ok      |       |
| 17  | Haren           | Garo GMN3D      | ok      |       |
| 18  | Kronhjorten     | Garo GMN3D      | ok      |       |

## Getting startedi

[Here](https://resource.milesight.com/milesight/iot/document/em300-series-user-guide-en.pdf) is the user guide for the sensor.

1. Update the firmware on the Dragino DLOS8N Outdoor LoRaWAN Gateway, visit [this guide](md/firmware.md).

2. Configure the Dragino DLOS8N Outdoor LoRaWAN Gateway for the Helium network, visit [this guide](md/helium.md).

3. Use the pre-onboarded key, visit [this guide](md/pre-onboarded.md).

4. Log into helium console (chirpstack), visit [this guide](md/console.md).

5. Map the coverage of the gateway, visit [this guide](md/coverage.md).

**Notice:** The value for the pulse is called `water` in the decoder.

## Datacake integration

To integrate the data from the sensors to Datacake, follow the steps below.

## Maintenance

To keep the whole system running, there are a few things to keep in mind.

### Keep DC balance above 0

Every time a sensors sends a message (uplink), the Data Credit (DC) balance is decreased. The size of the message determines how many DCs are used. One Data Credit equals $0.00001 USD or 0,00011 SEK.

| Byte Range  | Number of DCs |
| ----------- | ------------- |
| 0-24 bytes  | 1 DC          |
| 25-48 bytes | 2 DC          |
| ...         | ...           |
| 241 bytes   | 11 DC         |

This table presents the relationship between byte ranges and the corresponding number of DCs (presumably "Data Cells" or similar). More on that in the [DC Documentation page](https://docs.helium.com/tokens/data-credit/).

## Lora coverage

The gateway is was installed on top of the reception building.

here is a image of the coverage map
TODO: ADD points on the map for the locations for the motions sensors.
![coverage map](images/covrage_map.png)

For the area with the cabins which is relative close the the gateway the coverage is good.
There is two spots in the island that is of interest for a motion detection sensor. One of the spots had relative bad coverage and the other spot had not coverage at all. On the way to the point on the north side of the island the signal diapered about a third of the way there. As we did the coverage test in the fall season there is no guarantee that there will be coverage in the summer sine the trees will have leaves.
