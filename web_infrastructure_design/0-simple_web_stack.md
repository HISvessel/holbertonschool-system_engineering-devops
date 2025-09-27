This file contains a diagram of a one server infrastructure

As you can see, it is quite simple, with everything contained upon a single infrastructure. It is found by searching for the domain www.foobar.com. The dns is the domain name system name, which is an object used to retrieve the specific server IP address with human language instead of numerical notation(since this is harder to search for and remember). The domain name is foobar.com, with www being the CNAME(canoinical name) that points to the domain name and an A name, which points to the IP address. You search for this in a network search bar.

This server is an architecture that contains the following: 
1. a port - the address by which a communication between a server and a client can be established. 

2. an operating system - a software infrastructure component that has computer instructions for computerized operations. 

3. a web server, designed to be the point of interaction once the domain is fetched by searching for it on the web browser. This is the main point of entry and interaction with the application server, commonly known as the API, or application programming interface. 

4. An application server, which is the place where the server logic, source code and port communication from end to end is established. As learned previously, this communication is done by sending http requests and sending http responses to the client. It is also the point of contact with the database. This information can be fetched new or cached for easier finding. 

5. The database, where all the external client information is stored for the customer to access and retrieve, interacts with the application server to recieve incoming requests based on the server web server layer protections. This is the final point of a client request, which sends a response object as data for the application server to display on the web server interface. 


Additionally it also contains a domain name, which is an object used to retrieve the specific port IP address, that directs us to the server in question, without having to remember the exact numerical IP address. 

Purpose and perks:
This single server infrastructure is configured to allow communication with only a single computer. This is very lightweight and allows a small number of customers to send requests and expects responses. Due to it being of a small size, network traffic must be kept to a very reduced number for it to run efficiently. Additionally, maintaining the server is troublesome; since you do not have another server to give service and control traffic while updates and upgrades are being worked on, servers must be offline and clients cannot interact with the server until further notice. Finally, due to containing the whole server in a single hardware or software unit, one small error makes the whole infrastructure fail. 