<u>Data Packets</u>

Packets are **segments of data**. They contain various information:
- **Header**:
	- Sender and recipient **IP addresses**.
	  The sender and the recipient’s IP addresses act like a postcode, allowing the packet to be delivered to the correct destination and enabling the recipient device to trace where the packet came from.
	- **Protocol** being used.
	  The protocol allows the recipient computer to understand how to interpret the packet.
	- **Order** of the packets.
	  Upon arriving at the recipient device, packets are reconstructed in the appropriate order as specified in the header.
	- **Time To Live / Hop Limit The Time To Live (TTL)**
	  Tells the packet when to expire so that it does not travel forever.
- **Payload**:
	- Raw data to be transmitted.
	  Formats may differ, for example, in HTTP it might be: binary, JSON, XML, plain text
- **Trailer**:
	- Checksum, or cyclic redundancy check.
	  The trailer contains a code used to detect whether any errors have occurred during transmission, or is the data transmitted valid and trustable if any conditions should check it.