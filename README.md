# ZHNETWORK BIRD CONFIG
<img src="zhnetremovebg-cut.png" />
  
## ZH NET (AS202888) BGP Communities [FOR PUBLIC SERVICE]
#### Community list for ZHNET customers
6939  = Hurricane Electric  
3257  = GTT  
40676 = PSYCHZ.NET  
58057 = Securebit.ch  
#### ZHNET-LAX (PSYCHZ.NET UPSTREAM)  
<strong>No advertise communities</strong>  
666:x where is the ASN of the peer your route will not be advertised to at all   

## ZH NET (AS202888) BGP Communities [FOR INTERAL SERVICE]  
  
#### BGP Pref
upstream: bgp_local_pref = 300;  
peer: bgp_local_pref = 500;  
downstream: upstream: bgp_local_pref = 900;  
  
#### OSPF Node ID
LAX-BGP-Service = 1111  
DE-FRA = 2222 

#### IBGP IP CIDR & Range 
LAX-BGP-Service 174.136.238.114 <-> LAX Core 174.136.238.1  
LAX-BGP-Service <-> DE FRA = 10.10.19.1 - 10.10.19.2 (10.10.19.0/30) + 2a12:3fc2:5555:4444:3333:2222::1/128 - 2a12:3fc2:5555:4444:3333:2222::2/128 (OSPF+ANYCAST)  

Tanuki IX <-> Beijing CN1  10.19.1.1 10.19.1.2  
Tanuki IX <-> Beijing CN1  fddd:2233:3344:4455::2 fddd:2233:3344:4455::1001  
EOIX Henan <-> Beijing CN1 10.19.2.1 10.19.2.2
EOIX Henan <-> Beijing CN1  fddd:3344:4455:5566::2 fddd:3344:4455:5566::1001 

  

#### 202888, 6 ZHNET-CN Beijing - ZH NETWORK Beijing CN1 Facilities    
202888, 600, 65001 From Downstreams  
202888, 600, 65002 From Peers  
202888, 600, 65003 From Upstreams  

#### 202888, 1 ZHNET-LAX (PSYCHZ.NET UPSTREAM)  
202888, 1, 65001 From Downstreams  
202888, 1, 65002 From Peers  
202888, 1, 65003 From Upstreams  
  
#### 202888, 2 ZHNET-LAX (-FMT UPSTREAM)  
202888, 2, 65001 From Downstreams  
202888, 2, 65002 From Peers  
202888, 2, 65003 From Upstreams  

#### 202888, 3 ZHNET-DE (DE-FRA UPSTREAM)  
202888, 3, 65001 From Downstreams  
202888, 3, 65002 From Peers  
202888, 3, 65003 From Upstreams  
  
#### 202888, 4 ZHNET-HK (HongKong UPSTREAM) Pending - - -   
202888, 4, 65001 From Downstreams  
202888, 4, 65002 From Peers  
202888, 4, 65003 From Upstreams  
  
#### 202888, 5 ZHNET-SG (Singapore UPSTREAM) Pending - - -   
202888, 5, 65001 From Downstreams  
202888, 5, 65002 From Peers  
202888, 5, 65003 From Upstreams  

#### 202888, 6 ZHNET-CN Wuh - Tanuki-IX    
202888, 6, 65001 From Downstreams  
202888, 6, 65002 From Peers  
202888, 6, 65003 From Upstreams  

#### 202888, 7 ZHNET-CN Henan - EO-IX HENAN    
202888, 7, 65001 From Downstreams  
202888, 7, 65002 From Peers  
202888, 7, 65003 From Upstreams  
  
#### 202888, 8 ZHNET-CN GuangZhou    
202888, 8, 65001 From Downstreams  
202888, 8, 65002 From Peers  
202888, 8, 65003 From Upstreams  

#### 202888, 9 ZHNET-CN Seattle    
202888, 9, 65001 From Downstreams  
202888, 9, 65002 From Peers  
202888, 9, 65003 From Upstreams  

