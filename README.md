# Inter-VLAN-Routing-
Implementing Inter-VLAN Routing using 802.1Q encapsulation, trunking, switch port security, and sub-interface on Cisco Catalyst switches and ISR routers.

(Router)(R1) --> CISCO 4331/ ISR 4221
(Switches)(S1,S2) --> Cisco Catalyst 2960
(Hosts)--> PC-A (CLAN 20), PC-B (VLAN 30)

ADDRESSING TABLE

| Device | Interface   |  IP Address  |  Subnet Mask  | Default Gateway  |
--------------------------------------------------------------------------
|   R1   |  G0/0/1.10  | 192.168.10.1 | 255.255.255.0  |        -        |
|   R1   |  G0/0/1.20  | 192.168.20.1 | 255.255.255.0  |        -        |
|   R1   |  G0/0/1.30  | 192.168.30.1 | 255.255.255.0  |        -        |
|   R1   | G0/0/1.1000 |       -      |       -        |        -        |
|   S1.  |   VLAN 10   | 192.168.10.11 | 255.255.255.0 |  192.168.10.1   |
|   S2   |   VLAN 10   | 192.168.10.12 | 255.255.255.0 |  192.168.10.1   |
|  PC-A  |     NIC     | 192.168.20.3  | 255.255.255.0 |   192.168.20.1  |
|  PC-B  |     NIC     | 192.168.30.3  | 255.255.255.0 |  192.168.30.1   |

VLAN TABLE 

| VLAN |     Name    |                      Interface Assigned                        |
---------------------------------------------------------------------------------------
|  10  |  Management |                    S1: VLAN 10, S2: VLAN 10                    |
|  20  |   Sales     |                           S1: F0/6                             |
|  30  |  Operations |                           S2: F0/18                            |
|  999 | Parking_Lot |   S1: F0/2-4, F0/7-24, G0/1-2<br>S2: F0/2-17, F0/19-24, G0/1-2 |
| 1000 |   Native    |                               -                                |
 
