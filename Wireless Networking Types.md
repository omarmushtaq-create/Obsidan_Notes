-  [[Access Points]]
- [[Frequency Bands]]
- [[IEEE 802.11a]]
- [[IEEE 802.11b-g]]
- [[802.11n]]
- [[Wi-Fi 5 and Wi-Fi 6]]
- [[Wi-Fi 7 (802.11be)]]
- [[Wireless LAN Installation Considerations]]
- 


Clients identify an infrastructure WLAN through the network name or service set identi(SSID) configured on the access point. An SSID can be up to 32 bytes in length and, for maximum compatibility, should only use ASCII letters and digits plus the hyphen and underscore characters.

Configuring an access point![A screenshot of the T P-Link Archer V R 900 router's web-based interface displays the Wireless Settings page under the Advanced tab.](https://cdn.testout.com/a-plus-220-120x-en-us/materials/resources/text/s_wireless_networking_types/9986-1637605645920-ap_configuration.png)

Screenshot courtesy of TP-Link.

Description

When configuring an access point, you need to choose whether to use the same or different network names for both frequency bands. If you use the same SSID, the access point and client device will use a probe to select the band with the strongest signal. If you configure separate names, the user can choose which network and band to use.

For each frequency band, you also need to select the operation mode. This determines compatibility with older standards and support for legacy client devices. Supporting older devices can reduce performance for all stations.

Finally, for each frequency band, you need to configure the channel number and whether to use channel bonding. If there are multiple access points whose ranges overlap, they should be configured to use nonoverlapping channels to avoid interference. An access point can be left to autoconfigure the best channel, but this does not always work well. You can configure wide channels (bonding) for more bandwidth, but this has the risk of increased interference if there are multiple nearby wireless networks. Channel bonding may only be practical in the 5 GHz band, depending on the wireless site design.

Note:

Along with the Wi-Fi frequency band and channel settings, you should also configure security parameters to control who is allowed to connect.
