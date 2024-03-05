# Scanning

# 10.11.12.6

FLAGS FOUND:
- LDAP service - shared directory (FLAG-6811)
- DIG txt (banner) grabbing (FLAG-6649)

## Nmap scanning

![NMAP scan](image.png)

## Dig

![Dig axfr scan](image-12.png)

The command dig axfr @10.11.12.6 vault.vinyl initiates a DNS zone transfer request for the domain vault.vinyl using the AXFR protocol. This request is sent to the DNS server at IP address 10.11.12.6. The AXFR protocol is used to replicate DNS records across DNS servers, allowing for the efficient management of DNS zones without manual edits on multiple servers.

## nbts scan

![nbtscan](image-1.png)

## ldap scan

sudo nmap --script=ldap-rootdse 10.11.12.6 

![LDAP scan](image-2.png)

![LDAP scan2](image-3.png)

![LDAP scan3](image-4.png)

## RPC scan

You get this folder, because you are talking to the NFS service.

![showmount](image-5.png)

![Shared Folder + Flag](image-7.png)

# 10.11.12.13

## NMAP

Port 53 open, meaning we have a DNS server (domain)

![NMAP scan](image-6.png)

![NMPA version](image-11.png)

## Dig

dig any victim.com @10.11.12.13 - dig any victim.com @<DNS_IP>

![Dig check of strings](image-8.png)

![Dig check A](image-9.png)

![Dig check A 2](image-10.png)