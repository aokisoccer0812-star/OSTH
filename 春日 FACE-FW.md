## Hostname: RJFF-FDMS-FW01
Model: srx320
Junos: 20.4R3-S3.4

## services
ssh
telnet
xnm-clear-text
web-management http interface reth0.0, ge-0/0/2.0
web-management https system-generated-certificate,  reth0.0, ge-0/0/2.0
dhcp router 192.168.1.1, low 192.168.1.2, high 192.168.1.254, propagate-settings ge-0/0/0.0
name-server 208.67.222.222, 208.67.220.220
ntp server 10.107.190.5


## security zones
### Trust
host-inbound-traffic system-services all
host-inbound-traffic protocols ospf
interfaces ge-0/0/2.0
### Untrust
host-inbound-traffic system-services all
host-inbound-traffic protocols ospf
interfaces ge-0/0/3.0
interfaces ge-0/0/4.0


## interfaces
ge-0/0/2 unit 0 family inet address 10.107.190.251/24
ge-0/0/3 unit 0 family inet address 10.2.70.100/24
ge-0/0/4 unit 0 family inet address 10.2.67.100/24
lo0 unit 0 family inet filter input ACCESS-FILTER


## prefix-list
MANAGER-IP 10.101.190.0/24, 10.102.190.0/24, 10.107.190.0/24


## firewall filter
### ACCESS-FILTER term 10
from source-address 0.0.0.0/0
from source-prefix-list MANAGER-IP except
from protocol tcp
from destination-port ssh
from destination-port https
from destination-port telnet
from destination-port http
discard
### ACCESS-FILTER term 20
accept


## routing-options
static route 10.101.190.0/24 next-hop 10.107.190.254
static route 10.19.2.0/24 next-hop 10.107.190.254
router-id 10.2.67.251


## FADP-Trust
ATSDB1 10.107.190.121/32
ATSDB2 10.107.190.122/32
FACE-AD-TZ-IN-11 10.101.190.11/32
FACE-AD-TZ-IN-14 10.101.190.14/32
FACE-AD-FF-IN-11 10.107.190.11/32
FACE-AD-FF-IN-14 10.107.190.14/32
FACE-WS-TZ-IN-140 10.101.190.140/32
FACE-WS-TZ-IN-141 10.101.190.141/32
FACE-WS-TZ-IN-142 10.101.190.142/32
FACE-WS-TZ-IN-143 10.101.190.143/32
FACE-WS-FF-IN-137 10.107.190.137/32
FACE-WS-FF-IN-138 10.107.190.138/32
FACE-WS-FF-IN-148 10.107.190.148/32
FACE-WS-FF-IN-149 10.107.190.149/32
FACE-AD-FF-IN-13 10.107.190.13/32
FACE-WS-FF-IN-15 10.107.190.15/32
EPO-112 10.19.2.112/32
EPO-92 10.19.2.92/32

FADP-G = ATSDB1, ATSDB2, FADP01, FADP51
FACE-AD-IN-G = FACE-AD-TZ-IN-11, 14; FACE-AD-FF-IN-11, 14, 13; FACE-WS-FF-IN-137, 138, 148, 149, 15; EPO-112, 92

## FDMS-Untrust
FDPS01-1 10.1.3.1/32
FDPS01-2 10.1.3.2/32
FDPS51-1 10.1.3.51/32
FDPS51-2 10.1.3.52/32
FDPS01-11 10.2.70.176/32
FDPS01-21 10.2.70.177/32
FDPS51-11 10.2.70.178/32
FDPS51-21 10.2.70.179/32
FACE31 172.19.30.101/32
FACE31-21 10.2.70.191/32
Router51 10.2.67.205/32
FACE-FDPS-1 172.19.32.100/32
FACE-FDPS-11 172.19.32.102/32
FACE-FDPS-21 172.18.32.105/32
FACE-AD-OUT-1 10.2.70.1/32

FDMS-G = FDPS01-1, 2, 11, 21; FDPS51-1, 2, 11, 21; FACE31, FACE31-21; FACE-FDPS-1, 11, 21
FACE-AD-OUT-G = FACE-AD-OUT-1


## FROM-UNTRUST rule U-T-5
destination-address 10.2.67.1/32
static-nat prefix 10.107.190.121/32

## FROM-UNTRUST rule U-T-6 ==deactivate==
destination-address 10.2.67.1/32
static-nat prefix 10.107.190.1/32

## FROM-UNTRUST rule U-T-1
destination-address 10.2.67.2/32
static-nat prefix 10.107.190.122/32

## FROM-UNTRUST rule U-T-2 ==deactivate==
destination-address 10.2.67.2/32
static-nat prefix 10.107.190.2/32

## FROM-UNTRUST rule U-T-3 ==deactivate==
destination-address 10.2.70.4/32
static-nat prefix 10.107.190.122/32

## FROM-UNTRUST rule U-T-4 ==deactivate==
destination-address 10.2.70.4/32
static-nat prefix 10.107.190.2/32

## FROM-UNTRUST rule U-T-10
destination-address 10.2.70.11/32
static-nat prefix 10.101.190.11/32

## FROM-UNTRUST rule U-T-11
destination-address 10.2.70.14/32
static-nat prefix 10.101.190.14/32

## FROM-UNTRUST rule U-T-12
destination-address 10.2.70.21/32
static-nat prefix 10.107.190.11/32

## FROM-UNTRUST rule U-T-13
destination-address 10.2.70.24/32
static-nat prefix 10.107.190.14/32

## FROM-UNTRUST rule U-T-110
destination-address 10.2.70.137/32
static-nat prefix 10.107.190.137/32

## FROM-UNTRUST rule U-T-111
static-nat prefix 10.107.190.138/32
destination-address 10.2.70.148/32

## FROM-UNTRUST rule U-T-112
destination-address 10.2.70.148/32
static-nat prefix 10.107.190.148/32

## FROM-UNTRUST rule U-T-113
destination-address 10.2.70.149/32
static-nat prefix 10.107.190.149/32

## FROM-UNTRUST rule U-T-114
destination-address 10.2.70.13/32
static-nat prefix 10.107.190.13/32

## FROM-UNTRUST rule U-T-115
destination-address 10.2.70.15/32
static-nat prefix 10.107.190.15/32

## FROM-TRUST rule T-U-1 ==deactivate==
destination-address 10.107.190.170/32
static-nat prefix 10.1.3.1/32

## FROM-TRUST rule T-U-2 ==deactivate==
destination-address 10.107.190.171/32
static-nat prefix 10.1.3.2/32

## FROM-TRUST rule T-U-3 ==deactivate==
destination-address 10.107.190.172/32
static-nat prefix 10.1.3.51/32

## FROM-TRUST rule T-U-4 ==deactivate==
destination-address 10.107.190.173/32
static-nat prefix 10.1.3.52/32

## FROM-TRUST rule T-U-5
destination-address 10.107.190.182/32
static-nat prefix 10.2.67.205/32

## FROM-TRUST rule T-U-6
destination-address 10.107.190.176/32
static-nat prefix 10.2.70.176/32

## FROM-TRUST rule T-U-7
destination-address 10.107.190.177/32
static-nat prefix 10.2.70.177/32

## FROM-TRUST rule T-U-8
destination-address 10.107.190.178/32
static-nat prefix 10.2.70.178/32

## FROM-TRUST rule T-U-9
destination-address 10.107.190.179/32
static-nat prefix 10.2.70.179/32

## FROM-TRUST rule T-U-10
destination-address 10.107.190.189/32
static-nat prefix 172.19.30.101/32

## FROM-TRUST rule T-U-11
destination-address 10.107.190.191/32
static-nat prefix 10.2.70.191/32

## FROM-TRUST rule T-U-0
destination-address 10.107.190.170/32
static-nat prefix 172.19.32.100/32

## FROM-TRUST rule T-U-20
destination-address 10.107.190.60/32
static-nat prefix 10.2.70.1/32


## Trust to Untrust
### FDMS-FDPS01-1
source-address FADP-G
destination-address FDPS01-1
destination-address FACE-FDPS-1
destination-address FACE-FDPS-11
application FADP-SERVER = tcp-59001, 57001, 57002, 59101, 57101, 57102
application FDMS-SERVER = tcp-9001, 7001, 7002, 9101, 7101, 7002, 20030, 20032, 20212
application PING = junos-icmp-all
application TRACEROUTE = troute = udp 33434-33534

### FDMS-FDPS01-2
source-address FADP-G
destination-address FDPS01-2
application FADP-SERVER
application FDMS-SERVER
application PING
application TRACEROUTE

### FDMS-FDPS51-1
source-address FADP-G
destination-address FDPS51-1
application FADP-SERVER
application FDMS-SERVER
application PING
application TRACEROUTE

### FDMS-FDPS51-2
source-address FADP-G
destination-address FDPS51-2
application FADP-SERVER
application FDMS-SERVER
application PING
application TRACEROUTE

### FDMS-FACE31
source-address FADP-G
destination-address FACE31
application FADP-SERVER
application FDMS-SERVER
application PING
application TRACEROUTE

### FDMS-FDPS01-11
source-address FADP-G
destination-address FDPS01-11
application FADP-SERVER
application FDMS-SERVER
application PING
application TRACEROUTE

### FDMS-FDPS01-21
source-address FADP-G
destination-address FDPS01-21
application FADP-SERVER
application FDMS-SERVER
application PING
application TRACEROUTE

### FDMS-FDPS51-11
source-address FADP-G
destination-address FDPS51-11
application FADP-SERVER
application FDMS-SERVER
application PING
application TRACEROUTE

### FDMS-FDPS51-21
source-address FADP-G
destination-address FDPS51-21
application FADP-SERVER
application FDMS-SERVER
application PING
application TRACEROUTE

### FDMS-FACE31-21
source-address FADP-G
destination-address FACE31-21
application FADP-SERVER
application FDMS-SERVER
application PING
application TRACEROUTE

### ROUTER
source-address any
destination-address Router51
application PING
application TELNET
application TRACEROUTE


## Untrust to Trust
### test ==deactivate==
source-address any
destination-address any
application any

### ATSDB1
source-address FDMS-G
destination-address ATSDB1
application FDMS-SERVER
application FADP-SERVER
application PING
application TRACEROUTE

### ATSDB2
source-address FDMS-G
destination-address ATSDB2
application FDMS-SERVER
application FADP-SERVER
application PING
application TRACEROUTE

### FADP01
source-address FDMS-G
destination-address FADP01
application PING
application FDMS-SERVER
application FADP-SERVER
application TRACEROUTE

### FADP51
source-address FDMS-G
destination-address FADP51
application PING
application FDMS-SERVER
application FADP-SERVER
application TRACEROUTE

### FACE-WS-AD-U-T ==deactivate==
source-address FACE-AD-OUT-G
destination-address FACE-AD-IN-G
application PING
application TRACEROUTE
application KERBEROS = TCP-88, UDP-88
application DNS = junos-dns-tcp, junos-dns-udp
application NTP = junos-ntp
application UDP-135, 137, 138, 389
application TCP-139, 389, 445, 636, 464, 3268, 3269, 9389

### FACE-WS-AD-U-T-per
source-address FACE-AD-OUT-G
destination-address FACE-AD-IN-G
application any












