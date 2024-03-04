# Lab 2 NSP

## Second: Scan a live machine either scanme.nmap.org or always.snwb.howest.be

### What ports are open?

Here is the result scan of open ports on the always.snwb.howest.be
![alt text](image.png)

Here is the result scan of open ports on the scanme.nmap.org
![alt text](image-1.png)

* Connecting to the VPN, and then get the ip address:
    * ip a

    ![alt text](image-2.png)

* Find the DNS Server:
    * dig always.snwb.howest.be
    * nslookup 10.11.12.6

    ![alt text](image-3.png)

    amplifier.vault.vinyl.

* Find number of Live addresses

    * ip a

    We get our subnet mask 

    ![alt text](image-4.png)

    * ipcalc 10.11.12.24/23

    We get the minimum one

    * sudo nmap -sn 10.11.12.1-100

    Then we get our result

    ![alt text](image-5.png)

* Find the DomainController

    * since we had the DNS server, we run an nmap on that

    ![alt text](image-6.png)

    * We see a 53 port, domain on it, so it works

* Hostname

    * one of the host, with the highest ip AND online, seems to be **catalog.vault.vinyl**

    ![alt text](image-7.png)

