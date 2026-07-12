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
- Run **./run.sh** in terminal (Linux/macOS)
- ▼
- Open Browser
- ▼
- if it does not work
- ▼
- in terminal **python -m http.server 49242**
- ▼
- Open your browse and search **http://localhost:49242**
- ▼
- NetPractice Interface

> [!IMPORTANT]
> Keep the terminal window open while using NetPractice.
>
> Running `python3 -m http.server 49242` starts a **local web server** that serves the NetPractice files to your web browser.
>
> If you close the terminal, the local server will stop, and your browser will no longer be able to access the NetPractice website.
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

- 5|| Get my config >> to download your configuration whenever you need to; you will need it
when submitting your assignment.
<img width="949" height="429" alt="image" src="https://github.com/user-attachments/assets/46d64a85-775b-4a38-8817-e5f6047b7f00" />

# 🌐 Chapter 2 — Computer Networks

## What Is a Nomputer Network ?

- "A network is a group of two or more devices, like computers, phones, or printers, that are connected together to share information, data, and resources. These devices can be linked using wires, such as cables and fibre optics, or wirelessly through Wi-Fi and other technologies. The main purpose of a network is to allow these devices to communicate with each other easily and quickly. 
Networks can be small, like those in a home or school, or very large, like the internet, which connects millions of devices worldwide. By connecting devices, networks make it possible to share files, use shared printers, and access the internet, making our daily tasks simpler and more efficient."

### Types Of network:

- LAN ( Personal Area Network ):it is used for short range communication between personal devices , such as bluethooth or  earbuds , it's range around (1 to 10) m , that mean if dectence
  between you personal devices becom more than 10 metter you will loss the connection .

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
  - A router is a networking device that forwards data packets between different computer networks. It connects multiple packet-switched networks or subnetworks, managing traffic by directing
    packets to their intended IP addresses. Routers allow multiple devices to share an Internet connection efficiently.
  
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
 
# chapter 3 : Introduction to IP Addressing

So far, we've learned about the devices that make up a computer network, such as hosts, switches, and routers.
But here's an important question:

**How does one device know where to send data?**
Imagine trying to send a letter without knowing the recipient's address. It would never reach the correct destination.
Computer networks work in a similar way. Before two devices can communicate, each device must have its own unique address that identifies it on the network.
This address is called an **IP Address**.

## 📍 What Is an IP Address?

**IP** stands for **Internet Protocol**.

An **IP Address** is a unique **logical address** assigned to a device (or more precisely, a network interface) that communicates using the Internet Protocol (IP).

Its primary purpose is to identify devices on a network and enable them to send and receive data correctly.

### Why Is It Called a Logical Address?

An IP address is called a **logical address** because it is not permanently tied to the device.

It can be changed whenever the device joins a different network or when the network administrator assigns a new address.

This flexibility allows devices to communicate correctly on different networks.
## IPv4 (Internet Protocol Version 4)

There are two versions of the Internet Protocol currently in use:

- **IPv4 (Internet Protocol version 4)**
- **IPv6 (Internet Protocol version 6)**

 we'll focus on **IPv4**, since it is the version used throughout the **42 NetPractice** project.
 
 ### **IPv4 Address**: An IPv4 address is a **32-bit logical address** assigned to a device on a network. It uniquely identifies the device and enables it to send and receive data using the Internet Protocol (IP).
 ```text
IPv4 Address

32 bits = 4 byte
4 Octets 
each octet range 0-255
[0-255].[0-255].[0-255].[0-255]
```
**IPv4 addresses can be represented in two notations:**

- binary notation
- dotted decimal notation
**binary notation**
  ```text
  01100110.11011101.11011010.11000000
  octet.octet.octet.octet
  ```
  **decimal notation**
  ```text
  192.168.20.50
  octet.octet.octet.octet
  ```
### Rules for a Valid IPv4 Address

For an IPv4 address to be valid, it must follow these rules:

- It consists of **4 octets** separated by dots (`.`).
- Each octet contains a decimal number between **0** and **255**.
- Only numbers are allowed.
- No octet can be greater than **255** or less than **0**.

#### ✅ Valid Examples

- `192.168.1.10`
- `10.0.0.1`
- `172.16.25.100`

#### ❌ Invalid Examples

- `256.168.1.10` → An octet is greater than **255**.
- `192.168.1` → Missing one octet.
- `192.168.1.10.5` → Too many octets.
- `192.168.one.10` → Contains letters instead of numbers.
- `192.-1.1.10` → Negative values are not allowed. 

> Historically, IPv4 addresses were divided into **Classes (A, B, and C)** to allocate addresses according to network size. Today, this system has largely been replaced by **CIDR**, which provides more flexible and efficient address allocation.

> [!NOTE]
> An IPv4 address is **32 bits** long, which provides approximately **4.3 billion unique addresses** (2³²). As the number of Internet-connected devices grew rapidly, this address space became insufficient. To help overcome this limitation, private IP addresses and technologies such as **Network Address Translation (NAT)** were introduced, allowing many devices to share a single public IP address.
> **NAT** (Network Address Translation) allows multiple devices in a private network to share a single public IP address when accessing the internet

## Public vs Private IP Addresses 

### Private IP Address
Private IP Addresses are those addresses that work within the local network.
- Used within a local or private network
- Not routable on the public internet
- Scope is limited to the local network
- Requires NAT for internet access

> [!IMPORTANT]
> **Private IPv4 Address Ranges**
>
> - **10.0.0.0/8** → `10.0.0.0` – `10.255.255.255`
> - **172.16.0.0/12** → `172.16.0.0` – `172.31.255.255`
> - **192.168.0.0/16** → `192.168.0.0` – `192.168.255.255`
>
> These address ranges are reserved for **private networks** and **cannot be routed directly over the public Internet**.


### Public IP Address
- Used for communication over the internet
- Routable on the public internet
- Scope is global
- Does not require NAT

> [!NOTE]
> Private IP addresses help conserve the limited IPv4 address space. Unlike public IP addresses, they **do not need to be globally unique**, which means the same private IP address can be reused in millions of different local networks around the world.

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/e5e30774-6901-4c49-809e-aff29f238e81" />

# Chapter 5 — Subnet Mask

## Introduction

We learned that every device needs an **IP address** to communicate.

But here's an important question:

**How does a device know whether the destination is on the same network or on a different network?**

Looking at the IP address alone is **not enough**.

For example:

- Device A → `192.168.1.10`
- Device B → `192.168.1.50`

Are they in the same network?

Now consider:

- Device A → `192.168.1.10`
- Device B → `192.168.2.50`

Are they in the same network?

To answer these questions, we need another piece of information called the **Subnet Mask**.

## What Is a Subnet?

A **subnet** is a smaller logical network created by dividing a larger network into multiple smaller networks.
> A subnet is a group of devices that can communicate directly without passing through a router.
### Example

Imagine you have a network that contains **256 IP addresses**, but you only need to connect **10 devices**.

Without subnetting, the remaining **246 IP addresses** would be unused, resulting in inefficient use of the available address space.

Subnetting solves this problem by dividing the large network into smaller networks, allowing each subnet to contain only the number of addresses it actually needs.

## Why Do We Need a Subnet Mask?

Subnet masks are used for several important reasons:

- **Divide a large network into smaller subnets**, making the network easier to manage.
- **Use IP addresses more efficiently** by creating networks that contain only the required number of hosts.
- **Reduce broadcast traffic**, which improves network performance.
- **Help devices determine whether the destination is on the same network or a different network.**
- **Decide whether data should be sent directly to the destination or forwarded to a router (default gateway).**

## How Does a Subnet Mask Work?

A subnet mask works by dividing an IPv4 address into two logical parts:

- **Network Portion** – Identifies the network.
- **Host Portion** – Identifies the individual device.

The subnet mask determines where the **network portion** ends and the **host portion** begins.

> [!NOTE]
> An IPv4 address consists of **4 octets (32 bits)**.
>
> Depending on the subnet mask, different numbers of bits are used for the network and host portions.
>
> The following examples are simplified representations:
>
> ```
> N.N.N.H
> N.N.H.H
> N.H.H.H
> ```
>
> **N** = Network Portion  
> **H** = Host Portion
>
> In reality, the boundary is determined by **bits**, not necessarily by whole octets.

If two devices have the same **network portion**, they belong to the same network and can communicate directly.

If their **network portions** are different, the packet must be sent to the **default gateway (router)** so it can reach the destination network.

## CIDR Notation

Writing the full subnet mask every time can be inconvenient. To make it shorter and easier to read, a notation called **CIDR (Classless Inter-Domain Routing)** is used.

Instead of writing:

```
255.255.255.0
```

we simply write:

```
/24
```
> [!NOTE]
> The number after the slash (`/`) in CIDR notation indicates how many **bits** belong to the **network portion**.
>
> For example:
>
> ```
> /24
> ```
>
> means that the first **24 bits** of the **subnet mask** are `1`, and the remaining **8 bits** are `0`.
>
> ```
> /24
> ↓
> 11111111.11111111.11111111.00000000
> ↓
> 255.255.255.0
> ```
>
> The **1s** identify the **network portion**, while the **0s** identify the **host portion**.
### Example: `/27`

```
CIDR:
/27
```

The subnet mask is:

```
11111111.11111111.11111111.11100000
```

which is equal to:

```
255.255.255.224
```

The first **27 bits** belong to the **network portion**, while the remaining **5 bits** belong to the **host portion**.

```
11111111.11111111.11111111.11100000
 NNNNNNNN.NNNNNNNN.NNNNNNNN.NNNHHHHH
```

- **27 Network bits**
- **5 Host bits**

### Applying the Mask to an IP Address

```
IP_1 Address : 192.168.1.130/27
IP_1 Address : 192.168.1.135/27
Binary:
IP_1
11000000.10101000.00000001.10000010
11111111.11111111.11111111.11100000
-----------------------------------
NNNNNNNN.NNNNNNNN.NNNNNNNN.NNNHHHHH
IP_2
11000000.10101000.00000001.10000101
11111111.11111111.11111111.11100000
-----------------------------------
NNNNNNNN.NNNNNNNN.NNNNNNNN.NNNHHHHH
```
> [!NOTE]
> Notice that after converting both IP addresses to binary, the **first 27 bits** (the network portion) are identical.
>
> Since both devices have the same **network portion**, they belong to the **same subnet** and can communicate directly without using a router.

> 
> **IP Address 1:** `192.168.122.15`
>
> **IP Address 2:** `192.168.122.60`
>
> Assuming the subnet mask is **255.255.255.0 (/24)**, the first **24 bits** (the first three octets) represent the **network portion**, while the last **8 bits** represent the **host portion**.
>
> ```
> 192.168.122.15
> N.N.N.H
>
> 192.168.122.60
> N.N.N.H
> ```
>
> Since both IP addresses have the same **network portion**, they belong to the **same subnet**.
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/56638d16-61ad-4af9-9569-1c5c0ce3b53c" />

### Number of Hosts

The number of usable host addresses depends on the number of **host bits**.

The formula is:

```
Usable Hosts = 2^(Host Bits) − 2
```

We subtract **2** because:

- The **first address** is reserved as the **Network Address**.
- The **last address** is reserved as the **Broadcast Address**.

Therefore, neither of these addresses can be assigned to a host.

### Example: /27

```
CIDR: /27

Host Bits = 32 - 27 = 5

Usable Hosts = 2^5 - 2 = 30
```

Subnet:

```
192.168.1.128/27
```
**Address**
192.168.1.128  Network Address
192.168.1.129 First Usable Host
 
192.168.1.158 Last Usable Host 
192.168.1.159 Broadcast Address 

> [!TIP]
> You can use an online **Subnet Calculator** to verify your calculations while learning.

# Common Log Messages
- **packet accepted** : The device has successfully received the packet and started processing it.
- **invalid IP address** :The interface is configured with an invalid IP address. Check that the IP address is correctly formatted and belongs to the appropriate network.
- **destination does not match any interface** : The destination IP **does not** belong to any network (directly connected) >> (in same network) to the current device.
- **pass through routing table** : The device searches its routing table to find the best route to the destination. This is a normal step, not an error. this prosses done when two devices want to make comunication but thay are not belong in same network .
- **invalid destination IP for this way** : The configured destination IP is not valid for this communication path. Verify the destination IP address and network configuration.
- **loop detected** :The packet returned to a device that had already processed it, causing a forwarding loop or packet repetition.

 > [!NOTE]
> Routers route packets to **networks**, not individual hosts.
>
> For example, if a router connects the network:
>
> ```
> 93.74.210.128/25
> ```
>
> a single route to this network allows access to **every host** inside it:
>
> ```
> 93.74.210.129
> ...
> 93.74.210.254
> ```
>
> If a router connects multiple LANs, each LAN requires **one route** in the routing table—not one route for every device.

# AI USING
# RESOURCES 
- [https://study-ccna.com/what-is-a-network/](https://www.msoftserv.com)
 

  




