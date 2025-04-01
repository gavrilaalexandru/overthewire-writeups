# Bandit Wargame - Level 13 -> Level 14

### Objective
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. 

For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. 

Note: localhost is a hostname that refers to the machine you are working on

Logging into the machine we see that we only have one file:

<img width="202" alt="Screenshot 2025-04-01 at 09 55 19" src="https://github.com/user-attachments/assets/cb33df29-2f10-4764-9a9c-2d52adaa2c86" />

My guess is that we will use the file to connect as user `bandit14`. But first of all we need to transfer the file on our machine. For that we will use [scp](https://linuxize.com/post/how-to-use-scp-command-to-securely-transfer-files/)


**New Password:** `FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn`

