# 0x09-web Infrastructure Design README

## Files
- `0-simple_web_stack`
- `1-distributed_web_infrastructure`
- `2-secured_and_monitored_web_infrastructure`
- `3-scale_up`

## Explanations

### What is a server?
A server is a computer or computer program that manages access to a centralized resource or service in a network¹.

### What is the role of the domain name?
The domain name serves as a human-readable address for Internet resources, allowing users to locate websites easily without remembering numerical IP addresses⁹.

### What type of DNS record is 'www' in www.foobar.com?
The 'www' in www.foobar.com is typically a CNAME (Canonical Name) record, which is used to alias one name to another²⁸.

### What is the role of the web server?
A web server processes HTTP requests from clients and serves them HTTP responses, usually in the form of HTML documents, images, CSS, and JavaScript files¹¹.

### What is the role of the application server?
The application server hosts applications, providing an environment for the application's logic to run and offering services like transaction management and security[^20^].

### What is the role of the database?
The database stores and retrieves data as requested by other software applications, ensuring organized, secure, and efficient data management².

### Server Communication
Servers communicate with the user's computer using HTTP/HTTPS, protocols for transferring web pages and content on the internet¹⁶.

### Single Point of Failure (SPOF)
SPOF refers to a component within a system that, if it fails, can cause the entire system to stop functioning²⁴.

### Downtime for Maintenance
Downtime can occur during maintenance, such as deploying new code or restarting servers. Techniques like rolling updates can minimize this downtime³⁴.

### Scaling Issues
A system may struggle to scale with too much incoming traffic. Solutions include load balancers and horizontal scaling to manage the load³³.
