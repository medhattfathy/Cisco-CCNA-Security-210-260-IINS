# Cisco-CCNA-Security-210-260-IINS
Cisco CCNA Security 210-260 IINS 
#table of content


| Command                                                       | Description                                    |
|:--------------------------------------------------------------|:-----------------------------------------------|
| (config)# interface range g1/1 - 2                            | configure g1/1 and g1/2 at the same time       |
| (config-if-range)# channel-group 1 mode {auto, desirable}     | Add both interfaces to etherchannel 1 (PAgP)   |
| (config-if-range)# channel-group 1 mode {active, passive}     | Add both interfaces to etherchannel 1 (LACP)   |
| (config-if-range)# channel-group 1 mode on                    | Add both interfaces to etherchannel 1 (Static) |
| (config)# interface port-channel 1                            | Configure virtual interface for etherchannel 1 |
| (config-if)# switchport mode trunk                            | Put etherchannel 1 in trunk mode               |
| (config-if)# switchport trunk allowed vlan 10,20,30           | Add tagged vlans 10,20,30 on ethercahnnel 1    |



### Troubleshoot Etherchannel (Link Aggregation)

| Command                            | Description                                           |
|:-----------------------------------|:------------------------------------------------------|
| # show interface port-channel 1    | Has the combined bandwidth and members as extra info. |
| # show etherchannel summary        | Show etherchannel protocols and members as a list     |
| # show etherchannel port-channel 1 | Show per member state and stats                       |
