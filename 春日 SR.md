## JADGE-SR
System Version: SC-8259  79HAUE Ver.H Tue Jan 14 16:15:48 JST 2020

hostname adm
route 0.0.0.0/0 10.107.191.254

acc telnet 0.0.0.0/0
acc ssh 0.0.0.0/0

interface ethernet 0
 ip address 10.107.191.1/24
 interface ethernet 1
 speed auto

custom
 convert enable
 x25 bltimer 120000
 rcvbuf 10240
 rcvlen 8000
 ust_host 10.107.191.2:999
 ust_lport 887
 hdlc fault_code S2
 hdlc bltimer 30000
 host_code jis8

interface serial 1
 bsc healthtimer 30000
 code jis8
 port 64206
 dte_reset enable
 open_reset disable
 x25 da disable
 x25 sa disable
 hdlc healthtimer 40000


## 移動1-SR
System Version: SC-8259  79HAUE Ver.H Tue Jan 14 16:15:48 JST 2020

hostname adm
route 0.0.0.0/0 10.107.190.254

acc telnet 0.0.0.0/0
acc ssh 0.0.0.0/0

interface ethernet 0
 ip address 10.107.190.242/24

interface ethernet 1
 speed auto

custom
 convert enable
 x25 bltimer 120000
 rcvbuf 10240
 rcvlen 8000
 ust_host 10.107.190.243:999
 ust_lport 887
 hdlc fault_code S2
 hdlc bltimer 30000
 host_code jis8

interface serial 1
 bsc healthtimer 30000
 code jis8
 port 64206
 dte_reset enable
 open_reset disable
 x25 da disable
 x25 sa disable
 hdlc healthtimer 40000


## 移動2-SR
System Version: SC-8259  79HAUE Ver.H Tue Jan 14 16:15:48 JST 2020

hostname adm
route 0.0.0.0/0 10.107.190.254

acc telnet 0.0.0.0/0
acc ssh 0.0.0.0/0

interface ethernet 0
 ip address 10.107.190.244/24

interface ethernet 1
 speed auto

custom
 convert enable
 x25 bltimer 120000
 rcvbuf 10240
 rcvlen 8000
 ust_host 10.107.190.245:999
 ust_lport 887
 hdlc fault_code S2
 hdlc bltimer 30000
 host_code jis8

interface serial 1
 bsc healthtimer 30000
 code jis8
 port 64206
 dte_reset enable
 open_reset disable
 x25 da disable
 x25 sa disable
 hdlc healthtimer 40000












