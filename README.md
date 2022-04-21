الله المستعان # 

# CCNA Security 210-260 Cheat Sheet BY MEDHAT Fathy

# Table of Contents



- [PVLAN ](#PVLAN)
        - [Troubleshoot PVLAN](#troubleshoot-PVLAN)






## PVLAN 
| Command                                                         | Description                                               |
|:----------------------------------------------------------------|:----------------------------------------------------------|
| (config)# vtp mode transparent                                  | Setting device to VTP TRANSPARENT mode.                   |
| (config)# vlan 501                                              | Create Vlan                                               |
| (config-vlan)# private-vlan community                           | switch this type to  a community VLAN                     |
| (config-vlan)# vlan 500                                         | creating VLAN 500                                         |
| (config-vlan)# private-vlan primary                             | switch this type to  a primary  VLAN                      |
| (config-vlan)# private-vlan association add 501                 | telling the switch that VLAN 501 is a secondary VLAN      |
| (config)# vlan 502                                              | creating VLAN 500                                         |
| (config-vlan)# private-vlan isolated                            | switch this type to  a isolated  VLAN                     |
| (config-vlan)#  vlan 500                                        | enter vlan 500                                            |
| (config-vlan)#private-vlan association add 502                  | add the association between the primary and secondary VLAN|
|
