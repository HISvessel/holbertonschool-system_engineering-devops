This repository ha task to learn and dominate web infrastructure

These are the concepts that we will discuss
1. Netowrking basics
2. Server
3. Web Server
4. DNS
5. Load balancer
6. Monitoring

a) Networking basics
    This is a big part of computers being so powerful and why the internet exists. It enables communications between each other. 
    1) network protocol:
    this is a set of established rules that specify how to format, send and recieve data so that computer network endpoints(computers, servers, routers virtual machines) can communicate despite their differences. To have this exchange in data, both endpoints must adhere to the same established protocols, built into either the software, hardware or both. 

    protocol models: protocol models exist to break large processes into discrete, narrowly defined functions and tasks across every level of the network.
        I. OSI models: a network protocol divided into 7 different concrete and abstract layers. Lower layers deal with the transport of data, higher layers deal with software and application.
        -> Physical Layer: establishes the physical connection adn deals with hardware components, such as the Network interface cards, coltage levels, cables, modems, routers, etc. 
        -> Data link layer: is responsible for the error free delivery of data from one node to the other over the physical layer. 
        -> Network layer: this is the layer concerned with information flow regulation, switching and routing between workstations.
        -> Transport Layer: this layer transfers services from the network layer to the application layer and breaks down data into data frames for error checking at the network segment level. 
        -> Session layer: establishes a connection between  two worksyations that need to communicate. In addition to ensuring security, this lauer oversees connection estalishment, session maintenance and authentication.
        -> Presentation layer: also known as the translation layer, it retrieves the data from the application layer and formats it for transmissino over the network.
        -> Application layer: the topmost layer of the network, relaying application requests to the lower levels. 

        II. TCP/IP model:this is a set of protocols method called a suite. This paeticular suite is commonly used in client-server models and includes numerous protocols across layers, such as the data, network, transport and application layers, working together to enable internet connectivity. 

        it uses the following concepts:
        -> tcp, which uses a set of rules to exchange messages with other internet points at the information packet level. 
        -> udp, which acts as an alternative to the tcp, making it more tolerable to lost connections and lower latency. 
        -> ip, which uses a set of rules to send and recieve messages at the level of ip addresses. 
        -> http: hypertext transfer protocol, it speaks of how internet pages communicate with each other, and pass requests and responses that redirect and connect pages together.
        -> ftp: file transfer protocol

        tcp/ip follows only four layers instead of seven:
        -> Application layer: the topmost layer, is responsible for providing with access to network resources.
        -> Transport layer: this layter ensures that segments are transmitted correctly via the communication channel. 
        -> Internet layer: this layer sends and recieves packets for the network, such as IPs, ARPs and ICMPs.
        -> Network access layer: combines the physical and data-link layers of the OSI model.


     2) IP address: it is the unique identifier for the computer that follows the TCP IP protocol for network communication. It has two different versions:
        IPv4: an ip address version that all computers have. It uses 32 binary bits to create a single unique address on the network. ex. 216.27.61.137
        IPv6: it uses 128 binary bits to create a single unique address on the network. The address is represented by eight groups of hexadecimals numbers separated by colons. ex. 2001:cdba:0000:0000:0000:0000:3257:9652
    The transition from Ipv4 to Ipv6 came with the expansion of the internet. v4 could offer only 232 different combinations, offering just under 4.3 billion unique addresses. v6 came to fix this, which provided 2128 possible combinations, giving more unique identifiers for hardware and software connections that bump up to the trillions. AN IP can be dynamic or static. Statics are permanently assigned addresses that can be assigned to devices on the local network or, on rarer occasions, by the internet service provider. It can create network issues if done without understanding TCP/IP. Dynamic IP addresses are most common, and are assigned by the Dynamic Host Configuration Protocol, which is a service running on the network that runs on network hardware such as a router or dedicated DHCP server. Dynamic IP addresses are leased and assigned temporarily and are active for a limited time. If it expires, it will request a new lease. 

    The numbers could be represented somewhere between 00000000 to 11111111, or from 0 to 255. In other words, 0.0.0.0 to 255.255.255.255 is the valid range of numbers in the IPv4 address. 
    -> 0.0.0.0 represents the default network.
    -> 255.255.255.255 is reserved for network broadcasts, or messages that should go to all computers.
    -> 127.0.0.1 is called the loopback address, or in other words, the computers way of identifying itself, whether it has an IP address or not.
    -> 169.254.0.1 to 169.254.255.254: This is the Automatic Private IP Addressing (APIPA) range of addresses assigned automatically when a computer's unsuccessful getting an address from a DHCP server.

    Other IP addresses are reserved for subnet classes. A subnet class is a smaller network of computers conected to a larger network through a router and can have its own address system so computers on the same subnet can communicate quickly without sending data across the larger network. The following addresses are reserved for subnets:
    -> 10.0.0.0 to 10.255.255.255: This falls within the Class A address range of 1.0.0.0 to 127.0.0.0, in which the first bit is 0.
    -> 172.16.0.0 to 172.31.255.255: This falls within the Class B address range of 128.0.0.0 to 191.255.0.0, in which the first two bits are 10.
    -> 192.168.0.0 to 192.168.255.255: This falls within the Class C range of 192.0.0.0 through 223.255.255.0, in which the first three bits are 110.
    -> Multicast (formerly called Class D): The first four bits in the address are 1110, with addresses ranging from 224.0.0.0 to 239.255.255.255.
    -> Reserved for future/experimental use (formerly called Class E) : addresses 240.0.0.0 to 254.255.255.254.

Network functionality:
    the network is the one that establishes the communication between the server(the one hosting the service) and the customer(the one soliciting the service from the server.)
    A protocol is set as rules, with these rules being the layers through which the information or service requested is sent from the host hardware to the customer software, the final end goal of the communication chain. 


b) Server
    Servers are located in datacenter, which are buildings that host up to thousands of computers(servers). These computers are just the port, only accessible by a network, and can be physical or virtual. Additionally, a server runs an Operating System(OS).

Server components:
    Case, RAM, Keyboard, Network connection, Motherboard, Hard Drive, Mouse, Operating System, CPU, Video Card, Screen and Applications. Everything a computer has is a server component.

Server functionality:
    In a web infrastructure, servers provide the service, and everyone that connects to the network obtains a service from the server. And the source of the service exists in the Operating System, so that OS is the primary component of a server.

Dynamic Service: 
    the software system that stores organizes and provides access to information in a computer's OS directory. 

c) DNS: 
    stands for Dynamic Name Service and serves the function of translating a      domain name into an IP address. It's a method used to simplify the IP address you are looking for by typing the host's domain name instead of the exact IP address you are looking for(which you may not know or want to remember.)

    Storage of domains:
    All website domains are first checked on the OS, search engine and resolver's cached data system to find them by their own memory. If they do not know it, they go to the ISP(internet service provider)'s root TLD(top level domain) server to find the appropriate domains suffix(.COM, .NET, .GOV, .EDU, etc.), and in its relative path, find the correct domain name in the domain registrar contained for that TLD. 

    Search goal: run a search and obtain the server port attached to the domain name, which gives us access to its server. Simply put, we use the domain, search for its name in the quickest access point(cached in the searcher, resolver or TLD relative path for the domain registrar) and the domain name will give us the IP address we need to communicate with the server. 

d) Web server:
    provides a service for hosting and managing websites. Routes the traffic and provides the services in websites. They are accessed by users via a web browser.

e) Proxy Server
    a standalone intermediate between the endpoint device and the server the endpoint device is requesting from. Pertinent to add for the security component, ensure that only people located in the correct layer and the correct service or infrastructure can create requests. This layer of the server communicates with the firewall to ensure security.

f) firewall service:
    server monitors that exclude access to servers by blocking IP addressess in the netwrk traffic. It does so by establishing its own set of rules and monitors. It should be balanced and well administrated, where the correct traffic is allowed in and provided services while blocking those who you do not want having access tonthat sofware.

