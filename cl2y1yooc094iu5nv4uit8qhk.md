## Security of your web application: Why exactly do we need HTTPS? Learn how Presear Software can help!

### **What is HTTP?**

HTTP stands for Hypertext Transfer Protocol, of stateless protocol that transfers information between the clients and the webserver. 

However, HTTP takes no measure to secure the data of the user. Despite decreased security, there are potential benefits that HTTP brings. Hence, HTTP is most often preferred by websites that do not have any confidential information.

Since the data is delivered in plain text, anyone can read your data by programming the hub/switch easily because they own and have physical access to it, or by wiretapping the cable itself coming into that ARP table.
When an origin server receives an HTTP request, it sends an HTTP response, which is similar:

```
HTTP/1.1 200 OK
Date: Wed, 30 Jan 2019 12:14:39 
GMTServer: Apache
Last-Modified: Mon, 05 Apr 2022 11:17:01 
GMTAccept-Ranges: bytes
Content-Length: 12
Vary: Accept-Encoding
Content-Type: text/plain

``` 
The attacker sees something like:

```
Hello World!
``` 
HENCE, WE CAN SAY IT HAS **BAD HTTP!**

### **How does HTTPS overrule HTTP?**

So, in order to overcome this data confidentiality and data integrity issue, the letter *'S'* stands for secure. HTTPS encrypts HTTP requests and responses with TLS (or SSL), so an attacker would see a series of seemingly random characters instead of the text. In other words, no one in the middle can sniff your traffic.


```
GET /hello.txt HTTP/1.1
User-Agent: curl/7.63.0 libcurl/7.63.0 OpenSSL/1.1.l zlib/1.2.11
Host: www.example.com
Accept-Language: en

``` 
The attacker sees something like:

```
t8Fw6T8UV81pQfyhDkhebbz7+oiwldr1j2gHBB3L3RFTRsQCpaSnSBZ78Vme+DpDVJPvZdZUZHpzbbcqmSW1+3xXGsERHg9YDmpYk0VVDiRvw1H5miNieJeJ/FNUjgH0BmVRWII6+T4MnDwmCMZUI/orxP3HGwYCSIvyzS3MpmmSe4iaWKCOHQ==
``` 

### **How does HTTPS work?**

The HTTPS in the web browser indicates that your communication with the server is encrypted. Data is encrypted with a unique symmetric key and delivered from client to server; the server receives the encrypted data as well as the key used to decrypt the data. This is process is called TLS handshakes.

There is one problem left with the above process, any man in the middle can obtain a certificate and pretend to be the origin server, sending harmful content to the browser or gaining access to the encrypted data and decrypting it using the key.


To fix this problem, the server transmits its public key to the browser along with the domain name encoded in a certificate, and the browser sends back a pre-master secret key encrypted with the server's public key. To retrieve the pre-master secret key, the server decrypts the encrypted communication with its private key. Both the browser and the server now convert the pre-master key into the master secret key, which is eventually used for encryption of all future server-browser communications.


In terms of the certificates used in this process, browsers guarantee that they are embedded with information that allows them to determine which certificates are legitimate. In simple words, certificate authorities are well-known organizations that everyone knows are trustworthy (it all boils down to trust). If there is no such signature in the certificate, the browser will tell the user that the connection is not HTTPS. The server, on the other hand, must physically authenticate their identity in order to obtain the signed certificate from one of the certificate authorities (by sending docs, etc.).

#### **As we all know, HTTPS works, the main question that arises is: "How can we get HTTPS for our website?"**

TLS stands for Transport Layer Security, and it protects data privacy in the same way as SSL does. Because SSL is no longer in use, this is the correct word that people should begin using TLS. Websites that install and set up an SSL/TLS certificate can utilize the HTTPS protocol to connect to the server in a secure manner.

### **Why is HTTPS or SSL/TLC imported for a website?**

There are three key reasons why SSL/TLS is essential for your website:
- 	**When you need to authenticate something:** Any server can appear to be your server, intercepting the data that people send along the route. SSL/TLS allows you to prove your server's identity so that people know you are who you say you are.
-  **To implant trust:** If you're running an e-commerce site or asking customers for sensitive information, you must instill trust in them. Using an SSL/TLS certificate is a tangible approach to demonstrate to visitors that they can trust you, and it is far more effective than anything you might say about yourself.
- **When it is necessary to adhere to industry standards:** Some businesses, such as finance, will need you to maintain certain baseline levels of security. If you want to accept credit card information on your website, you must also follow Payment Card Industry (PCI) requirements. The use of an SSL/TLS certificate is one of those prerequisites.


### **Future of HTTPS**

When compared to HTTP, HTTPS unquestionably outperforms HTTP in terms of data privacy and security.

The availability of HTTPS does not imply that a website is authentic. Some astute phishers have noticed that consumers look for the HTTPS indication and lock icon, and they may go to great lengths to conceal their websites. Certificates are also available for scammers' scam servers. Other scammers may try to fool you by altering their website's favicon (the icon that appears in the URL bar) to a lock. When monitoring your connection to a website, keep a watch out for these techniques.

In addition, all browsers should force HTTPS, which means they should reject the request if it is not. Currently, this is accomplished through the use of the HSTS preload list, which is optional for websites to use; however, it would be ideal if all websites were required to use HTTPS. End-user security would be improved as a result of this. Many people are advocating for the switch to HTTPS everywhere.

### How Presear softwares can help with an SSL certificate?
Presear software provides a free SSL certificate for a duration of 15 years powered by Cloudfare, the features of such an SSL certificate are as follows,

- *Custom Certificates* - Cloudflare automatically provisions SSL certificates that are shared by multiple customer domains. Business and Enterprise customers have the option to upload a custom, dedicated SSL certificate that will be presented to end-users. This allows the use of extended validation (EV) and organization validated (OV) certificates.
- *Modern TLS Only* - PCI 3.2 compliance requires either TLS 1.2 or 1.3, as there are known vulnerabilities in all earlier versions of TLS and SSL. Cloudflare provides a “Modern TLS Only” option that forces all HTTPS traffic from your website to be served over either TLS 1.2 or 1.3.
- *Opportunistic Encryption* - Opportunistic Encryption provides HTTP-only domains that can't upgrade to HTTPS, due to mixed content or other legacy issues, the benefits of encryption and web optimization features only available using TLS without changing a single line of code.
- *TLS Client Auth* - Cloudflare’s Mutual Auth (TLS Client Auth) creates a secure connection between a client, like an IoT device or a mobile app, and its origin. When a client attempts to establish a connection with its origin server, Cloudflare validates the device’s certificate to check it has authorized access to the endpoint. If the device has a valid client certificate, like having the correct key to enter a building, the device is able to establish a secure connection. If the device’s certificate is missing, expired, or invalid, the connection is revoked and Cloudflare returns a 403 error.
- *HSTS* - Supporting the HTTP Strict Transport Security (HSTS) protocol is one of the easiest ways to better secure your website, API, or mobile application. HSTS is an extension to the HTTP protocol that forces clients to use secure connections for every request to your origin server. Cloudflare provides HSTS support with the click of a button.
- *Automatic HTTPS Rewrites* - Automatic HTTPS Rewrites safely eliminates mixed content issues while enhancing performance and security by rewriting insecure URLs dynamically from known (secure) hosts to their secure counterpart. By enforcing a secure connection, Automatic HTTPS Rewrites enables you to take advantage of the latest security standards and web optimization features only available over HTTPS.
_ *Encrypted Server Name Indicator (SNI)* - Encrypted SNI replaces the plaintext “server_name” extension used in the ClientHello message during TLS negotiation with an “encrypted_server_name.” This capability expands on TLS 1.3, increasing the privacy of users by concealing the destination hostname from intermediaries between the visitor and website.
- *Geo Key Manager* - Geo Key Manager provides the ability to choose which Cloudflare data centers have access to private keys in order to establish HTTPS connections. Cloudflare has preconfigured options to select from either US or EU data centers as well as the highest security data centers in the Cloudflare network. Data centers without access to private keys can still terminate TLS, but they will experience a slight initial delay when contacting the nearest Cloudflare data center storing the private key.

Cloudflare SSL operates in different modes depending on the level of security required and the amount of configuration you’re willing to do. Traffic to the end user will always be encrypted, which means your website will always enjoy the benefits of HTTPS. However, traffic between Cloudflare and your origin server can be configured in a variety of ways.

Source - [Cloudfare](https://www.cloudflare.com/en-gb/ssl/)

**For understanding how Presear Softwares can help you more feel free to mail us your project idea or the problem statement at support@presear.com**


