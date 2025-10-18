# Level 1: Network Foundations — <your-handle>

## Objective
Build a functional SOHO network in Cisco Packet Tracer.

## Topology
- 2 PCs
- 1 Switch
- 1 Router

## IP Addressing Scheme
| Device | Interface | IP Address | Subnet Mask | Gateway |
|---------|------------|-------------|--------------|----------|
| Router  | G0/0       | 192.168.1.1 | 255.255.255.0 | - |
| PC0     | FA0        | 192.168.1.2 | 255.255.255.0 | 192.168.1.1 |
| PC1     | FA0        | 192.168.1.3 | 255.255.255.0 | 192.168.1.1 |

## Verification
Both PCs should be able to ping each other successfully.
