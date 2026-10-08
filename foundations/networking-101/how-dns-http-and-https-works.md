# How DNS, HTTP and HTTPS works

## 1. Domain Name System (DNS): The Phonebook of the Internet

* You type in a domain name (like [www.example.com](https://www.example.com/)) into your web browser's address bar.
* Your computer doesn't understand domain names, it needs an IP address. Think of DNS as a giant phonebook. Your computer asks a DNS server, "Hey, what's the IP address for [www.example.com](https://www.example.com/)?"
* The DNS server looks up the domain name and replies with the corresponding IP address (e.g., 192.168.1.1).

## 2. Hypertext Transfer Protocol (HTTP): The Language of the Web

* Your browser now has the IP address. It uses HTTP to "talk" to the web server at that address.
* Your browser sends an HTTP request: "GET /index.html" (asking for the main page of the website).
* The web server understands HTTP, processes the request, and sends back an HTTP response containing the website's code (HTML, CSS, JavaScript).

## 3. Hypertext Transfer Protocol Secure (HTTPS): Adding Security

* HTTPS is the secure version of HTTP. It uses SSL/TLS to provide two key benefits:
  * **Encryption:** The data between your browser and the server is encrypted; if someone intercepts the traffic, it's unreadable without the correct encryption key. This protects login details, credit card info, etc.
  * **Authentication:** SSL/TLS uses certificates to help ensure the website is who it claims to be. This prevents attackers from impersonating legitimate websites.

## 4. Secure Sockets Layer/Transport Layer Security (SSL/TLS): The Security Mechanism

* Before HTTPS communication begins, your browser and the web server perform a "handshake" to establish encryption parameters.
* The web server provides a digital certificate to prove its identity, which your browser verifies
* Once this is done, a secure encrypted connection is established.

SSL/TLS, which stands for Secure Sockets Layer/Transport Layer Security, is a set of protocols that ensure secure communication over a computer network. It creates an encrypted tunnel between two parties, typically a web browser and a web server, protecting the confidentiality and integrity of the data transmitted. Here's a breakdown of how SSL/TLS works and encrypts traffic:

## The Actors Involved

* **Client:** This is typically your web browser on your computer or phone.
* **Server:** This is the computer hosting the website or service you're trying to access.
* **Certification Authority (CA):** A trusted third-party entity that verifies the identity of the server and issues SSL certificates.

## The Encryption Process

1. **Handshake:**
   * The client initiates the connection and requests a secure connection.
   * The server responds by sending its SSL certificate, which contains the server's public key and information about the CA that issued it.
   * The client's browser verifies the certificate's validity with the CA.
   * If valid, the client generates a random secret key (session key) to be used for encryption.
   * The client encrypts the session key with the server's public key from the certificate and sends it to the server. (Only the server's private key, which is not shared, can decrypt this).
   * Both sides agree on a set of encryption algorithms and parameters to be used for secure communication.
2. **Secure Communication:**
   * The session key established during the handshake is used to encrypt all data transmission between the client and server.
   * The client encrypts any data it sends to the server using the session key.
   * The server decrypts the received data using the same session key.
   * Any data sent back and forth between the client and server remains encrypted throughout the communication.

## Benefits of SSL/TLS

* **Confidentiality:** Encrypted data becomes unreadable to anyone who intercepts it, protecting sensitive information like login credentials, credit card details, or private messages.
* **Integrity:** Ensures that data hasn't been tampered with during transmission. Any modification to the data would be detected by the decryption process.
* **Authentication:** Validates the identity of the server using the SSL certificate, helping to prevent man-in-the-middle attacks where someone impersonates a legitimate server.

## How to Identify a Secure Connection

* Look for the padlock symbol in your browser's address bar when visiting a website.
* Verify that the website's address starts with "HTTPS://" instead of "HTTP://". "HTTPS" indicates the use of SSL/TLS for a secure connection.

**Overall, SSL/TLS plays a critical role in securing our online interactions, protecting sensitive data, and ensuring trust in our digital communications.**

## Putting it All Together

1. You type in [www.example.com](https://www.example.com/)
2. DNS gives your browser the server's IP address.
3. Browser establishes an HTTPS connection with the webserver (involving the SSL/TLS handshake).
4. Browser requests the website using HTTP, but communication happens over the secure, encrypted connection.
5. The web server responds with the website's content, also protected by the HTTPS connection.
