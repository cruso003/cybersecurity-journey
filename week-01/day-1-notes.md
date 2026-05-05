# Day 1 - November 17, 2025

## Accomplishments

- [x] Created DigitalOcean droplet (Ubuntu 24.04, AMS3)
- [x] Set up GitHub repository
- [x] Started TryHackMe Pre-Security path (7%)
- [x] Created learning plan with Claude

## TryHackMe Progress

- Currently on: Intro to LAN
- Completion: 7%
- Target: 100% by Day 3

## Infrastructure Setup

- **Droplet:** ubuntu-s-1vcpu-1gb-ams3-01
- **Specs:** 1GB RAM, 25GB Disk, Ubuntu 24.04 LTS
- **Status:** Initial updates running

## Today's Learnings

### TryHackMe - Intro to LAN

## Today's Deep Dive: Network Segmentation

### Key Question: Why separate cash registers from public WiFi?

**Answer: Security through Network Isolation**

1. **Prevent unauthorized access**

   - Public WiFi users can't scan/attack employee systems
   - Firewall blocks cross-subnet traffic

2. **Contain breaches**

   - If customer device compromised, malware can't spread to critical systems
   - Limits blast radius of attacks

3. **Compliance requirements**

   - PCI-DSS requires payment systems isolated from public networks
   - Legal/regulatory requirements

4. **Real-world example:**
   - Liberian government office: Guest WiFi vs. sensitive executive network
   - Same principle applies

### Concepts Mastered Today:

- **DHCP**: Automatic IP assignment (Discover → Offer → Request → ACK)
- **ARP**: Maps IP addresses to MAC addresses (Request/Reply)
- **Subnetting**: Dividing networks for efficiency, security, control
- **Network Topologies**: Star, Bus, Ring designs
- **Switches vs Routers**: Local forwarding vs. network routing

### Security Implications:

- Flat networks (no segmentation) = easy lateral movement for attackers
- Proper subnetting = defense in depth
- Firewall rules between subnets = critical security control

### Application to Liberia Cybersecurity:

Many .lr government sites likely on flat networks. External assessment would:

1. Compromise public web server
2. Scan internal network (if no segmentation)
3. Pivot to sensitive systems
4. Full compromise

**Solution:** Network segmentation, DMZ architecture, firewall rules

### HTTP Status Codes:

100-199 - Information Response These are sent to tell the client the first part of their request has been accepted and they should continue sending the rest of their request. These codes are no longer very common.
200-299 - Success This range of status codes is used to tell the client their request was successful.
300-399 - Redirection These are used to redirect the client's request to another resource. This can be either to a different webpage or a different website altogether.
400-499 - Client Errors Used to inform the client that there was an error with their request.
500-599 - Server Errors This is reserved for errors happening on the server-side and usually indicate quite a major problem with the server handling the request.
Common HTTP Status Codes:

There are a lot of different HTTP status codes and that's not including the fact that applications can even define their own, we'll go over the most common HTTP responses we are likely to come across:

200 - OK The request was completed successfully.
201 - Created A resource has been created (for example a new user or new blog post).
301 - Moved Permanently This redirects the client's browser to a new webpage or tells search engines that the page has moved somewhere else and to look there instead.
302 - Found Similar to the above permanent redirect, but as the name suggests, this is only a temporary change and it may change again in the near future.
400 - Bad Request This tells the browser that something was either wrong or missing in their request. This could sometimes be used if the web server resource that is being requested expected a certain parameter that the client didn't send.
401 - Not Authorised You are not currently allowed to view this resource until you have authorised with the web application, most commonly with a username and password.
403 - Forbidden You do not have permission to view this resource whether you are logged in or not.
405 - Method Not Allowed The resource does not allow this method request, for example, you send a GET request to the resource /create-account when it was expecting a POST request instead.
404 - Page Not Found The page/resource you requested does not exist.
500 - Internal Service Error The server has encountered some kind of error with your request that it doesn't know how to handle properly.
503 - Service Unavailable
This server cannot handle your request as it's either overloaded or down for maintenance.

### Infrastructure Setup

- Successfully created non-root user "cyberlab"
- Configured SSH access
- Running comprehensive security tool installation
- Droplet IP: 104.248.195.177 (AMS3 datacenter)

## Time Spent

- Setup: 45 minutes
- THM Learning: [update with hours]
- Total: [calculate]

## Tomorrow's Goals

- [ ] Complete 50%+ of Pre-Security
- [ ] Install Kali tools on droplet
- [ ] Complete first HTB Starting Point machine

## Questions/Challenges

- None yet - just getting started!
