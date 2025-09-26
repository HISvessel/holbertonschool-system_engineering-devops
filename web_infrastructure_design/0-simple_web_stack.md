This file contains a diagram of a one server infrastructure

As you can see, it is quite simple, with everything contained upon a single infrastructure. This server is an architecture that contains a port, an operating system, the codebase and a database. 

Additionally it also contains a domain name, which is an object used to retrieve the specific port IP address, that directs us to the server in question, without having to remember the exact numerical IP address. 

Here are some of the things it contains:
1. a web server, designed to be the point of interaction once the domain is fetched by searching for it on the web browser. This is the main point of entry and interaction with the application server, commonly known as the API, or application programming interface. 
2. An application server, which is the place where the server logic, source code and port communication from end to end is established. As learned previously, this communication is done by sending http requests and sending http responses to the client. It is also the point of contact with the database. This information can be fetched new or cached for easier finding. 
3. The database, where all the external client information is stored for the customer to access and retrieve, interacts with the application server to recieve incoming requests based on the server web server layer protections. This is the final point of a client request, which sends a response object as data for the application server to display on the web server interface. 