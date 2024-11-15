# lab06 - Create S2S

---

## Topology
<img src="https://i.imgur.com/hZuS5Yr.png">

---

## cfg Remote-FG
````sh
# static ip - Remote-FG
config system interface
edit port2
set alias LAN
set role lan
set ip 10.0.2.254/24
set allowaccess http ping https ssh
next
end

# dhcp port2 - Remote-FG
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
set hostname Remote-FG
set admintimeout 60
end
````

---

## Local-FG
````sh
# static ip - Local-FG
config system interface
edit port2
set alias LAN
set role lan
set ip 10.0.1.254/24
set allowaccess http ping https ssh
next
end

# dhcp port2 - Local-FG
config system dhcp server
edit 2
set dns-service default
set default-gateway 10.0.1.254
set netmask 255.255.255.0
set interface "port2"
config ip-range
edit 1
set start-ip 10.0.1.1
set end-ip 10.0.1.99
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
set hostname Local-FG
set admintimeout 60
end
````
