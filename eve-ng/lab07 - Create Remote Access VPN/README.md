# lab07 - Create Remote Access VPN

---

## Topology
<img src="https://raw.githubusercontent.com/pc-aide/FCA/refs/heads/main/eve-ng/lab07%20-%20Create%20Remote%20Access%20VPN/Lab07%20-%20Create%20Remote%20Access%20VPN.png">

---

## cfg FG-Remote
````sh
# static ip - FG-Remote
config system interface
edit port2
set alias LAN
set role lan
set ip 10.0.2.254/24
set allowaccess http ping https ssh
next
end

# dhcp port2 - FG-Remote
config system dhcp server
edit 2
set dns-service default
set default-gateway 10.0.2.254
set netmask 255.255.255.0
set interface "port2"
config ip-range
edit 1
set start-ip 10.0.2.1
set end-ip 10.0.2.99
next
end
next
end

# cfg WAN
config system interface
edit port1
set alias WAN
set role wan
next
end

# cfg fw policy - Allow LAN - WAN - internet
config firewall policy
edit 1
set name "Allow LAN-To-WAN - Internet"
set srcintf "port2"
set dstintf "port1"
set action accept
set srcaddr "all"
set dstaddr "all"
set schedule "always"
set service "Web Access"
set logtraffic all
set nat enable
next
end

# cfg system global
config system global
set hostname FG-Remote
set admintimeout 60
end

# remove popUP what 's new in fortios 7.0
config system admin
edit admin
set gui-ignore-release-overview-version "7.0.0"
end
````

---

## Requirements
### IKEv1
1. same config between the client device & router device
   1. Mode Agressive or Main - both on FG & Windows
<img src="https://github.com/pc-aide/FCP-SO/blob/main/CLI/mode%20aggressive.png">


#### Phase 1
1. IKE Proposal - Encryption & auth
<img src="https://github.com/pc-aide/FCP-SO/blob/main/CLI/diag%20vpn%20ipsec%20status.png?raw=true">
3. DH Group
