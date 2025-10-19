-> **SOHO Network:**

  This is a simple small office home office (SOHO) network made using Cisco Packet Tracer. 

  It includes: 2 PCs, 1 Switch (cisco 2960), and 1 Router (cisco 2911). Copper Straight-Through cables have been used, and static IPv4 addressing     (192.168.1.0 network). The PCs are connected to the switch, and the switch is connected to the router.

---------------------------------------------------------------------------------------------------------------------------------------------------



-> **IP Scheme:**

  Static IPs were assigned from the 192.168.1.0/24 network:



 | Device       | Interface           | IP Address     | Subnet Mask       | Default Gateway  |

 | PC0          | FastEthernet0       | 192.168.1.10   | 255.255.255.0     | 192.168.1.1      |

 | PC1          | FastEthernet0       | 192.168.1.11   | 255.255.255.0     | 192.168.1.1      |

 | Router0      | GigabitEthernet0/0  | 192.168.1.1    | 255.255.255.0     |                  |

---------------------------------------------------------------------------------------------------------------------------------------------------

-> **Ping Results:**

  Ping from PC0 to PC1:

  Reply from 192.168.1.11: bytes=32 time=9ms TTL=128
  Reply from 192.168.1.11: bytes=32 time<1ms TTL=128
  Reply from 192.168.1.11: bytes=32 time<1ms TTL=128
  Reply from 192.168.1.11: bytes=32 time<1ms TTL=128



  Ping from PC1 to PC0:

  Reply from 192.168.1.10: bytes=32 time<1ms TTL=128
  Reply from 192.168.1.10: bytes=32 time<1ms TTL=128
  Reply from 192.168.1.10: bytes=32 time<1ms TTL=128
  Reply from 192.168.1.10: bytes=32 time<1ms TTL=128

  Successful communication established between the 2 PCs, connectivity verified using ICMP ping.

---------------------------------------------------------------------------------------------------------------------------------------------------



