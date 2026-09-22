Ethernet communications are established by either electrical signaling over copper twisted  cables or pulses of light transmitted over fiber optic cable. The physical connection to the cable is made using a transceiver port in the computer's network interface card (NIC). The majority of PC motherboards today have a built-in 1000BASE-T compatible adapter.

- You might use a NIC adapter card to support other types of Ethernet, such as fiber optic.
- You can also get cards with multiple of the same port.
- The multiple ports can be bonded to create a higher-speed link. Four Gigabit Ethernet ports could be bonded to give a nominal link speed of 4 Gbps.
- For the NIC to be able to process the electrical or light signals as digital data, the signals must be divided into regular units with a consistent format.
- Ethernet allows nodes on a LAN to comunicate with each other and interpret the light/electrical siganals.
- Each Ethernet NIC port has a unique media access control (MAC) adress.  Each frame of Ethernet data identifies the source MAC address and destination MAC address in fields in a header.

	- **Captured Ethernet frame showing the destination and source MAC addresses. The destination address is a broadcast address**![A screenshot of the Wireshark network protocol analyzer capturing packets from a network interface.](https://cdn.testout.com/a-plus-220-120x-en-us/materials/resources/text/s_networking_hardware/7431-1636621539755-wireshark_frame_fields_example.png)


- A MAC address consists of 48 binary digits, making it six bytes in size. A MAC address is typically represented as 12 digits of hexadecimal.
- A MAC address is typically written out with a colon separating every two digits. They may occasionally use a hyphen or no separator - for example, `00:60:8C:12:3A:BC` or `00608C123ABC`.
- A MAC address is broken into two distinct parts:

	- The first 24 bits are known as the **Organizationally Unique Identifier (OUI)**. This identifies the manufacturer of the NIC.
	    
	- The last 24 bits are known as the **Network Interface Controller (NIC) Specific**. This is a unique identifier for each NIC.
- When you convert the first two hex digits of a MAC address to binary, the two right-most bits act as flags. 
- The very last bit shows individual (0) versus group / multicast (1). 
- The bit just to its left shows universally administered (0, factory) versus locally administered (1, set by software). 