
# بسم الله الرحمن الرحيم 
الله المستعان # 

# CCNA Security 210-260 Cheat Sheet BY MEDHAT Fathy

# Table of Contents


- [Port Security ](#Port-Security)
    - [Troubleshoot Port Security](#troubleshoot-Port-Security)


- [PVLAN ](#PVLAN)
    - [Troubleshoot PVLAN](#troubleshoot-PVLAN)
    







## Port-Security

| Command                                                              | Description                                                                       |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| Switch(config)# interface FastEthernet 0/1                           | enter interface                                                                   |
| Switch(config-if)# switchport mode access                            | set the interface to access mode.                                                 |
| Switch(config-if)# switchport port-security                          | enables the port security on a switch.                                            |
| Switch(config-if)# switchport port-security maximum max-addr         | specify the maximum number of MAC addresses {1-1024}                              |
| Switch(config-if)#switchport port-security mac-address 0013.0002.0023| define one or more MAC addresses that are allowed on a switch interface           |
| Switch(config-if)# switchport port-security mac-address sticky       | configure a static address entry on an interface.                                 |
| Switch(config-if)#switchport port-security violation restrict        | If a violation occurs, you want the port to be configured in restrict mode.       |
| Switch(config-if)#switchport port-security violation shutdown        | If a violation occurs, you want the port to be configured in shutdown mode        |
| Switch(config-if)#switchport port-security violation protect         | If a violation occurs, you want the port to be configured in protect mode         |

![145](https://user-images.githubusercontent.com/88751099/164518916-a6243c72-e4ad-484d-a4a9-14ca74807560.png)


### troubleshoot-Port-Security

| Command                                                              | Description                                                                       |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| Switch# show port-security interface FastEthernet 0/1                |                                                                                   |
| Switch# show port-security address                                   |  Secure Mac Address Table                                                         |
| Switch(config)# interface FastEthernet 0/2                           | if it  unused  interface                                                          |
| Switch(config-if)# shutdown                                          |                                                                                   |




## PVLAN 
| Command                                                           | Description                                                                       |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| (config)# vtp mode transparent                                    | Setting device to VTP TRANSPARENT mode.                                           |
| (config)# vlan 501                                                | Create Vlan                                                                       |
| (config-vlan)# private-vlan community                             | switch this type to  a community VLAN                                             |
| (config-vlan)# vlan 500                                           | creating VLAN 500                                                                 |
| (config-vlan)# private-vlan primary                               | switch this type to  a primary  VLAN                                              |
| (config-vlan)# private-vlan association add 501                   | telling the switch that VLAN 501 is a secondary VLAN                              |
| (config)# vlan 502                                                | creating VLAN 500                                                                 |
| (config-vlan)# private-vlan isolated                              | switch this type to  a isolated  VLAN                                             |
| (config-vlan)#  vlan 500                                          | enter vlan 500                                                                    |
| (config-vlan)#private-vlan association add 502                    | add the association between the primary and secondary VLAN                        |
| (config)#interface range fa0/1 - 2                                | enter Interface fa0/1 and fa0/2                                                   |
| (config-if-range)#switchport mode private-vlan host               | tell the switch that these are host ports                                         |
| (config-if-range)#switchport private-vlan host-association 500 501| tell the switch that VLAN 500 is the primary VLAN and 501 is the secondary VLAN.  |
| (config)# interface fa0/24                                        | inter  Interface fa0/24                                                           |
| (config-if)# switchport mode private-vlan promiscuous             |  switch this type to  a promiscuous  VLAN                                         |
| (config-if)# switchport private-vlan mapping 500 501,502          |  create a mapping between VLAN 500 (primary) and VLAN 502,502 (secondary).        | 



<!-- MEDHAT FATHY -->



### troubleshoot-PVLAN

| Command                                                           | Description                                                                       |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| SW1# show vlan private-vlan                                       |  gives us valuable information                                                    |
| SW1# show vlan private-vlan type                                  |  gives us a quick overview of the private VLANs                                   | 




