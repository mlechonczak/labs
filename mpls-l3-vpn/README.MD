# MPLS Layer 3 VPN

![MPLS topology](https://github.com/mlechonczak/labs/blob/master/mpls-l3-vpn/mpls.png)


## Loopback addresses
```
R1: 1.1.1.1/32
R2: 2.2.2.2/32
R3: 3.3.3.3/32
R4: 4.4.4.4/32
R5: 5.5.5.5/32
R6: 6.6.6.6/32
R7: 7.7.7.7/32
R8: 8.8.8.8/32
R9: 9.9.9.9/32
```

## Service Provider Network 
Service Provider is running OSPF (IGP) and MPLS in the core network (R5, R6, R7, R8).
R5 (PE1) and R9 (PE2) are iBGP neighbors (ASN: 100). 

## Client Red 
Client Red is running eBGP as CE-PE routing protocol. Both sites of Client Red have BGP ASN 65000 and because of that Service Provider on PE routers is using option as-override (another option is to use option allowas-in in both CE routers). 

## Client Purple 
Client Purple is running OSPF as CE-PE routing protocol. 
