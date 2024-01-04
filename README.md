# Django CTF
![](https://raw.githubusercontent.com/Adel-Ahmed777/TryHackMe-Writeups/main/TryHackMe%20Images/Django%20CTF-image.png)
## Unit-5 CTF.

### Information to start with:
> Username: django-admin  

> Password: roottoor1212  

## Nmap Scan
> Results:

```
Nmap scan report for 10.10.172.150
Host is up (0.31s latency).
Not shown: 998 closed tcp ports (reset)
PORT     STATE SERVICE  VERSION
22/tcp   open  ssh      OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey:
|   2048 35:30:91:45:b9:d1:ed:5a:13:42:3e:20:95:6d:c7:b7 (RSA)
|   256 f5:69:6a:7b:c8:ac:89:b5:38:93:50:2f:05:24:22:70 (ECDSA)
|_  256 8f:4d:37:ba:40:12:05:fa:f0:e6:d6:82:fb:65:52:e8 (ED25519)
8000/tcp open  http-alt WSGIServer/0.2 CPython/3.6.9
|_http-title: DisallowedHost          at /
|_http-server-header: WSGIServer/0.2 CPython/3.6.9
| fingerprint-strings:
|   FourOhFourRequest:
|     HTTP/1.1 400 Bad Request
|     Date: Tue, 01 Feb 2022 08:07:07 GMT
|     Server: WSGIServer/0.2 CPython/3.6.9
|     Content-Type: text/html
|     Connection: close
|     <!DOCTYPE html>
|     <html lang="en">
|     <head>
|     <meta http-equiv="content-type" content="text/html; charset=utf-8">
|     <meta name="robots" content="NONE,NOARCHIVE">
|     <title>DisallowedHost
|     /nice ports,/Trinity.txt.bak</title>
|     <style type="text/css">
|     html * { padding:0; margin:0; }
|     body * { padding:10px 20px; }
|     body * * { padding:0; }
|     body { font:small sans-serif; background-color:#fff; color:#000; }
|     body>div { border-bottom:1px solid #ddd; }
|     font-weight:normal; }
|     margin-bottom:.8em; }
|     margin:1em 0 .5em 0; }
|     margin:0 0 .5em 0; font-weight: normal; }
|     code, pre { font-size: 100%; white-space: pre-wrap; }
|     table { border:1px solid #ccc; border-collapse: collapse; width:100%; ba
|   GetRequest:
|     HTTP/1.1 400 Bad Request
|     Date: Tue, 01 Feb 2022 08:07:01 GMT
|     Server: WSGIServer/0.2 CPython/3.6.9
|     Content-Type: text/html
|     Connection: close
|     <!DOCTYPE html>
|     <html lang="en">
|     <head>
|     <meta http-equiv="content-type" content="text/html; charset=utf-8">
|     <meta name="robots" content="NONE,NOARCHIVE">
|     <title>DisallowedHost
|     /</title>
|     <style type="text/css">
|     html * { padding:0; margin:0; }
|     body * { padding:10px 20px; }
|     body * * { padding:0; }
|     body { font:small sans-serif; background-color:#fff; color:#000; }
|     body>div { border-bottom:1px solid #ddd; }
|     font-weight:normal; }
|     margin-bottom:.8em; }
|     margin:1em 0 .5em 0; }
|     margin:0 0 .5em 0; font-weight: normal; }
|     code, pre { font-size: 100%; white-space: pre-wrap; }
|     table { border:1px solid #ccc; border-collapse: collapse; width:100%; background:white; }
|_    tbody
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port8000-TCP:V=7.92%I=7%D=2/1%Time=61F8EA25%P=x86_64-pc-linux-gnu%r(Get
SF:Request,2CDB,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nDate:\x20Tue,\x2001
SF:\x20Feb\x202022\x2008:07:01\x20GMT\r\nServer:\x20WSGIServer/0\.2\x20CPy
SF:thon/3\.6\.9\r\nContent-Type:\x20text/html\r\nConnection:\x20close\r\n\
SF:r\n<!DOCTYPE\x20html>\n<html\x20lang=\"en\">\n<head>\n\x20\x20<meta\x20
SF:http-equiv=\"content-type\"\x20content=\"text/html;\x20charset=utf-8\">
SF:\n\x20\x20<meta\x20name=\"robots\"\x20content=\"NONE,NOARCHIVE\">\n\x20
SF:\x20<title>DisallowedHost\n\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20at\x
SF:20/</title>\n\x20\x20<style\x20type=\"text/css\">\n\x20\x20\x20\x20html
SF:\x20\*\x20{\x20padding:0;\x20margin:0;\x20}\n\x20\x20\x20\x20body\x20\*
SF:\x20{\x20padding:10px\x2020px;\x20}\n\x20\x20\x20\x20body\x20\*\x20\*\x
SF:20{\x20padding:0;\x20}\n\x20\x20\x20\x20body\x20{\x20font:small\x20sans
SF:-serif;\x20background-color:#fff;\x20color:#000;\x20}\n\x20\x20\x20\x20
SF:body>div\x20{\x20border-bottom:1px\x20solid\x20#ddd;\x20}\n\x20\x20\x20
SF:\x20h1\x20{\x20font-weight:normal;\x20}\n\x20\x20\x20\x20h2\x20{\x20mar
SF:gin-bottom:\.8em;\x20}\n\x20\x20\x20\x20h3\x20{\x20margin:1em\x200\x20\
SF:.5em\x200;\x20}\n\x20\x20\x20\x20h4\x20{\x20margin:0\x200\x20\.5em\x200
SF:;\x20font-weight:\x20normal;\x20}\n\x20\x20\x20\x20code,\x20pre\x20{\x2
SF:0font-size:\x20100%;\x20white-space:\x20pre-wrap;\x20}\n\x20\x20\x20\x2
SF:0table\x20{\x20border:1px\x20solid\x20#ccc;\x20border-collapse:\x20coll
SF:apse;\x20width:100%;\x20background:white;\x20}\n\x20\x20\x20\x20tbody")
SF:%r(FourOhFourRequest,2CDB,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nDate:\
SF:x20Tue,\x2001\x20Feb\x202022\x2008:07:07\x20GMT\r\nServer:\x20WSGIServe
SF:r/0\.2\x20CPython/3\.6\.9\r\nContent-Type:\x20text/html\r\nConnection:\
SF:x20close\r\n\r\n<!DOCTYPE\x20html>\n<html\x20lang=\"en\">\n<head>\n\x20
SF:\x20<meta\x20http-equiv=\"content-type\"\x20content=\"text/html;\x20cha
SF:rset=utf-8\">\n\x20\x20<meta\x20name=\"robots\"\x20content=\"NONE,NOARC
SF:HIVE\">\n\x20\x20<title>DisallowedHost\n\x20\x20\x20\x20\x20\x20\x20\x2
SF:0\x20\x20at\x20/nice\x20ports,/Trinity\.txt\.bak</title>\n\x20\x20<styl
SF:e\x20type=\"text/css\">\n\x20\x20\x20\x20html\x20\*\x20{\x20padding:0;\
SF:x20margin:0;\x20}\n\x20\x20\x20\x20body\x20\*\x20{\x20padding:10px\x202
SF:0px;\x20}\n\x20\x20\x20\x20body\x20\*\x20\*\x20{\x20padding:0;\x20}\n\x
SF:20\x20\x20\x20body\x20{\x20font:small\x20sans-serif;\x20background-colo
SF:r:#fff;\x20color:#000;\x20}\n\x20\x20\x20\x20body>div\x20{\x20border-bo
SF:ttom:1px\x20solid\x20#ddd;\x20}\n\x20\x20\x20\x20h1\x20{\x20font-weight
SF::normal;\x20}\n\x20\x20\x20\x20h2\x20{\x20margin-bottom:\.8em;\x20}\n\x
SF:20\x20\x20\x20h3\x20{\x20margin:1em\x200\x20\.5em\x200;\x20}\n\x20\x20\
SF:x20\x20h4\x20{\x20margin:0\x200\x20\.5em\x200;\x20font-weight:\x20norma
SF:l;\x20}\n\x20\x20\x20\x20code,\x20pre\x20{\x20font-size:\x20100%;\x20wh
SF:ite-space:\x20pre-wrap;\x20}\n\x20\x20\x20\x20table\x20{\x20border:1px\
SF:x20solid\x20#ccc;\x20border-collapse:\x20collapse;\x20width:100%;\x20ba
SF:");
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 128.68 seconds
```
> ssh port is open. We already have credentials. So I logged in.

> port 8000 is also open so, I will login through the url. The website is not working.

> Through the ssh port, I will add the machine IP into the seetings.py file so I can load the website.

> success. I am able to log into the admin page.

![](https://raw.githubusercontent.com/Adel-Ahmed777/TryHackMe-Writeups/main/TryHackMe%20Images/Djano-admin-page.png)

> I tried the credentials provided, but they didn't work.

> I have to create a superuser and add new credentials. I used them to access through the admin page.

> Success. I am in and the first flag is retrieved.

![](https://raw.githubusercontent.com/Adel-Ahmed777/TryHackMe-Writeups/main/TryHackMe%20Images/2-Django-admin-page.png)

> the users page has login credentials for another user with a password hash. https://crackstation.net/ will help crack it.

> success. I can now change to the new user. I found the second user flag under the home directory of this user.

> I don't know where is the hidden flag. So I will use grep to find it

```
grep -r 'THM'
```

> I couldn't find any thing within this user. May be it is in the first user.

> Success. The flag is within the files of the django-admin user.
