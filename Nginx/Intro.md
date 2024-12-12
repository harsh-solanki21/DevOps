## Nginx Intro

- Nginx is a web server.
- Technically, a web server is any computer that has a running service accepting HTTP requests on some port(by default, 80), and replying with HTTP response.
- Nginx is defined as an HTTP and reverse proxy server, a mail proxy server, and a generic TCP/UDP proxy server.

### Why should we use Nginx?

**1. Speed**
Faster loading page

**2. Acceleration**
Routes traffic to web servers in a way that enhances the overall speed when we have two or more web servers running the same application.

**3. Load balancing**
A load balancer is a device/service that distributes traffic load on two or more web servers.
Nginx provides fault tolerance and increase in speed.

**4. Scalable concurrent connections handling**

**5. The ability to operate on relatively cheap hardware**

**6. On-the-fly upgrades**
Nginx can patched or upgraded without having to take downtime and disrupt the business.

**7. Ease of installation and maintenance**

<br />

- A reverse proxy is a service that stands between the client and the web servers. It receives the request from the client and sends it on its behalf to the web server behind it. When the response is received from the web servers, it relays it back to the requesting client.
  Reverse proxies are used for performance and security reasons.

- Every feature can be activated/deactivated using modules. This makes it easier for the administrator to work with the required functionality only.

- Nginx uses asynchronous way of serving requests.

- It allows you to serve many protocols not just HTTP and HTTPS. You can use it to serve IMAP, POP3 and SMTP for mail protocols. Also the latest full-duplex WebSocket protocol is supported.

- Nginx excels when it comes to serving large files or streaming media as other web servers(Apache) create a thread for each new request.
