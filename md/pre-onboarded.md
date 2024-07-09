# Replace the generated key with one already onboarded

1. Go to the `LoRaWAN` tab.
2. Click on `Helium IoT`.
3. Navigate to `Upload gateway-rs key` and upload the `gateway_key.bin` then click `Upload_Hotspot_Key`.
4. Click on `Save&Apply` to save the settings.

The `gateway_key.bin` file contains the private key for a Helium gateway. This key is used for authentication on the Helium network and for minting an NFT on the Solana blockchain to represent the gateway. IOT tokens can be earned through data relay, and the gateway's coverage can be mapped by external parties. The file essentially serves as the gateway's digital identity.

# Disable WiFi Client and AP

Once the gateway is configured, it is recommended to disable the WiFi client and access point to prevent unauthorized access to the gateway. This can be done by navigating to the `Network` tab, then `WiFi` and unchecking the `Enable` box for both the `WiFi Access Point` and `WiFi WAN Client` sections. Click on `Save&Apply` to save the settings. From now on, the gateway will only be accessible through the Ethernet port and its fallback IP address (`172.31.255.254`). More on page 44 in the [Dragino DLOS8N Outdoor LoRaWAN Gateway User Manual](</docs/Dragino%20DLOS8N%20Gateway%20User%20Manual%20(EN).pdf>).

![alt text](/images/wifi_ap.png)
