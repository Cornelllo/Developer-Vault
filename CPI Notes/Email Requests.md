Hi @CPI Platforms

  

Requesting a remote server resource(virtual machine) for

Open edX to self managed and host it with the following

  

Requirements

- **Supported OS:** any 64-bit, UNIX-based OS.
    
- **Architecture:** Both AMD64 and ARM64 are supported.
    
- **Required software:**
    

- -Docker: v24.0.5+
    
-         -Docker Compose: v2.0.0+
    
-  With root access if unable to install the required dependencies above.
    
- Ports 80 and 443 should be open.
    
- **Hardware:**
    
    -Minimum configuration: 4 GB RAM, 2 CPU, 8 GB disk space
    
    -Recommended configuration: 8 GB RAM, 4 CPU, 25 GB disk space


Hi @CPI Platforms

  

Kindly requesting for a DNS configuration to add a subdomain in **`cpi.com.ph`**

For **`learn.cpi.com.ph`** this is for the self hosted LMS using Open edX

  

Create the following record:

- a record of type A
    
    learn 1800 IN A 52.74.85.83    
    
- A CNAME record
    
    *.learn 1800 IN CNAME learn.cpi.com.ph.
    

The IP address (52.74.85.83) provided above is from the remote server Linux Ubuntu that I requested with ID: 0000296


Hi @CPI Platforms  
  
Kindly requesting for a configuration to create an email sender with **@cpi.com.ph** as the domain this is for the learning management system 

which will send and email to that email sender and finally forward it to the users.

  

For example, "**learn@cpi.com.ph**"  
Enable both configurations for **SPF**(Sender Policy Framework) and **DKIM**(DomainKeys Identified Mail)

  

**Server ip4:** 52.74.85.83