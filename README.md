*This activity has been created as part of the 42 curriculum by ssleit*
- - - 
# 🌐 NetPractice
Welcome to the **NetPractice** guide!
- - - 
# Introduction
This repository is designed to help beginners understand the fundamentals of computer networking through the **42 School NetPractice** project.
Whether you've never studied networking before or simply want a structured reference, this guide will walk you through every concept step by step.؟
## What is NetPractice?
NetPractice is a networking project developed by **42 School** that teaches the fundamental concepts of computer networks through interactive exercises.

Instead of writing code, you'll configure IP addresses, subnet masks, gateways, and routing tables to allow devices to communicate correctly.

Each level presents a networking scenario where your goal is to identify configuration issues, and establish successful communication between devices.

By completing NetPractice, you'll build a strong foundation in networking that will help you understand real-world computer networks.
## Why Learn Networking?

Networking is one of the core foundations of computer science.
Every website you visit, every message you send, and every online game you play you use depends on computer networks.
Understanding networking will help you:

-  Understand how the Internet works.
-  Learn how devices communicate.
-  Configure networks correctly.
-  Understand routing and packet forwarding.
-  Troubleshoot network problems.

## Learning Objectives

By the end of this guide, you will be able to:

- Understand the basics of computer networking.
- Explain how devices communicate.
- Identify the role of routers and switches.
- Understand IPv4 addressing.
- Calculate subnet masks and CIDR notation.
- Read and configure routing tables.
- Analyze packet flow through a network.
- Solve every NetPractice level with confidence.
- - - 
> [!TIP]
> New to networking? Don't worry! Every concept will be explained step by step.
- - -
# chapter_one : Gitting started 
Why i am learning this ?
Before learning networking concepts, let's become familiar with the NetPractice environment. In this chapter, you'll learn how to access the project, navigate the interface.

## 🌐 What is the NetPractice Website?
NetPractice is an interactive web-based learning platform developed by **42 School** to help students understand the fundamentals of computer networking through practical exercises.
The website contains **10 networking levels**, each presenting a different network topology with one or more configuration problems.
Your task is to analyze each network, identify the issue, and correctly configure elements such as IP addresses, subnet masks, gateways, and routing tables until all devices can communicate successfully.
NetPractice allows you to learn by solving real networking scenarios in an interactive environment.

 ### Access NetPractice
- first  Download NetPractice folder.
-  ▼ 
-  Extract the archive.
-  ▼
- Run run.sh (Linux/macOS)
- ▼
- Open Browser
- if it does not work
- ▼
- in terminal python -m http.server 49242
- ▼
- Open http://localhost:49242
- ▼
- NetPractice Interface

> [!IMPORTANT]
> Keep the terminal running while using NetPractice. Closing it will stop the local web server.
>  
-
   <img width="284" height="403" alt="image" src="https://github.com/user-attachments/assets/02fe6cf0-8c47-421e-92e5-bb140ffe5593" />
- enter your 42 login
- ▼
- <img width="941" height="432" alt="image" src="https://github.com/user-attachments/assets/3bd45680-170f-4594-96ee-12dbf2b98e36" />

## net practice interface :
- 1|| network >> The main area where you'll solve each NetPractice level.
  This is where all network devices, connections, and configurations are displayed.
- 3|| Goals >> Lists the objectives that must be completed to solve the current level ,A level is considered solved **only when all goals are marked** as **OK** 
- 2|| Logs Panel >> Displays the simulation output after pressing **Check Again** ,it shows whether communication succeeds or fails and provides hints about the problem.
- 4|| Check Again >> Runs the simulation and checks whether your current configuration is correct.
- 5|| Get my config >> Restores your personal configuration if you've modified or not .
<img width="949" height="429" alt="image" src="https://github.com/user-attachments/assets/46d64a85-775b-4a38-8817-e5f6047b7f00" />

# 🌐 Chapter 2 — Computer Networks

## What Is a Nomputer Network ?
- "A network is a group of two or more devices, like computers, phones, or printers, that are connected together to share information, data, and resources. These devices can be linked using wires, such as cables and fibre optics, or wirelessly through Wi-Fi and other technologies. The main purpose of a network is to allow these devices to communicate with each other easily and quickly. 
Networks can be small, like those in a home or school, or very large, like the internet, which connects millions of devices worldwide. By connecting devices, networks make it possible to share files, use shared printers, and access the internet, making our daily tasks simpler and more efficient."

### Types Of network:
- LAN ( Personal Area Network ):it is used for short range communication between personal devices , such as bluethooth or  earbuds , it's range around (1 to 10) m , that mean if dectence between you personal devices becom more than 10 metter you will loss the connection .
- PAN( Local Area Network ): network that connect devices on local area such as home , office or mapy small campus. 
- MAN( Metropolitan Area Network ):connect "" muliple network "" togather it is  can cover city .  
- WAN( Wide Area Network ) :A WAN connects networks over large geographical areas such as countries.

- How Does Communication Happen Between Two Devices? To answer this question, we first need to understand the basic elements of a computer network.
# 🖥️ Network devices 
Imagine you want to send a message to your friend.
A few seconds later, your friend receives it.
But how did your message travel from your device to your friend's device?

To answer this question, we first need to understand the basic network devices that make communication possible.
> [!NOTE]
> In NetPractice, you will mainly work with hosts, switches, routers, and the default gateway. You will also learn how these devices communicate through the Internet, which is a global network connecting millions of smaller networks.
## Nodes
nodes : A node is any device connected to a network that can send, receive, or forward data.
it is can classify into two branch :
   ### end devices (Hosts) :
   End devices (also called **hosts**) are the devices where network communication starts or ends. They send data, receive data, or both.
   as printer , pc , smartphone ...
   ### Intermediate Devices (Network Devices)
   Intermediate devices connect end devices and forward data from one device to another.
   In NetPractice, we mainly focus on the following network components:
   #### Switches
   - What Is Switch ?A switch is a networking device used to connect numerous networkable devices together, this can include: PC's, servers, printers, routers and other switches, allows            multiple devices to be connected within a local area network (LAN).
   #### Routers
   - A router is a networking device that forwards data packets between different computer networks. It connects multiple packet-switched networks or subnetworks, managing traffic by directing    packets to their intended IP addresses. Routers allow multiple devices to share an Internet connection efficiently.
  - How Does a Router Work?
   Routers determine the path for a packet by examining its destination IP address and consulting the routing table, which contains information on network paths. They use a set of rules to        identify the most efficient route for each packet.
   Static routing: Configured manually, suitable for small or stable networks.
  Dynamic routing: Automatically updated based on network activity, ideal for large or changing networks.
 - Routing: Determines the optimal path for packets using routing tables and algorithms
  #### Default Gateway
  - When Default Gateway is Used:
  when the source wants to reach a destination which is outside its network then, the source uses the default gateway to forward the data and locate the destination's network so that data        should reach its intended destination. The default gateways are  used when the host doesn't know about the destination's network i.e. the network in which the destination is present or when    the route information is not available for any destination then it goes to the default gateway so that it can identify in     which network the destination is and can forward the data          through that route. The default gateway is an important device for the data forwarding and routing of the data on the other network. It helps in the communication of one network computer       with  the other network computer. 
## Transmission Media
Transmission Media can be wired or wireless :
   ### wired media :
   using ( fiber , coaxil , USB or others )
   ### wireless media :
   using (satellite , microwaves , radio or others)
 
# 📍Introduction to IP Addressing

So far, we've learned about the devices that make up a computer network, such as hosts, switches, and routers.
But here's an important question:
> **How does one device know where to send data?**
Imagine trying to send a letter without knowing the recipient's address. It would never reach the correct destination.
Computer networks work in a similar way. Before two devices can communicate, each device must have its own unique address that identifies it on the network.
This address is called an **IP Address**.

# RESOURCES 
- [https://study-ccna.com/what-is-a-network/](https://www.msoftserv.com)
- 

  




