# Basics of Backend
### What is API
* API stands for **Application Programming Interface.** In the context of APIs, the word Application refers to any software with a distinct function. Interface can be thought of as a contract of service between two applications. This contract defines how the two communicate with each other using requests and responses.      
* APIs are mechanisms that enable two software components to communicate with each other using a set of definitions and protocols. For example, the weather bureau’s software system contains daily weather data. The weather app on your phone “talks” to this system via APIs and shows you daily weather updates on your phone.        

### How do APIs work?
* API architecture is usually explained in terms of client and server. The application sending the request is called the client, and the application sending the response is called the server. So in the weather example, the bureau’s weather database is the server, and the mobile app is the client.     
* Another Example we can give as, When two  different Web Application wants to comunicate with each other they can do with the help of API.           
1. **SOAP APIs**        
These APIs use **Simple Object Access Protocol**. Client and server exchange messages using XML.        
2. **Rest Apis**        
These are the most popular and flexible APIs found on the web today. The client sends requests to the server as data. The server uses this client input to start internal functions and returns output data back to the client. Let’s look at REST APIs in more detail below.       
**[Rest vs SOAP](https://stoplight.io/api-types/vs-rest-api)**      

## Protocols
### HTTP
* HTTP is a protocol for fetching resources such as HTML documents. It is the foundation of any data exchange on the Web and it is a client-server protocol, which means requests are initiated by the recipient, usually the Web browser. A complete document is reconstructed from the different sub-documents fetched, for instance, text, layout description, images, videos, scripts, and more.
* HTTP messages require a reliable transport protocol, such as TCP (Transmission Control Protocol), which provides a reliable and ordered delivery of data, error checking, and congestion control. TCP ensures that all data is delivered correctly and in the correct order, which is essential for the proper functioning of HTTP.
* In summary, HTTP requests cannot be sent through UDP because HTTP requires a reliable transport protocol such as TCP to ensure the correct delivery of data.      
### Here is a list of common features controllable with HTTP:       
#### 1) Proxy and tunneling:     
* Servers or clients are often located on intranets and hide their true IP address from other computers. HTTP requests then go through proxies to cross this network barrier. Not all proxies are HTTP proxies. The SOCKS protocol, for example, operates at a lower level. Other protocols, like ftp, can be handled by these proxies.
* An HTTP proxy is a server that acts as an intermediary between clients and servers. When a client sends a request to a server, the request is first sent to the proxy server, which then forwards the request to the destination server. The response from the server is also sent back to the proxy server, which then forwards it to the client.
* **Difference between HTTP proxy and HTTPS proxy**     
> -> The main difference between an HTTP proxy and an HTTPS proxy is the level of security and encryption they provide. While HTTP proxies are faster and require less computational resources, they do not provide any encryption or security for the data transmitted over them. HTTPS proxies, on the other hand, provide a secure and encrypted connection, ensuring the confidentiality and integrity of the data transmitted between the client, proxy server, and destination server.     
-> **But in both cases proxy server knows what data is passeed throught that request and that is not good**.
* To Secure our data from proxy **HTTP CONNECT** method is used.**HTTP tunneling** technique is enable using **HTTP CONNECT** method. 
* **HTTP tunneling** is often used to bypass firewalls or other network restrictions that block certain types of traffic. For example, if an organization blocks access to certain websites using a firewall, an HTTP tunnel can be used to access those sites by encapsulating HTTP traffic within TCP packets that can bypass the firewall.
* **Difference between forward proxy and  HTTP connect**
| Forward Proxy	      | HTTP Connect |
| ------------------- | ----------- |
| Sits between the client and server | Creates a tunnel between the client and server|
| Intercepts all communication between client and server |Bypasses the proxy for direct communication |
| Can modify the content of the requests and responses	 | Does not modify the content of the requests and responses |
## Reference
* [Proxy servers and tunneling]("https://developer.mozilla.org/en-US/docs/Web/HTTP/Proxy_servers_and_tunneling")