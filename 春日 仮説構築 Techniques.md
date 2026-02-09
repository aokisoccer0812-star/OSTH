
| アクター                         | APT41                                                                                                                                                                                                                                                                              | BlackTech                                   | Salt Typhoon                 |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------- | ---------------------------- |
| **別名**                       | Wicked Panda<br>Blass Typhoon<br>BARIUM                                                                                                                                                                                                                                            | Palmerworm                                  |                              |
| **母体**                       | 中国政府                                                                                                                                                                                                                                                                               | 中国語圏                                        | 中国国家支援                       |
| **目的**                       | サイバースパイ、金銭                                                                                                                                                                                                                                                                         | サイバースパイ                                     | サイバースパイ                      |
| **標的**                       | 世界各国                                                                                                                                                                                                                                                                               | 台湾、日本、米国等                                   | 米国、世界各国                      |
| **対象**                       | 医療、通信、技術、金融、教育等                                                                                                                                                                                                                                                                    | メディア、建設、エンジニアリング、電気、金融等                     | 通信、防衛、政府、交通、重要インフラ           |
| **Reconnaissance**           | T1595.002, T1595.003, ~~T1596.005, T1593.002, T1594~~                                                                                                                                                                                                                              |                                             | T1590.004                    |
| ~~**Resource Development**~~ | ~~T1583.007, T1586.003, ==T1588.003==, ==T1588.002==~~                                                                                                                                                                                                                             | ~~==T1588.003==, T1588.004, ==T1588.002==~~ | ~~T1587.001, ==T1588.002==~~ |
| **Initial Access**           | ==T1190==, ~~T1133~~, ~~==T1566.001==~~, T1195.002, T1078                                                                                                                                                                                                                          | ==T1190==, ~~==T1566.001==, T1566.002~~     | ==T1190==                    |
| **Execution**                | T1059.007, T1059.001, T1059.004, T1059.003, ==T1203==, T1053.005, T1569.002, T1047                                                                                                                                                                                                 | ==T1203==, T1106, ~~T1204.002, T1204.001~~  |                              |
| **Persistence**              | T1098.007, T1197, ==T1547.001==, T1037, T1036.001, T1543.003, ~~T1546.008~~, ~~T1133~~, T1574.001, T1574.006, T1112, T1542.003, T1053.005, T1505.003, T1078                                                                                                                        | ==T1574.001==                               | T1098.004, T1136             |
| **Privilege Escalation**     | T1134, T1098.007, ==T1547.001==, T1037, T1543.003, T1484.001, ~~T1546.008~~, T1574, T1574.001, T1574.006, T1055, T1053.005, T1078                                                                                                                                                  | ==T1574.001==                               | T1098.004                    |
| **Defense Evasion**          | T1134, T1197, T1140, T1484.001, T1480.001, T1574, ==T1574.001==, T1574.006, T1562.006, ~~T1656~~, T1070.003, T1070.001, T1070.004, T1036.004, T1036.005, T1112, T1599, T1027, T1027.013, T1027.002, T1542.003, T1055, T1014, T1553.002, T1218.001, T1218.011, ~~T1550.002~~, T1078 | ==T1574.001==, ~~T1036.002~~                | T1562.004, T1070.002         |
| **Credential Access**        | T1110, T1555, T1555.003, T1056.001, T1003.001, T1003.003, T1003.002                                                                                                                                                                                                                |                                             | T1110.002, T1040             |
| **Discovery**                | T1087.002, T1087.001, ~~T1083~~, ~~T1680~~, ==T1046==, T1135, T1069, T1012, ~~T1018~~, T1082, T1016, T1049, T1033                                                                                                                                                                  | ==T1046==                                   | T1040                        |
| **Lateral Movement**         | ~~T1570~~, T1021.001, T1021.002, T1550.002                                                                                                                                                                                                                                         | ==T1021.004==                               | ==T1021.004==                |
| **Collection**               | ~~T1560.003~~, T1560.001, T1119, ~~T1213.003~~, T1213.006, T1005, T1074.001, T1056.001                                                                                                                                                                                             |                                             | T1602.002                    |
| **Command and Control**      | T1071.004, T1071.002, T1071.001, ~~T1001.003~~, ~~T1568.002~~, T1573.002, ~~T1008~~, T1105, T1104, T1090, T1102, ~~T1102.001~~                                                                                                                                                     |                                             | T1572                        |
| **Exfiltration**             | T1030, ==T1048.003==,  T1041, T1567, T1567.002                                                                                                                                                                                                                                     |                                             | ==T1048.003==                |
| **Impact**                   | T1486, ~~T1496.001~~                                                                                                                                                                                                                                                               |                                             |                              |

# Reconnaisance
### T1595.002: Active Scanning: Vulnerability Scanning
APT41 used vulnerability scanner. 
### T1595.003: Active Scanning: Wordlist Scanning
APT41 brute-forces directories on web servers.
### T1590.004: Network Topology
Salt Typhoon has use configuration files from exploited network.

# Initial Access
### T1190: Exploit Public-Facing Application
APT41 exploited vulnerabilities to gain initial access.
BlackTeck has exploited a buffer overflow vulnerability in Microsoft IIS.
Salt Typhoon has exploited in Cisco software.
### T1195.002: Supply Chain Compromise: Compromise Software Supply Chain
APT41 gained access to where injected malicious code.
### T1078: Valid Accounts
APT41 used compromised credentials.

# Execution
### T1059.007: Command and Scripting Interpreter: JavaScript
APT41 deployed JScript web shells.
### T1059.001: Command and Scripting Interpreter: PowerShell
APT41 leveraged PowerShell to deploy malware families.
### T1059.004: Command and Scripting Interpreter: Unix Shell
APT41 used Linux shell commands.
### T1059.003: Windows Command Shell
APT41 used `cmd.exe /c` and a batch file.
### T1203: Exploitation for Client Execution
APT41 leveraged exploits.
BlackTech has exploited multiple vulnerabilities.
### T1053.005: Scheduled Task/Job: Scheduled Task
APT41 used scheduled tasks.
### T1569.002: System Services: Service Execution
APT41 used svchost.exe and net to execute services.
### T1106: Native API
BlackTech has used built-in API functions.
### T1047: Windows Management Instrumentation
APT41 uses WMI in several ways.

# Persistence
### T1098.007: Account Manipulation: Additional Local or Domain Groups
APT41 has added user accounts to User and Admin groups.
### T1098.004: Account Manipulation: SSH Authorized Keys
Salt Typhoon has added SSH authorized_keys.
### T1197: BITS Jobs
APT41 used BITSAdmin to download and install payloads.
### T1547.001: Boot or Logon Autostart Execution: Registry Run Keys / Startup Folder
APT41 created startup files and added registry key for persistence.
### T1037: Boot or Logon Initialization Scripts
APT41 used a hidden shell script `/etc/rc.d/init.d` to leverage backdoor and rootkit.
### T1136: Create Account
Salt Typhoon has created users on compromised network devices.
### T1136.001: Create Account: Local Account
APT41 has created user accounts.
### T1543.003: Create or Modify System Process: Windows Service
APT41 modified legitmate Windows services and created a new service.
### T1574.001: Hijack Execution Flow: DLL
APT41 has used search order hijacking and DLL side-loading.
BlackTech has used DLL side loading.
### T1574.006: Hijack Execution Flow: Dynamic Linker Hijacking
APT41 has configured payloads to load via LD_PRELOAD.
### T1112: Modify Registory
APT41 used a malware variant called GOODLUCK to steal credentials.
### T1542.003: Pre-OS Boot: Bootkit
APT41 deployed MBR bootkits.
### T1053.005
### T1505.003: Server Software Component: Web Shell
APT41 used web shells for persistence.
### T1078

# Privilege Escalation
### T1134: Access Token Manipulation
APT41 used a ConfuserEX obfuscated BADPOTATO exploit to abuse named-pipe impersonation for local `NT AUTHORITY\SYSTEM` privilege escalation.
### T1098.007
### T1098.004
### T1547.001
### T1037
### T1543.003
### T1484.001: Domain or Tenant Policy Modification: Group Policy Modification
APT41 used scheduled tasks created via GPOs.
### T1574.001
### T1574.006
### T1053.005
### T1078

# Defense Evasion
### T1134
### T1197
### T1140: Deobfuscate/Decode Files or Information
APT41 used the DUSTPAN loader to decrypt embeded payloads.
### T1480.001: Environmental Keying
APT41 has encrypted payloads using DPAPI and volume serial number.
### T1574.001
### T1574.006
### T1562.004: Impair Defences: Disable or Modify System Firewall
Salt Typhoon has made changes to ACL and loopback address.
### T1562.006: Impair Defences: Indicator Blocking
APT41 developed a custom injector that enables ETW bypass.
### T1070.003: Indicator Removal: Clear Command History
APT41 deleted bash histories.
### T1070.002: Indicator Removal: Clear Linux or Mac System Logs
Salt Typhoon has cleared logs.
### T1070.001: Clear Windows Event Logs
APT41 cleared Windows security and system events.
### T1070.004: File Deletion
APT41 deleted files.
### T1036.004: Masquerading: Masquerade Task or Service
APT41
### T1036.005: Masquerading: Match Legitimate Resource Name or Location
APT41
### T1112
### T1599: Network Boundary Bridging
APT41 used `NATBypass` to access via RDP.
### T1027: Obfuscated Files or Information
APT41
### T1027.013: Obfuscated Files or Information: Encrypted/Encoded File
APT41
### T1027.002: Obfuscated Files or Information: Software Packing
APT41
### T1542.003
### T1055: Process Injection
APT41 malware TIDYELF loaded the main WINTERLOVE component by injecting.
### T1014: Rootkit
APT41 developed rootkits on Linux systems.
### T1553.002: Subvert Trust Controls: Code Signing
APT41
### T1218.001: System Binary Proxy Execution: Compiled HTML File
APT41 used .chm files for targeting.
### T1218.011: System Binary Proxy Execution: Rundll32
APT41 has used rundll32.exe to execute a loader.
### T1078

# Credential Access
### T1110: Brute Force
APT41 performed password brute-force attacks on the local admin account.
### T1110.002: Brute Force: Password Cracking
Salt Tyhoon has cracked passwords.
### T1555: Credentials from Password Stores
APT41 has obtained information from databases.
### T1555.003: Credentials from Password Stores: Credentials from Web Browsers
APT41 used BrowserGhost to obtain credentials from browsers.
### T1056.001: Keylogging
APT41 used a keylogger called GEARSHIFT.
### T1040: Network Sniffing
Salt Typhhon has captured packet data.
### T1003.001: OS Credential Dumping: LSASS Memory
APT41 has used hashdump, Mimi_katz, Procdump to dump password hashes from memory.
### T1003.003: OS Credential Dumping: NTDS
APT41 used ntdsutil to copy `ntds.dit` file.
### T1003.002: OS Credential Dumping: Security Account Manager
APT41 extracted user account data from SAM by using `reg save` or exploiting volume shadow copy.

# Discovery
### T1087.002: Account Discovery: Domain Account
APT41 used `net` to enumerate local administrator groups.
### T1087.001: Account Discovery: Local Account
APT41 used `net` to enumerate domain administrator users.
### T1046: Network Service Discovery
APT41 used a malware variant called WIDETONE to conduct port scans.
BlackTech has used the SNScan tool.
### T1135: Network Share Discovery
APT41 used `net share` command.
### T1040
### T1069: Permission Groups Discovery
APT41 used `net group` commands.
### T1012: Query Registry
APT41 queried registry values to determine such as RDP ports.
### T1082: System Information Discovery
APT41 uses such as `systeminfo` and `net config Workstation` to enumerate.
### T1016: System Network Configuration Discovery
APT41 collected MAC addresses.
### T1049: System Network Connections Discovery
APT41 has enumerated IP addresses, used `netstat` command, and used a malware variant HIGHNOON to enumerate active RDP sessions.
### T1033: System Owner/User Discovery
APT41 has executed `whoami` command, including using the WMIEXEC utility.

# Lateral Movement
### T1021.001: Remote Services: Remote Desktop Protocol
APT41 used NATBypass to expose local RDP ports.
### T1021.002: Remote Services: SMB/Windows Admin Shares
APT41 has transfered implant files using Windows Admin Shares and SMB protocol, then executes files through WMI.
### T1021.004: Remote Services: SSH
BlackTech has used Putty.
Salt Typhoon has used modified loopback address with SSH connections to bypass ACLs.
### T1550.002: Use Alternate Authentication Material: Pass the Hash
APT41 uses tools such as Mimi-katz.

# Collection
### T1560.001: Archive Collected Data: Archive via Utility
APT41 created a RAR archive and used makecab.exe to both download and archive.
### T1119: Automated Collection
APT41 used tools such as SQLULDR2 and PINEGAROVE.
### T1602.002: Data from Configuration Repository: Network Device Configuration Dump
Salt Typhoon has acquired credentials.
### T1213.006: Data from Information Repositories: Databases
APT41 collected data from Oracle databases using SQLULDR2.
### T1005: Data from Local System
APT41 has uploaded files and data.
### T1074.001: Data Staged: Local Data Staging
APT41
### T1056.001

# Command and Control
### T1071.004: Application Layer Protocol: DNS
APT41 used DNS for C2 communication.
### T1071.002: Application Layer Protocol: File Transfer Protocols
APT41 used exploit payloads via ftp.
### T1071.001: Application Layer Protocol: Web Protocols
APT41 used HTTP to download payloads and HTTPS for command and control.
### T1573.002: Encrypted Channel: Asymmetric Cryptography
APT41 used HTTPS for command and control.
### T1105: Ingress Tool Transfer
APT41 used certutil to download additional files.
### T1104: Multi-Stage Channels
APT41 used storescyncsvc.dll BEACON backdoor to download a secondary backdoor.
### T1572: Protocol Tunneling
Salt Typhoon has created GRE tunnels.
### T1090: Proxy
APT41 used a tool called CLASSFON to covertly proxy network communications and Cloudflare CDN to proxy C2 network.


# Exfiltration
### T1030: Data Transfer Size Limits
APT41
### T1048.003: Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted Non-C2 Protocol
APT41 exfiltrated victim data via DNS lookups.
Salt Typhoon has exfiltrated configuration files over FTP and TFTP.
### T1041: Exfiltration Over C2 Channel
APT41 used its Cloudflare services C2 channels for data exfiltration.
### T1567.002: Exfiltration Over Web Service: Exfiltration to Cloud Storage
APT41 exfiltrated to OneDrive,

# Impact
### T1486: Data Encrypted for Impact
APT41 used a ransomware called Encryptor RaaS, Microsoft Bitlocker and Jetico's BestCrypt.