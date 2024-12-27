# Active Directory Home Lab

# Network Diagram

![image](https://github.com/user-attachments/assets/9b7e53f3-814a-49fb-a1e6-2f4b225e0298)

## High Level Overview

- Download and install Oracle VirtualBox to run our virtual machines.
- Download Windows 10 ISO and Server 2019 ISO.
- Create our first virtual machine with is going to be our Domain Controller which is going to house Active Directory.
  -  This virtual machine will have two network adapters:
     -  One for external connection to the internet.
     -  One private network that the client will connect to.
- Install server 2019 in the virtual machine and assign ip addressing to the internal network.
    - External network will get ip addressing for our home router.
- Name the server.
- Install Active Directory and create our domain.
- Configure NAT and Routing so the clients on the private network can reach the internet through the domain controller.
- Create a Dynamic Host Configuration Protocol (DHCP) so when we create our Windows 10 machine it can get automatically ip address.
- Run a PowerShell script to creak +1K users. (https://github.com/rrivm1997/AD_PS_USRS)
- Create another virtual machine and install windows 10 on it and it will be connected to the private virtual box network
- Name the machine Client1 and join it to the domain and then we are going to log into it with one of our domain accounts. 

# Windows Server 2019 
I will be creating the first virtual machine:
![image](https://github.com/user-attachments/assets/c4cd816c-9dd2-476f-824d-6884d9abc1b3)

Applying 2048 MB and 4 CPU.
![image](https://github.com/user-attachments/assets/195db44b-2600-4217-ba2e-80b691e72fc8)

Hard Disk defaults.
![image](https://github.com/user-attachments/assets/5350d727-336e-4b82-b1af-58fb1ede5c5e)

Summary.
![image](https://github.com/user-attachments/assets/d8d6267d-e103-415d-b952-0bc881fa7a4a)

Before adding the ISO, lets configure some settings.

Changing to bi-direction so that we can share clipboard and files withing host machine and virtual machine.
![image](https://github.com/user-attachments/assets/74f18517-ac8a-4edb-a5ce-5cd8cd6c2e23)

Since this is our Domain Controller we will want to add not NICs.
  - One dedicated for the internet.
  - One dedicated for the internal network.

Aapter 1 - NAT will connect to our house internet.
![image](https://github.com/user-attachments/assets/4626fb4c-5e20-449a-b60f-6a5961966a39)

Adapter 2 - Internal Network with the name 'intnet'.
  - Every Internal Network with the same name will be part of the same internal network.

![image](https://github.com/user-attachments/assets/a57e807a-1846-491c-89d8-209502e5fc13)

Lets power up the machine...

Since nothing is install, we'll get this pop up:
- ![image](https://github.com/user-attachments/assets/4bd9d27b-a5b4-4971-84ab-a4c4b45d216e)

Add the ISO and start the machine. 
- ![image](https://github.com/user-attachments/assets/7dadb075-1edf-4301-b5fd-e6d76180097d)

Click next.
- ![image](https://github.com/user-attachments/assets/af956645-57ba-4952-b54d-a78fecbd96b8)

Install Now.
- ![image](https://github.com/user-attachments/assets/b2cb5e0e-eff2-4530-9064-deaef0b73f78)

Select either of the Desktop experience. The other two will be command lines.
- ![image](https://github.com/user-attachments/assets/43217f4e-3af9-4ddb-81e2-cb08dd3861c6)

Accep terms.
- ![image](https://github.com/user-attachments/assets/fa9bb289-005f-47e7-bd2a-f0aa1842e982)

Choose Custom install.
- ![image](https://github.com/user-attachments/assets/68dd9872-ed23-42a4-8f05-f041453dbf15)
  
Clicking Next.
- ![image](https://github.com/user-attachments/assets/40348d76-6439-4a09-a09f-56b3d7162ba4)
- 









