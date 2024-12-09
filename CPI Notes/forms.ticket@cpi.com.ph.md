Send an email to request access to the remote server

Server - we can just SSH to it and set up Tutor for Open edX
- **Supported OS:** any 64-bit, UNIX-based OS.
    
- **Architecture:** Both AMD64 and ARM64 are supported.
    
- **Required software:**
    

- -[Docker](https://docs.docker.com/engine/installation/): v24.0.5+ 
    
- -[Docker Compose](https://docs.docker.com/compose/install/): v2.0.0+
    
-  With root access if unable to install the required dependencies above.
    
- Ports 80 and 443 should be open.
    
- **Hardware:**
    
- -Minimum configuration: 4 GB RAM, 2 CPU, 8 GB disk space
    
- -Recommended configuration: 8 GB RAM, 4 CPU, 25 GB disk space
    
-
DNS records - create an A type DNS record to point to our server's public IP (DNS propagation will take some time)

Get a domain or use the CPI domain