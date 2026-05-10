# Challenge 16 : Version Detection

### Objective :
- To identify service versions running on the target machine using Nmap version detection.

### Target Information :

| Item | Value |
|---|---|
| Target IP | 192.168.83.129 |


### Tool Used :
- Nmap

### Step :

1.Identify Target IP Address

Command : (Run inside Metasploitable 2)
```
ip a
```
Result:
<img width="749" height="238" alt="Screenshot 2026-05-10 151320" src="https://github.com/user-attachments/assets/5db1f9eb-712b-4ec9-9a1d-c4e7cfb12eea" />
<br>

---
2. Run Version Detection Scan

Command :
```
nmap -sV 192.168.83.129
```
Result Summary :
<img width="627" height="456" alt="Screenshot 2026-05-10 155753" src="https://github.com/user-attachments/assets/6016877e-c702-47c3-a7e2-7b843eb66c40" />

<br>

| Port | Service | Version |
|---|---|---|
| 21 | FTP | vsFTPd 2.3.4 |
| 22 | SSH | OpenSSH 4.7p1 Debian |
| 25 | SMTP | Postfix smtpd |
| 80 | HTTP | Apache httpd 2.2.8 |
| 445 | SMB | Samba 3.0.20-Debian |
| 3306 | MySQL | MySQL 5.0.51a |

Findings :
- Multiple services and software versions were successfully identified on the target machine.
- Several detected versions appear outdated.

---
### Conclusion
- Nmap version detection successfully identified several active services and their corresponding software versions on the target machine.
