The Internet is a **network of networks** which allows computers on opposite sides of the globe to communicate with each other. Continents are connected to each other using large international backbone cables. Many of these pass underwater, linking continents to one another.

<u>The TCP/IP Stack and protocol layering</u>

**TCP/IP** stands for **Transmission Control Protocol / Internet Protocol**. A stack of networking protocols that work together passing packets during communication, they work as follows:

- **Application Layer**
	- The application layer is based at the top of the stack. It specifies what protocol needs to be used in order to relate the application that’s being sent.
	- For example, if the application is a browser hosted then it would select a protocol such as **HTTP**, **POP3**, **FTP**, **WebSockets** and so on.
- **Transport Layer**
	- The transport layer uses TCP to establish an end-to-end connection between the source and recipient computer.
	- The transport layer splits data up into packets and labels these packets with their packet number, the total number of packets the original data was split up into and the port number being used for communication.
	- If any packets get lost, the transport layer requests retransmissions of these lost packets.
- **Network Layer**
	- The network layer adds the source and destination IP addresses. (The **combination** of the IP address and the port number is called a **socket address**.)
	- Routers operate on the network layer and the router is what uses the IP addresses to forward the packets.
	- The sockets are then used to specify which device the packets must be sent to and the application being used on that device.
- **Link Layer**
	- The link layer is the connection between the network devices, it adds the **MAC address** identifying the Network Interface Cards of the source and destination computers.
	- For devices on the same network, the destination MAC address is the address of the recipient computer, otherwise, it will be the MAC address of the router.

It’s important to realise that this is really a stack.

On the recipient’s computer these layers are looked at from bottom to top. Once the destination has been reached, the MAC address is removed by the link layer, then the IP addresses are removed by the Network Layer, then the transport layers remove the port number and reassemble the packets. Finally, the application layer presents the data to the recipient in the form it was requested in.

![connections image](https://github.com/MyNameIsNeXTSTEP/WebProgrammingCourse/blob/master/Computer%20science/Connections%20and%20networks/connections.png)