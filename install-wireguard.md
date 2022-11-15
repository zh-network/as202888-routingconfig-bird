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