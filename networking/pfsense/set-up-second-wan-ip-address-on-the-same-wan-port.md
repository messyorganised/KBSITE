# Set up second WAN IP address on the same WAN port



## Intro

This article will provide you with a step-by-step guide on how to configure a second WAN IP address on the same WAN port supplied by the same ISP.



This is helpful for sites that host other user's services and they would like the entire network from internal to external to be separated from each other as this configuration will forces the target network to utilize an external address different from the primary address.



### Prerequisite:

A fully configured, fully working WAN interface.

Known support for multiple WAN IP address and valid multiple WAN IP addresses assigned for the premise. (Discuss with ISP )



1. Go to Firewall > Virtual IPs > Add.&#x20;
2. Set the new Virtual IP with the following configurations.

Type: IP Alias

Interface: Your WAN interfaces

Address type: Single Address

Address(es): Your secondary WAN IP address /29

Description: Your description of the Virtual IP. For easier identification

3. Go to Firewall > NAT > Outbound.
4. Set your mode to Hybrid Outbound NAT rule generation.
5. Add new mappings.
6. Set the new Mappings as per following:

Interface: WAN

Address Family: IPv4+IPv6

Protocol: any

Source: Your network source(s). (the LAN network)

Destination: any



Translation

Address: The newly created Virtual IP

Description: Your description of the Virtual IP. For easier identification.



Save your changes and youre done!
