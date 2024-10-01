# lab01 -FG & win10

---

## cfg FG
````sh
# cfg WAN
config system interface
edit port1
set alias wan
set role wan
next
end

# cfg port2 lan static ip
config system interface
edit port2
set mode static
set ip 10.46.0.1/24
set alias LAN
set allowaccess ping http https
next
end

# cfg dhcp srv on port2 - lan
config system dhcp server
edit 2
set dns-service default
set default-gateway 10.46.0.1
set netmask 255.255.255.0
set interface "port2"
config ip-range
edit 1
set start-ip 10.46.0.2
set end-ip 10.46.0.99
next
end
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
````
