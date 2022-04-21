الله المستعان # 

# CCNA Security 210-260 Cheat Sheet BY MEDHAT Fathy

# Table of Contents



- [PVLAN ](#PVLAN)
        - [Troubleshoot PVLAN](#troubleshoot-PVLAN)






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









###troubleshoot-PVLAN

| Command                                                           | Description                                                                       |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| SW1# show vlan private-vlan                                       |  gives us valuable information                                                    |
| SW1# show vlan private-vlan type                                  |  gives us a quick overview of the private VLANs                                   | 

