# A Simple Web Setup


## Description
This is a basic web infrastructure that hosts a website accessible through `www.foobar.com`. There are no firewalls or SSL certificates to protect the server's network. The server has to share its resources (CPU, RAM, SSD) between the database, application server, and other components.

## Details About This Infrastructure

+ **What is a server?** A server is a computer hardware or software that provides services to other computers, called *clients*.

+ **What's the role of the domain name?** The domain name provides a user-friendly alias for an IP address. For example, `www.wikipedia.org` is easier to remember than `91.198.174.192`. The IP address and domain name are mapped in the Domain Name System (DNS).

+ **What DNS record is used for `www.foobar.com`?** `www.foobar.com` uses an **A record**, which stores a hostname and its corresponding IPv4 address.

+ **What does the web server do?** The web server is software/hardware that accepts HTTP/HTTPS requests and responds with the requested content or an error message.

+ **What's the role of the application server?** The application server hosts and delivers applications and associated services for end-users, IT services, and organizations.

+ **What's the role of the database?** The database maintains a collection of organized information that can be easily accessed, managed, and updated.

+ **How do the client and server communicate?** Communication between the client (user's computer) and the server happens over the internet using the TCP/IP protocol suite.

## Issues With This Infrastructure

+ **Single Points of Failure (SPOF):** There are multiple SPOFs, like the MySQL database server. If it goes down, the entire site is unavailable.

+ **Downtime during maintenance:** When any component needs maintenance, the whole server has to be taken offline, resulting in website downtime.

+ **Lack of scalability:** It's difficult to scale this infrastructure because all the components are on a single server. The server can quickly run out of resources or slow down when handling a lot of traffic.

+ **Security vulnerabilities:** Without firewalls or SSL/TLS encryption, the server's network is exposed to security risks.

To improve this setup, we could consider adding redundancy, load balancing, and security measures like firewalls and SSL/TLS encryption.