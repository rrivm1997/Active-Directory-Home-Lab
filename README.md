# Active Directory Home Lab

# Network Diagram

![image](https://github.com/user-attachments/assets/9b7e53f3-814a-49fb-a1e6-2f4b225e0298)

## High Level Overview

- Download and install Oracle VirtualBox to run our virtual machines.
- Download Windows 10 ISO and Server 2019 ISO.
- Create our first virtual machine with is going to be our Domain Controller which is going to house Active Directroy.
  -  This virtual machine will have two network adapters:
     -  One for external connection to the internet.
     -  One private network that the client will connect to.
- Install server 2019 in the virtual machine and assign ip addressing to the internal network.
    - External network will get ip addressing for our home router.
- Name the server.
- Install Active Directory and create our domain.
- Configure NAT and Routing so the clients on the private network can reach the internet through th domain controller.
- Create a Dynamic Host Configuration Protocol (DHCP) so when we create our Windows 10 machine it can get automatically ip address.
- Run a PowerShell script to creak +1K users. (https://github.com/rrivm1997/AD_PS_USRS)
- Create another virtual machine and install windows 10 on it and it will be connected to the private virtual box network
- Name the machine Client1 and join it to the domain and then we are going to log into it with one of our domain accounts. 
