## Hostname: RJFF-DII-FW01
Model: srx320
Junos: 20.4R3-S3.4
10.107.190.253/24

## Hostname: RJFF-DII-FW02
Model: srx320
Junos: 20.4R3-S3.4
10.107.190.252/24

## services
ssh
telnet
xnm-clear-text
web-management http/https interface ge-0/0/2.0, reth0.0, ge-3/0/2.0
dhcp router 192.168.1.1, low 192.168.1.2, high 192.168.1.254, propagate-settings ge-0/0/0.0
name-server 208.67.222.222, 208.67.220.220
ntp server 10.107.190.5


## security zone
### Trust
host-inbound-traffic system-services all
host-inbound-traffic protocols ospf
interfaces reth0.0
### DMZ
host-inbound-traffic system-services all
host-inbound-traffic protocols ospf
interfaces reth1.0
### Untrust
host-inbound-traffic system-services all
host-inbound-traffic protocols ospf
interfaces reth2.0


## interfaces
ge-0/0/2 gigether-options redundant-parent reth0
ge-0/0/3 gigether-options redundant-parent reth1
ge-0/0/4 gigether-options redundant-parent reth2
ge-3/0/2 gigether-options redundant-parent reth0
ge-3/0/3 gigether-options redundant-parent reth1
ge-3/0/4 gigether-options redundant-parent reth2
fab0 fabric-options member-interfaces ge-0/0/5
fab1 fabric-options member-interfaces ge-3/0/5
lo0 unit 0 family inet filter input ACCESS-FILTER
reth0 redundant-ether-options redundancy-group 1
reth0 unit 0 family inet address 10.107.190.254/24
reth1 redundant-ether-options redundancy-group 2
reth1 unit 0 family inet address 10.107.189.12/28
reth2 redundant-ether-options redundancy-group 3
reth2 unit 0 family inet address 10.107.189.26/28


## prefix-list
MANAGER-IP 10.101.190.0/24, 10.102.190.0/24, 10.107.190.0/24
PREFIX-RJFF 10.107.189.0/28, 10.107.190.0/24


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


## RJFF-Untrust
RJTZ-NETWORK 10.101.190.0/24
RJTZ-190-(NW|WS)-x 10.101.190.x/32
RJTZ-191-WS-1, 2 10.101.191.1, 2/32
RJTZ-189-WS-1 10.101.189.1/32
RJCJ-190-(NW|WS)-x 10.94.190.x/32
RJSM-190-(NW|WS)-x 10.95.190.x/32
RJSK-190-(NW|WS)-x 10.125.190.x/32
RJST-190-(NW|WS)-x 10.96.190.x/32
RJAH-190-(NW|WS)-x 10.100.190.x/32
RJTJ-190-(NW|WS)-x 10.99.190.x/32
RJTY-190-(NW|WS)-x 10.167.190.x/32
RJAI-190-(NW|WS)-x 10.91.190.x/32
RJAW-190-(NW|WS)-x 10.126.190.x/32
RJNY-190-(NW|WS)-x 10.143.190.x/32
RJNH-190-(NW|WS)-x 10.104.190.x/32
RJNA-190-(NW|WS)-x 10.102.190.x/32
RJNG-190-(NW|WS)-x 10.103.190.x/32
RJNK-190-(NW|WS)-x 10.105.190.x/32
RJSN-190-(NW|WS)-x 10.134.190.x/32
RJOH-190-(NW|WS)-x 10.106.190.x/32
RJOF-190-(NW|WS)-x 10.150.190.x/32
RJFF-191-(NW|WS)-x 10.107.191.x/32
RJFF2-190-(NW|WS)-x 10.151.132.x/32
RJFA-190-(NW|WS)-x 10.152.190.x/32
RJFZ-190-(NW|WS)-x 10.108.190.x/32
RJFN-190-(NW|WS)-x 10.109.190.x/32
ROAH-190-(NW|WS)-x 10.110.190.x/32
RJSO-164-(NW|WS)-x 10.53.164.x/32
RJSH-164-(NW|WS)-x 10.60.164.x/32
RJTL-164-(NW|WS)-x 10.62.164.x/32
RJTE-164-(NW|WS)-x 10.14.164.x/32
RJTA-164-(NW|WS)-x 10.9.164.x/32
RJAW-153--(NW|WS)-x 10.61.153.x/32
RJOS-164-(NW|WS)-x 10.28.164.x/32
RJOP-164-(NW|WS)-x 10.27.164.x/32
RJBM-164-(NW|WS)-x 10.65.164.x/32
RJOI-164-(NW|WS)-x 10.33.164.x/32
RJOZ-164-(NW|WS)-x 10.47.164.x/32
RJDU-164-(NW|WS)-x 10.46.164.x/32
RJFY-164-(NW|WS)-x 10.45.164.x/32
RJCJ-191-(NW|WS)-x 10.94.191.x/32
RJSM-191-(NW|WS)-x 10.95.191.x/32
RJST-191-(NW|WS)-x 10.96.191.x/32
RJAH-191-(NW|WS)-x 10.100.191.x/32
RJTJ-191-(NW|WS)-x 10.99.191.x/32
RJTY-191-(NW|WS)-x 10.167.191.x/32
RJAI-5-WS-10, 100 10.88.5.10, 100/32
RJAI-2-WS-1 10.7.2.1/32
RJNH-191-(NW|WS)-x 10.104.191.x/32
RJNA-191-(NW|WS)-x 10.102.191.x/32
RJNG-158-WS-67 10.103.156.67/32
RJ-JYUHO-156-WS-67 10.93.158.67/32
RJNK-191-(NW|WS)-x 10.105.191.x/32
RJOH-191-(NW|WS)-x 10.106.191.x/32
RJFF-191-(NW|WS)-x 10.107.191.x/32
RJFA-191-(NW|WS)-x 10.152.191.x/32
RJFZ-191-(NW|WS)-x 10.108.191.x/32
RJFN-191-(NW|WS)-x 10.109.191.x/32
ROAH-191-(NW|WS)-x 10.110.191.x/32
RJSH-254-WS-138 10.60.254.138/32
RJSO-254-WS-82 10.53.254.82/32
RJTL-163-WS-1 - 4 10.62.163.1 - 4/32
RJTE-162-WS-1 - 4 10.62.162.1 - 4/32
RJTA-160-WS-1 - 4 10.9.160.1 - 4/32
RJOS-160-WS-1 - 4 10.28.160.1 - 4/32
RJFY-160-WS-1 - 4 10.45.160.1 - 4/32
RJAW-254-NW-58 10.61.254.58/32
RJFF-NETWORK_8 10.107.186.0/24
RJTZ-NETWORK_8 10.101.188.0/24
RJAI-7-WS-10, 12 10.88.7.10, 12/32
RJTZ-181-WS-129, 131 10.101.181.129, 131/32
RJFF-181-WS-101, 103 10.107.181.101, 103/32
RJAI-5-WS-11 10.7.5.11/32
RJTZ-254-NW-209 10.107.254.17/32
RJTZ-254-NW-217 10.107.254.25/32
RJTZ-254-WS-210 10.107.254.18/32
RJTZ-254-WS-218 10.107.254.26/32
RJTZ-190-WS-60 10.101.190.60/32
DII-EPO-19-112 10.19.2.112/32
DII-EPO-19-92 10.19.2.92/32
DII-NTP-16-51 10.16.1.51/32
DII-NTP-19-51 10.19.1.51/32
DII-WSUS-16-61 10.16.2.61/32
DII-WSUS-19-61 10.19.2.61/32
web-RJSO-x-WS-y 10.121.x.y/32
web-(略)

RJFF-IN-GAIBU-G = RJFF-191-WS-1, 2; RJFF-181-WS-101, 103; RJFF-233-WS-144, 145
RJTZ-HOST-G = RJTZ-190-WS-1, 2
RJTZ-NIN-G = RJTZ-190-WS-11, 14
RJTZ-IN-WS-KYOKUNAI-G = RJTZ-190-WS-130 - 135, 137, 138, 140 - 143
RJFF-OT-WS-G = RJTZ-254-NW-209, 217; RJTZ-254-WS-210, 218; RJTZ-190-(NW|WS)-x; (略)
RJFF-OT-GAIBU-G = (略)
DII-OT-G = DII-EPO-19-112, DII-EPO-19-112, DII-NTP-16-51, DII-NTP-19-51
web-RJFF-OT-WS-G = (略)
webaci-RJFF-OT-WS-G = (略)

## RJFF-Trust
RJFF-NETWORK 10.107.190.0/24
RJFF-254-NW-209 10.107.254.209/32
RJFF-254-NW-217 10.107.254.217/32
RJFF-254-WS-210 10.107.254.210/32
RJFF-254-WS-218 10.107.254.218/32
RJFF-190-(NW|WS)-x 10.107.190.x/32

RJFF-HOST-G = RJFF-190-WS-1, 2
RJFF-NIN-G = RJFF-190-WS-11, 14, 17
RJFF-IN-WS-KYOKUNAI-G = RJFF-190-WS-130 - 138, 148, 149, 60
RJFF-IN-WS-G = (略)

## RJFF-DMZ
RJFF-189-WS-1 10.107.189.1/32
RJFF-189-WS-2 10.107.189.2/32
RJFF-189-NW-11 10.107.189.11/32


## RJFF-Untrust-Trust-137
source-address RJTZ-190-WS-239 = 10.101.190.239 (補助コンソール)
destination-address RJFF-190-NW-238 = 10.107.190.238
destination-address RJFF-190-NW-239
destination-address RJFF-190-NW-237
application P137-APP = junos-ssh, TCP-62001-62003, TCP-62020, TCP-62022, TCP-3389

## RJFF-Untrust-Trust-139
source-address RJTZ-190-WS-142 = 10.101.190.142 (運用諸元評価用端末)
source-address RJTZ-190-WS-143
destination-address RJFF-190-WS-150 = 10.107.190.150 (運用諸元管理装置)
application P139-APP = TCP-1521

## RJFF-Untrust-Trust-132
source-address RJTZ-190-WS-142
source-address RJTZ-190-WS-143
destination-address RJFF-190-WS-3
destination-address RJFF-190-WS-2
destination-address RJFF-190-WS-4
application T-ANY-never

## RJFF-Untrust-Trust-001
source-address RJTZ-190-WS-15
destination-address RJFF-190-WS-15
destination-address RJFF-IN-WS-KYOKUNAI-G
application any

## RJFF-Untrust-Trust-002
source-address RJFF-OT-WS-G
destination-address RJFF-190-WS-15 = 10.107.190.15 (仮想化サーバー２（プログラム等管理サーバー）)
application any

## RJFF-Untrust-Trust-003
source-address RJFF-OT-WS-G
source-address RJFF-IN-GAIBU-G
source-address RJFF-OT-GAIBU-G
destination-address RJFF-IN-WS-G
application PING = junos-icmp-all
application TRACEROUTE = troute = udp 33434-33534

## RJFF-Untrust-Trust-004
source-address RJTZ-181-WS-129, 131
source-address RJFF-181-WS-101, 103
source-address RJFF-233-WS-144, 145
source-address RJTY-233-WS-144, 145
destination-address RJFF-HOST-G
application JWS = TCP-63001
application JWS-debug = TCP-63051

## RJFF-Untrust-Trust-004a
source-address RJTZ-HOST-G
destination-address RJFF-HOST-G
application HOST-HOST = TCP-64300

## RJFF-Untrust-Trust-005
source-address RJNA-190-WS-129 = 10.102.190.129 (遠隔操作卓)
source-address RJTZ-NETWORK
destination-address RJFF-NETWORK
application FTP = TCP-20, junos-ftp

## RJFF-Untrust-Trust-006
source-address RJFF-OT-WS-G
source-address RJTZ-189-WS-1
destination-address RJFF-190-WS-102 = 10.107.190.102 (WEBS（ＤＢ）サーバ)
destination-address RJFF-NIN-G (仮想化サーバー１，２（認証サーバ１，2）)
application DNS = junos-dns-tcp, junos-dns-udp

## RJFF-Untrust-Trust-007
source-address RJFF-OT-WS-G
destination-address RJFF-190-WS-102
destination-address RJFF-NIN-G
application LDAP = junos-ldap

## RJFF-Untrust-Trust-008
source-address RJFF-OT-WS-G
destination-address RJFF-190-WS-102
destination-address RJFF-NIN-G
application LDAPS = TCP-636

## RJFF-Untrust-Trust-008a
source-address RJFF-OT-WS-G
destination-address RJFF-190-WS-102
destination-address RJFF-NIN-G
application KERBEROS = TCP-88, UDP-88
application PING
application DNS
application NTP = junos-ntp
application UDP-135, 137, 138, 389
application TCP-139, 389, 445, 636, 464, 3268, 3269, 9389

## RJFF-Untrust-Trust-008ab
source-address RJFF-OT-WS-G
destination-address RJFF-190-WS-102
destination-address RJFF-NIN-G
application any

## RJFF-Untrust-Trust-009
source-address RJTZ-190-WS-140 - 143 = 10.101.190.140 - 143
source-address RJNA-190-WS-129 = 10.102.190.129 (遠隔操作卓)
destination-address RJFF-190-WS-103 - 113 = 10.107.190.103 - 113 (代替運用等サーバー１，２)
application any

## RJFF-Untrust-Trust-009a
source-address RJTZ-190-WS-140 - 143, 15
destination-address RJFF-190-NW-242 - 245
application SR-KANRI = TCP-999

## RJFF-Untrust-Trust-010
source-address RJFF-OT-WS-G
destination-address RJFF-NETWORK
application MS-SSN = junos-netbios-session
application junos-smb

## RJFF-Untrust-Trust-011
source-address RJFF-OT-WS-G
source-address RJTZ-189-WS-1 = 10.101.189.1 (ＷＥＢＳ（ＡＰ）サーバ)
destination-address RJFF-NETWORK
application MS-DS = junos-netbios-session, TCP-12520

## RJFF-Untrust-Trust-012
source-address RJFF-OT-WS-G
destination-address RJFF-NETWORK
application NBNAME = junos-nbname

## RJFF-Untrust-Trust-013
source-address RJFF-OT-WS-G
destination-address RJFF-NETWORK
application NBDS = junos-nbds

## RJFF-Untrust-Trust-016
source-address RJNA-190-WS-129
source-address RJTZ-NETWORK
destination-address RJFF-NETWORK
application XSTART = TCP-512

## RJFF-Untrust-Trust-017
source-address RJNA-190-WS-129
source-address RJTZ-NETWORK
destination-address RJFF-NETWORK
application EXCEED = TCP-0-65535_6000, UDP-0-65535_6000, UDP-6000-6001, TCP-6000-6001

## RJFF-Untrust-Trust-020 ==deny==
source-address RJTZ-NETWORK
destination-address RJFF-NETWORK
application TELNET = junos-telnet

## RJFF-Untrust-Trust-020g
source-address RJTZ-NETWORK
source-address RJNA-190-WS-129
destination-address RJFF-190-WS-100 - 113
destination-address RJFF-190-NW-254 - 251
match application SSH = junos-ssh
match application HTTPS = junos-https, UDP-443

## RJFF-Untrust-Trust-020a
source-address RJTZ-NIN-G
destination-address RJFF-NIN-G
application RTP = TCP-5002-5005

## RJFF-Untrust-Trust-020b
source-address RJTZ-NIN-G
destination-address RJFF-NIN-G
application EPMAP = junos-ms-rpc-tcp

## RJFF-Untrust-Trust-020c
source-address RJTZ-NIN-G
destination-address RJFF-NIN-G
application DFSR = TCP-5722

## RJFF-Untrust-Trust-020d
source-address RJTZ-NIN-G
destination-address RJFF-NIN-G
application NAMESERVER = TCP-42

## RJFF-Untrust-Trust-020e
source-address RJTZ-NIN-G
destination-address RJFF-IN-WS-G
application DNS-SOURCE = UDP-0-65535_53

## RJFF-Untrust-Trust-023
match source-address RJNA-190-WS-129
match source-address RJTZ-190-WS-140 - 143
destination-address RJFF-190-WS-2
application ATSS = TCP-377-378

## RJFF-Untrust-Trust-024
match source-address RJNA-190-WS-129
match source-address RJTZ-190-WS-140 - 143
destination-address RJFF-190-WS-2
application ROFBR = TCP-8010

## RJFF-Untrust-Trust-026
source-address RJFF-OT-WS-G
destination-address RJFF-190-WS-102
destination-address RJFF-NIN-G
application LDAP-UDP = UDP-389

## RJFF-Untrust-Trust-027
source-address RJTZ-NETWORK
destination-address RJFF-NETWORK
application HTTP = junos-http

## RJFF-Untrust-Trust-029
source-address RJTZ-NETWORK
destination-address RJFF-NETWORK
application RemoteDeskTop = TCP-3389

## RJFF-Untrust-Trust-029a
source-address RJTZ-HOST-G
destination-address RJFF-190-WS-100 - 113
application HOST-OPS = TCP-64208

## RJFF-Untrust-Trust-029b
source-address RJTZ-HOST-G
destination-address RJFF-190-WS-130, 137, 138
match application WS-YFYX = TCP-5310

## RJFF-Untrust-Trust-029bc
source-address RJTZ-HOST-G
destination-address RJFF-190-WS-137, 138, 148, 149, 20
application any

## RJFF-Untrust-Trust-030
source-address RJTZ-190-WS-20 = 10.101.190.20 (電算機ＷＳ)
destination-address RJFF-190-WS-20
application any

## RJFF-Untrust-Trust-021
source-address RJTZ-NIN-G
destination-address RJFF-NIN-G
destination-address RJFF-IN-WS-KYOKUNAI-G
application TCP-ANY

## RJFF-Untrust-Trust-022
source-address RJTZ-190-WS-11
destination-address RJFF-NIN-G
application UDP-ANY

## RJFF-Untrust-Trust-031 ==deny==
source-address any
destination-address any
application deny2967

## RJFF-Untrust-Trust-032
source-address RJTZ-189-WS-1
destination-address RJFF-190-WS-102
application LISTENER = TCP-57340

## RJFF-Untrust-Trust-109
source-address RJFF-OT-WS-G
destination-address RJFF-190-WS-15
application any

## RJFF-Untrust-Trust-110
source-address RJFF-OT-WS-G
destination-address RJFF-190-WS-15
application P110-APP = TCP-10080, TCP-8530, TCP-8531

## RJFF-Untrust-Trust-111
source-address RJTZ-190-WS-100, 101, 110, 111 (業務処理用サーバ１，２、ノータム処理装置)
destination-address RJFF-190-WS-100 - 113
application P111-APP = TCP-20, junos-ftp, junos-ssh, junos-rsh

## RJff-Untrust-Trust-112
source-address RJTZ-190-WS-100, 101, 142, 143, 140, 141 (運用諸元評価用端末１，２、連接試験用端末A, B)
destination-address RJFF-190-WS-121, 122 = 10.107.190.121, 122 (ＡＴＳＤＢ１，２系)
application P112-APP = TCP-20, junos-ftp, junos-ssh

## RJFF-Untrust-Trust-113
source-address RJTZ-190-WS-142, 143
destination-address RJFF-190-WS-103 - 113
application P113-APP = TCP-5600, TCP-6000-6099

## RJFF-Untrust-Trust-114
source-address RJNA-190-WS-129
destination-address RJFF-190-WS-106
application P114-APP = TCP-5600, TCP-6000-6099

## RJFF-Untrust-Trust-117
source-address RJTZ-190-WS-21, 22
destination-address RJFF-190-WS-120, 121, 122
application P117-APP = TCP-29003, UDP-29003

## RJFF-Untrust-Trust-118
source-address RJTZ-190-WS-21, 22  = 10.101.190.21, 22 (サーバー管理コンソール１，２)
destination-address RJFF-190-WS-123 = 10.107.190.123 (iStorage)
application P118-APP = HTTP

## RJFF-Untrust-Trust-131
source-address RJFF-OT-WS-G
destination-address RJFF-190-WS-121, 122
application P131-APP = TCP-1521

## RJFF-Untrust-Trust-133
source-address RJFF-OT-GAIBU-G
match destination-address RJFF-190-WS-148, 149
application any

## RJFF-Untrust-Trust-134
source-address RJTZ-190-WS-120, 121, 122
destination-address RJFF-190-WS-21, 22
application P134-APP = TCP-29010, UDP-29010

## RJFF-Untrust-Trust-138
source-address RJTZ-190-WS-142, 143, 140, 141
destination-address RJFF-190-WS-21, 22 = 10.107.190.21, 22 (サーバー管理コンソール１，２)
application P138-APP = TCP-3389

## RJFF-Untrust-Trust-140
source-address RJFF-OT-WS-G
destination-address RJFF-190-WS-200, 210 = 10.107.190.200, 210 (Oracle Database)
application P140-APP = TCP-1521

## RJFF-Untrust-Trust-141
source-address RJFF-NETWORK_8
source-address RJTZ-NETWORK_8
destination-address any
application TCP-ANY
application UDP-ANY
application PING

## RJFF-Untrust-Trust-142
source-address RJTZ-190-WS-21, 22, 142, 143, 140, 141, 136 = 10.101.190.136 (ＦＳ２)
destination-address any
application any

## RJFF-Untrust-Trust-143
source-address RJTZ-190-WS-6 - 8 (システム監視装置Ａ)
destination-address RJFF-190-WS-6 (システム監視装置Ｂ（SV）)
application any

## RJFF-Untrust-Trust-992
source-address DII-WSUS-16-61
source-address DII-WSUS-19-61
destination-address RJFF-190-WS-15
application any

## RJFF-Untrust-Trust-993
source-address DII-OT-G
destination-address RJFF-IN-WS-G
application PING
application TCP-8081-8083
application NTP

## RJFF-Untrust-Trust-995
source-address RJTA-164-WS-100
source-address RJNA-190-WS-160
destination-address RJFF-190-WS-6
application TCP-12080
application TCP-22533
application TCP-12443

## RJFF-Untrust-Trust-997
source-address RJTZ-190-WS-100, 101
destination-address RJFF-190-WS-137, 138, 148, 149
application any

## RJFF-Untrust-Trust-999 ==deny==
source-address any
destination-address any
application any

## RJFF-Untrust-Trust-998
source-address any
destination-address RJFF-190-WS-15
application any


## RJFF-Untrust-DMZ-002
source-address web-RJFF-OT-WS-G
source-address RJFF-OT-WS-G
destination-address RJFF-189-WS-1
application HTTP

## RJFF-Untrust-DMZ-003
source-address web-RJFF-OT-WS-G
source-address RJFF-OT-WS-G
destination-address RJFF-189-WS-1
application HTTPS

## RJFF-Untrust-DMZ-001a
source-address webaci-RJFF-OT-WS-G
destination-address RJFF-189-WS-1
application HTTPS
application FTP
application HTTP

## RJFF-Untrust-DMZ-004
source-address any
destination-address RJFF-189-WS-1
destination-address RJFF-189-NW-11
application PING

## RJFF-Untrust-DMZ-005
source-address RJTZ-NETWORK
source-address RJTZ-189-WS-1
destination-address RJFF-189-WS-1
application SSH

## RJFF-Untrust-DMZ-006
source-address RJTZ-189-WS-1
source-address web-RJFF-OT-WS-G
source-address RJFF-OT-WS-G
destination-address RJFF-189-WS-1
application FTP

## RJFF-Untrust-DMZ-007
source-address RJTZ-NETWORK
destination-address RJFF-189-WS-1
application FADPWEB = TCP-64208

## RJFF-Untrust-DMZ-014 ==deny==
source-address RJTZ-190-WS-100, 101
destination-address RJFF-189-WS-2
application SMTP = junos-smtp, UDP-25

## RJFF-Untrust-DMZ-015 ==deny==
source-address RJTZ-190-WS-100, 101
destination-address RJFF-189-WS-2
application POP3 = junos-pop3

## RJFF-Untrust-DMZ-016
source-address RJTZ-190-WS-110, 111
destination-address RJFF-189-WS-1
application TCP-ANY

## RJFF-Untrust-DMZ-999 ==deny==
source-address any
destination-address any
application any

## RJFF-Trust-Untrust-RJFF-A
source-address RJFF-190-WS-20
destination-address RJNA-190-WS-129
destination-address RJTZ-NETWORK
application FTP

## RJFF-Trust-Untrust-RJFF-B
source-address RJFF-IN-WS-KYOKUNAI-G
destination-address RJTZ-IN-WS-KYOKUNAI-G
application FTP

## RJFF-Trust-Untrust-ANY
source-address any
destination-address any
match application any

## RJFF-Trust-DMZ-001
source-address RJFF-NETWORK
destination-address RJFF-189-WS-1
application any

## RJFF-Trust-DMZ-014 ==deny==
source-address RJFF-190-WS-100 - 113
destination-address RJFF-189-WS-2
match application SMTP

## RJFF-Trust-DMZ-015 ==deny==
source-address RJFF-190-WS-100 - 113
destination-address RJFF-189-WS-2
match application POP3

## RJFF-Trust-DMZ-ANY
source-address any
destination-address any
application any

## RJFF-DMZ-Untrust-ANY
source-address any
destination-address any
application any

## RJFF-DMZ-Trust-205
source-address RJFF-189-WS-1
destination-address RJFF-190-WS-102
application TCP-57340

## RJFF-DMZ-Trust-201
source-address any
destination-address any
application PING
application TCP-636
application junos-dns-tcp
application junos-dns-udp
application junos-ntp
application TCP-57340
application TCP-88
application junos-rsh

## RJFF-DMZ-Trust-202
source-address any
destination-address RJFF-190-WS-102 = 10.107.190.102 (WEBS（ＤＢ）サーバ)
application junos-ssh
application TCP-20
application junos-ftp

## RJFF-DMZ-Trust-203
source-address RJFF-189-WS-1
destination-address any
application junos-smb
application TCP-12520

## RJFF-DMZ-Trust-204
source-address RJFF-189-WS-1
destination-address RJFF-190-WS-13, 21, 22 (仮想化サーバー２（計算機）、サーバー管理コンソール１，２)
application P204-APP = junos-smb
application SSH
application PING

## RJFF-DMZ-Trust-207
source-address RJFF-189-WS-1
destination-address RJFF-190-WS-11, 14 (仮想化サーバー１，２（認証サーバ１，２）)
application any

## RJFF-DMZ-Trust-210
source-address RJFF-189-WS-1
destination-address RJFF-190-WS-6
application TCP-12080
application TCP-22533
application TCP-12443























































































