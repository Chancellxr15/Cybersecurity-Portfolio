# OSPF Routing Configuration Lab

> **Step 1: Configure the routers**

# On the routers, enter global configuration mode and configure the hostname, console, virtual terminal, and passwords as instructed. 

### Step 2: Disable DNS lookup

> Router(config)#**no ip domain-lookup**

### Step 3: Configure the interfaces on Router

> Configure the interfaces on the routers with the IP addresses from the hands-on final information.

### Step 4: Verify IP addressing and interfaces

> Verify that the IP addressing is correct and that the interfaces are active.
>
> **Step 5: Configure Ethernet interfaces to the switches**

# Configure the Ethernet interfaces to the switches with the IP addresses and default gateways specified on the hands-on final information.

# **Step 6: Use the router ospf command in global configuration mode to enable OSPF on the R1 router.** Enter a process ID of 1 for the *process-ID* parameter.

> Router(config)#**router ospf 1**
>
> Router(config-router)#

### Step 7: Configure the network statement for the LAN network.

> Once you are in the Router OSPF configuration sub-mode, configure the LAN network as specified in the documentation to be included in the OSPF updates that are sent out of the router.
>
> The OSPF **network** command uses a combination of *network-address* and *wildcard-mask* similar to that which can be used by EIGRP. Unlike EIGRP, the wildcard mask in OSPF is required.
>
> Use an area ID of 0 for the OSPF *area-id* parameter. 0 will be used for the OSPF area ID in all of the **network** statement for this lab.
>
> Router(config-router)#**network x.x.x.x 0.0.0.255 area 0**
>
> Router(config-router)#

### Step 8: Configure the router to advertise the WAN network attached to the GigabitEthernet /0/1 interface.

> Router(config-router)# **network x.x.x.x. 0.0.0.255 area 0**
>
> Router(config-router)#

### Step 9: When you are finished with the OSPF configuration for the router, return to privileged EXEC mode.

> Router(config-router)#**end**
>
> %SYS-5-CONFIG_I: Configured from console by console Router#

## Task: Configure OSPF Router IDs

> The OSPF router ID is used to uniquely identify the router in the OSPF routing domain. A router ID is an IP address. Cisco routers derive the Router ID in one of three ways and with the following precedence:

1.  IP address configured with the OSPF **router-id** command.

2.  Highest IP address of any of the router's loopback addresses.

3.  Highest active IP address on any of the router's physical interfaces.

> Since no router IDs or loopback interfaces have been configured on the three routers, the router ID for each router is determined by the highest IP address of any active interface.
>
> The router ID can also be seen in the output of the **show ip protocols**, **show ip ospf**, and
>
> **show ip ospf interfaces** commands.

### Router#show ip protocols

> Routing Protocol is \"ospf 1\"
>
> Outgoing update filter list for all interfaces is not set Incoming update filter list for all interfaces is not set Router ID 10.100.x.x
>
> Number of areas in this router is 1. 1 normal 0 stub 0 nssa Maximum path: 4
>
> *\<output omitted\>*

### Router#show ip ospf

> Routing Process \"ospf 1\" with ID 10.100.x.x Supports only single TOS(TOS0) routes
>
> Supports opaque LSA
>
> SPF schedule delay 5 secs, Hold time between two SPFs 10 secs
>
> *\<output omitted\>*

### Router#show ip ospf interface

> FastEthernet0/0 is up, line protocol is up Internet address is 172.16.1.33/29, Area 0
>
> Process ID 1, Router ID 10.100.x.x, Network Type BROADCAST, Cost:
>
> 1
>
> Transmit Delay is 1 sec, State DR, Priority 1
>
> Designated Router (ID) 192.168.10.10, Interface address 172.16.1.33 No backup designated router on this network
>
> Timer intervals configured, Hello 10, Dead 40, Wait 40, Retransmit 5 Hello due in 00:00:00
>
> Index 1/1, flood queue length 0 Next 0x0(0)/0x0(0)
>
> Last flood scan length is 1, maximum is 1
>
> Last flood scan time is 0 msec, maximum is 0 msec Neighbor Count is 0, Adjacent neighbor count is 0 Suppress hello for 0 neighbor(s)
>
> *\<output omitted\>*

### Step 1: Use loopback addresses to change the router IDs of the routers in the topology.

+--------------------------------------------------+-----------------------+
| > Router1(config)#**interface loopback 0**       | > **255.255.255.255** |
| >                                                |                       |
| > Router1(config-if)#**ip address 10.10.1.1**    |                       |
+==================================================+=======================+
+--------------------------------------------------+-----------------------+

+--------------------------------------------------+-----------------------+
| > Router2(config)#**interface loopback 0**       | > **255.255.255.255** |
| >                                                |                       |
| > Router2(config-if)#**ip address 10.10.2.2**    |                       |
+==================================================+=======================+
+--------------------------------------------------+-----------------------+

+--------------------------------------------------+-----------------------+
| > Router3(config)#**interface loopback 0**       | > **255.255.255.255** |
| >                                                |                       |
| > Router3(config-if)#**ip address 10.10.3.3**    |                       |
+==================================================+=======================+
+--------------------------------------------------+-----------------------+

> **Step 2: Reload the routers to force the new Router IDs to be used.**
>
> When a new Router ID is configured, it will not be used until the OSPF process is restarted. Make sure that the current configuration is saved to NRAM, and then use the **reload** command to restart each of the routers..
>
> **Step 3: Use the show ip ospf neighbors command to verify that the router IDs have changed.**
>
> Router1#**show ip ospf neighbor**

+---------------+------+---------+----------------------+----------------+
| > Neighbor ID | Pri  | State   | > Dead Time          | > Address      |
| >             |      |         |                      |                |
| > Interface   |      |         |                      |                |
+===============+======+=========+======================+================+
| > 10.3.3.3    | 0    | > FULL/ | > \- 00:00:30        | > 192.168.10.6 |
+---------------+------+---------+----------------------+----------------+
| > Serial0/0/1 |      |         |                      |                |
+---------------+------+---------+----------------------+----------------+
| > 10.2.2.2    | 0    | FULL/   | > \- 00:00:33        | > 192.168.10.2 |
+---------------+------+---------+----------------------+----------------+
| > Serial0/0/0 |      |         |                      |                |
+---------------+------+---------+----------------------+----------------+

> Router2#**show ip ospf neighbor**

+---------------+------+---------+----------------------+-----------------+
| > Neighbor ID | Pri  | > State | > Dead Time          | > Address       |
| >             |      |         |                      |                 |
| > Interface   |      |         |                      |                 |
+===============+======+=========+======================+=================+
| > 10.3.3.3    | 0    | > FULL/ | > \- 00:00:36        | > 192.168.10.10 |
+---------------+------+---------+----------------------+-----------------+
| > Serial0/0/1 |      |         |                      |                 |
+---------------+------+---------+----------------------+-----------------+
| > 10.1.1.1    | 0    | > FULL/ | > \- 00:00:37        | > 192.168.10.1  |
+---------------+------+---------+----------------------+-----------------+
| > Serial0/0/0 |      |         |                      |                 |
+---------------+------+---------+----------------------+-----------------+

> Router3#**show ip ospf neighbor**

+-------------------------+-------+---------+----------------------+----------------+
| > Neighbor ID Interface | Pri   | > State | > Dead Time          | > Address      |
+=========================+=======+=========+======================+================+
| > 10.2.2.2              | 0     | > FULL/ | > \- 00:00:34        | > 192.168.10.9 |
+-------------------------+-------+---------+----------------------+----------------+
| > Serial0/0/1           |       |         |                      |                |
+-------------------------+-------+---------+----------------------+----------------+
| > 10.1.1.1              | 0     | > FULL/ | > \- 00:00:38        | > 192.168.10.5 |
+-------------------------+-------+---------+----------------------+----------------+
| > Serial0/0/0           |       |         |                      |                |
+-------------------------+-------+---------+----------------------+----------------+

> **Step 4: Use the router-id command to change the router ID on the R1 router.**
>
> **Note:** Some IOS versions do not support the **router-id** command. If this command is not available, continue to the next Task.
>
> Router(config)#**router ospf 1**
>
> Router(config-router)#**router-id 10.4.4.4**
>
> Reload or use "clear ip ospf process" command, for this to take effect
>
> If this command is used on an OSPF router process which is already active (has neighbors), the new router-ID is used at the next reload or at a manual OSPF process restart. To manually restart the OSPF process, use the **clear ip ospf process** command.
>
> Router#(config-router)#**end**
>
> Router# **clear ip ospf process**
>
> Reset ALL OSPF processes? \[no\]:**yes** Router#

### Step 5: Restart the OSPF process using the clear ip ospf process command.

> Restarting the OSPF process forces the router to use the IP address configured on the Loopback 0 interface as the Router ID.
>
> Router(config-router)#**end** Router# **clear ip ospf process**
>
> Reset ALL OSPF processes? \[no\]:**yes** Router#

## Task: Verify OSPF Operation

> **Step 1: On the R1 router, Use the show ip ospf neighbor command to view the information about the OSPF neighbor routers R2 and R3.** You should be able to see the neighbor ID and IP address of each adjacent router, and the interface that R1 uses to reach that OSPF neighbor.

### Step 2: On the R1 router, use the show ip protocols command to view information about the routing protocol operation.

> Notice that the information that was configured in the previous Tasks, such as protocol, process ID, neighbor ID, and networks, is shown in the output. The IP addresses of the adjacent neighbors are also shown.

### Router#show ip protocols

> Routing Protocol is \"ospf 1\"
>
> Outgoing update filter list for all interfaces is not set Incoming update filter list for all interfaces is not set Router ID 10.1.1.1
>
> Number of areas in this router is 1. 1 normal 0 stub 0 nssa Maximum path: 4
>
> Routing for Networks: 172.16.1.16 0.0.0.15 area 0
>
> 10.100.x.x 0.0.0.3 area 0
>
> 10.100.x.x 0.0.0.3 area 0
>
> Routing Information Sources:
>
> Gateway Distance Last Update
>
> 10.2.2.2 110 00:11:43
>
> 10.3.3.3 110 00:11:43
>
> Distance: (default is 110) Router#
>
> Notice that the output specifies the process ID used by OSPF. Remember, the process ID must be the same on all routers for OSPF to establish neighbor adjacencies and share routing information.

## Task: Examine OSPF Routes in the Routing Tables

> View the routing table on the R1 router. OSPF routes are denoted in the routing table with an "O".

### Router#show ip route

> Codes: C - connected, S - static, I - IGRP, R - RIP, M - mobile, B - BGP
>
> D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2 E1 - OSPF external type 1, E2 - OSPF external type 2, E - EGP i - IS-IS, L1 - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS
>
> inter area
>
> \* - candidate default, U - per-user static route, o - ODR P - periodic downloaded static route
>
> Gateway of last resort is not set
>
> 10.0.0.0/8 is variably subnetted, 2 subnets, 2 masks C 10.1.1.1/32 is directly connected, Loopback0
>
> O 10.10.10.0/24 \[110/65\] via 10.100.x.x, 00:01:02, Serial0/0/0
>
> 172.16.0.0/16 is variably subnetted, 2 subnets, 2 masks C 172.16.1.16/28 is directly connected, FastEthernet0/0
>
> O 172.16.1.32/29 \[110/65\] via 10.100.x.x, 00:01:12, Serial0/0/1

+---+----------------------------------------------+-------------------------------------------------------+
|   | 10.100.x.x/30                                | > is subnetted, 3 subnets                             |
+===+==============================================+=======================================================+
| C | 10.100.x.x                                   | > is directly connected, Serial0/0/0                  |
+---+----------------------------------------------+-------------------------------------------------------+
| C | 10.100.x.x                                   | > is directly connected, Serial0/0/1                  |
+---+----------------------------------------------+-------------------------------------------------------+
| O | 10.100.x.x                                   | > \[110/128\] via 192.168.10.6, 00:01:12, Serial0/0/1 |
|   |                                              | >                                                     |
|   |                                              | > \[110/128\] via 192.168.10.2, 00:01:02, Serial0/0/0 |
+---+----------------------------------------------+-------------------------------------------------------+
