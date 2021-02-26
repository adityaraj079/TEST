# TEST

```
Router>enable
Router#conf t
Enter configuration commands, one per line. End with CNTL/Z.
Router(config)#host R1
R1(config)#int fa0/0
R1(config-if)#ip add 192.168.10.1 255.255.255.0
R1(config-if)#no shut

R1(config-if)#
%LINK-5-CHANGED: Interface FastEthernet0/0, changed state to up

%LINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/0, changed state to up

R1(config-if)#exit

R1(config)#ip dhcp pool IP10 R1(dhcp-config)#net 192.168.10.0 255.255.255.0 R1(dhcp-config)#default 192.168.10.1 R1(dhcp-config)#exi

R1(config)#ip dhcp exc 192.168.10.1 192.168.10.10
R1(config)#exit
R1#
%SYS-5-CONFIG_I: Configured from console by console

R1#copy run start
Destination filename [startup-config]?
Building configuration...
[OK]
R1#sh run
Building configuration...

Current configuration : 631 bytes
!
version 12.2
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname R1
!
!
!
!

ip dhcp excluded-address 192.168.10.1 192.168.10.10
!
ip dhcp pool IP10
network 192.168.10.0 255.255.255.0
default-router 192.168.10.1
!
!
!
ip cef
no ipv6 cef
!

 
!
!
!
!
!
!
!
!
!
!
!
!
!

!
!
!
!
interface FastEthernet0/0

ip address 192.168.10.1 255.255.255.0
duplex auto
speed auto
!
interface FastEthernet0/1
no ip address
duplex auto
speed auto
shutdown
!
ip classless
!
ip flow-export version 9
!
!
!
!
!
!
!
!

line con 0
!
line aux 0
!
line vty 0 4
login
!
!
!
end
R1# exit

```
