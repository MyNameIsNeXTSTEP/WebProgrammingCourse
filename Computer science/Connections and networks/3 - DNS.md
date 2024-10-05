The **domain name system (DNS)** - is the system used to name and organise internet resources. It is a hierarchy, in which each smaller domain is separated from the larger domain by a full stop.

For example, `www.google.com`. Here the TLD is `com`, and the 2LD is `google` (world wide web)

**TLD** stands for **Top Level Domain**, and **2LD** stands for **2nd Level Domain**. Domain names are much easier to remember than IP addresses, which is why they are used to link to servers across the world. The role of the domain name system server (DNS server) is to translate these domain names into IP addresses when we wish to access a website.

![connections image](https://github.com/MyNameIsNeXTSTEP/WebProgrammingCourse/blob/master/Computer%20science/Connections%20and%20networks/url.png)

When you type a domain name into your browser, it sends a query to a DNS server — a computer that stores information about domain names and IP addresses. 
The DNS server then follows the DNS hierarchy to find the IP address that matches the domain name. 

For example, if you type www.example.com, the DNS server will first ask the root server for the IP address of .com, then ask the .com server for the IP address of example, and then ask the example server for the IP address of www.
This process is called DNS resolution.

And of course there's also a caching mechanism to it, so after first request to the specified domain the computer caches its related ip adress and port combination in a internal storage of cached DNS records.

---

A more detailed short voew on DNS maybe found here, for example - https://www.semrush.com/blog/top-level-domains/