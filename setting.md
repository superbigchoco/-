# BGP1

---

set protocols bgp system-as <自AS>

set protocols bgp parameters router-id <IPv4アドレス>

set protocols bgp neighbor <相手IP> remote-as <相手AS>

set protocols bgp address-family ipv4-unicast

set protocols bgp neighbor <相手IP> address-family ipv4-unicast

---

# BGP2

---

set protocols bgp system-as <自AS>

set protocols bgp parameters router-id <IPv4アドレス>

set protocols bgp neighbor <相手IP> remote-as <相手AS>

set protocols bgp address-family ipv4-unicast

set protocols bgp neighbor <相手IP> address-family ipv4-unicast

---

# BGP3

---

set protocols bgp system-as <自AS>

set protocols bgp parameters router-id <IPv4アドレス>

set protocols bgp neighbor <相手IP> remote-as <相手AS>

set protocols bgp address-family ipv4-unicast

set protocols bgp neighbor <相手IP> address-family ipv4-unicast

---

# other
---

set interfaces ethernet eth0 pppoe 0 user-id 'user@example'

set interfaces ethernet eth0 pppoe 0 password 'password'

set interfaces ethernet eth0 pppoe 0 default-route auto

set interfaces ethernet eth0 pppoe 0 mtu '1454'

set protocols bgp system-as 65001

set protocols bgp parameters router-id 192.0.2.1

set protocols bgp neighbor 203.0.113.1 remote-as 65000

set protocols bgp address-family ipv4-unicast

set protocols bgp neighbor 203.0.113.1 address-family ipv4-unicast

---

## client(PPPoE)

---

set interfaces ethernet eth0 pppoe 0 user-id 'testuser'

set interfaces ethernet eth0 pppoe 0 password 'testpass'

set interfaces ethernet eth0 pppoe 0 default-route auto

---

---
- set interfaces ethernet eth0 address '10.0.0.1/24'

- set service pppoe-server interface eth0
- set service pppoe-server authentication local-users username testuser password 'testpass'
- set service pppoe-server client-ip-pool start '10.0.0.10'
- set service pppoe-server client-ip-pool stop  '10.0.0.10'
---
