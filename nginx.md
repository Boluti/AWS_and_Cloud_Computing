## What are ports? (research) ## 
Ports are virtual communication endpoints used in computer networking to enable the exchange of data between different devices or processes over a network. 
They are essential for identifying specific services or applications running on a computer or server.

## What is a reverse proxy? How is it different to a proxy? (research) ##
A proxy server is an intermediary server that acts as a gateway between client devices (such as computers or smartphones) and other servers (typically web servers).
It receives requests from clients and forwards them to the target server, acting as an intermediary.

A reverse proxy, on the other hand, is a server that sits between client devices and one or more backend servers. 
The primary purpose of a reverse proxy is to distribute incoming client requests across multiple backend servers, often for load balancing and enhanced security. 


## What is Nginx's default configuration (hint - 'sites-available' directory) ##
Nginx, a popular web server and reverse proxy server, typically has a default configuration that includes a main configuration file located in the /etc/nginx/nginx.conf file, and it may also use a directory called sites-available (common on Debian-based systems) or conf.d (common on Red Hat-based systems) to manage site-specific configurations.
To view Nginx's default configuration, you can check the contents of /etc/nginx/nginx.conf and the files inside the sites-available or conf.d directory, depending on your system's configuration.

## How do you set up a Nginx reverse proxy? ##
Setting up an Nginx reverse proxy involves several steps:

-  Install Nginx: Ensure that Nginx is installed on your server. You can typically install it using your system's package manager (e.g., apt, yum, dnf, or brew).

- Create a Configuration File: Create a new configuration file for your reverse proxy in the sites-available or conf.d directory. You can copy an existing template or create one from scratch. Configure the proxy_pass directive to point to your backend server(s).

- Symlink to Sites-Enabled: Create a symbolic link from your configuration file in sites-available to the sites-enabled directory. 
This enables the site configuration.
- Test Configuration: Use the nginx -t command to test your Nginx configuration for syntax errors.

- Reload Nginx: If the configuration test is successful, reload Nginx to apply the changes: sudo systemctl reload nginx (systemd-based systems) or sudo service nginx reload (init.d-based systems).

- Adjust Firewall Rules: Ensure that your firewall allows traffic on the necessary ports (usually 80 and 443) for your reverse proxy setup.

- DNS Configuration: Update DNS records to point to the IP address of your Nginx reverse proxy if necessary.
Now, Nginx should be set up as a reverse proxy, forwarding requests to your backend server(s) as defined in your configuration file.