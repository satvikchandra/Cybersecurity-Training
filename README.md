This repository contains my college project demonstrating John the Ripper for educational password cracking simulations.

# John the Ripper

This is the community-enhanced, "jumbo" version of John the Ripper. It has a lot of code, documentation, and data contributed by jumbo developers and the user community. It is easy for new code to be added to jumbo, and the quality requirements are low, although lately we've started subjecting all contributions to quite some automated testing. This means that you get a lot of functionality that is not necessarily "mature", which in turn means that bugs in this code are to be expected.

## John the Ripper password cracker.

John the Ripper is a fast password cracker, currently available for many flavors of Unix, macOS, Windows, DOS, BeOS, and OpenVMS (the latter requires a contributed patch). Its primary purpose is to detect weak Unix passwords. Besides several crypt(3) password hash types most commonly found on various Unix flavors, supported out of the box are Kerberos/AFS and Windows LM hashes, as well as DES-based tripcodes, plus hundreds of additional hashes and ciphers in "-jumbo" versions.

## How to install
Go to the official website: 
```bash
openwall.com/john.
```
Download the community edition (free):

For Windows: Download the ZIP file, extract it, and run the installer. No admin rights needed usually.

For Linux (e.g., Ubuntu): Open a terminal and run:
```bash
sudo apt update
sudo apt install john
```
For Mac: Use Homebrew if you have it installed: brew install john. Otherwise, download the source code and compile it (quick guide on the site).

Verify installation: Open a command prompt or terminal and type john --version. It should display the version number. If not, double-check your download or search for "John the Ripper installation troubleshooting" on their site.

## How to use John the Ripper
- Firstly, open the kali linux operating system. Here, we add a user, for example, david. We set the password for this david user. 
```bash
sudo adduser david
```
- Then we find the shadow file which contains the hash password of the david user. It is located in etc folder. We extract the contents of this shadow file using:
```bash
sudo cat shadow
```
- Then we copy the hash password, create a text file on desktop and paste the hash password in the text file. To create a new file:
```bash
nano hash.txt
```
- Now we need to get a worlist file- a wordlist file contains millions of hash password. In kali linux, a file named rockyou.txt can be used as a wordlist file. Its located in wordlist folder. We need to unzip the file using
```bash
sudo gunzip rockyou.txt.gz
```
- Finally, using John the Ripper we are going to crack the password. For this, we use the syntax
```bash
sudo john -format=crypt --wordlist=/usr/share/wordlists/rockyou.txt hash.txt
```
The password will be successfully cracked!
  
