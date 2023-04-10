### 1
```
install wireguard-dkms wireguard-tools -y
```
### 2
```
cd /etc/wireguard  
wg genkey | tee privatekey | wg pubkey > publickey   
chmod 777 -R /etc/wireguard  
```
### conf
```
[Interface]  
PrivateKey =  
Address =  x.x.x.x/24, xxxx:xxxx::x/64
PostUp = /spin/ip addr add dev %i x.x.x.x/32 peer x.x.x.x/32
ListenPort =  
table = off
mtu = 1300
​
[Peer]
PublicKey =  
AllowedIPs =  
EndPoint =  
PersistentKeepalive =  
```
## up
```
wg-quick up xxx
```
### kernel :RTNETLINK answers: Operation not supported 
```
modprobe wireguard
```
4.19.0.-22  
```
apt install linux-headers-4.19.0-22-amd 
```
