# Bandit Wargame - Level 13 -> Level 14

### Objective
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. 

For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. 

Note: localhost is a hostname that refers to the machine you are working on

Logging into the machine we see that we only have one file:

<img width="202" alt="Screenshot 2025-04-01 at 09 55 19" src="https://github.com/user-attachments/assets/cb33df29-2f10-4764-9a9c-2d52adaa2c86" />

My guess is that we will use the file to connect as user `bandit14`. But first of all we need to transfer the file on our machine. For that we will use [scp](https://linuxize.com/post/how-to-use-scp-command-to-securely-transfer-files/).

<img width="1009" alt="Screenshot 2025-04-01 at 09 58 12" src="https://github.com/user-attachments/assets/30597cd0-743a-4c33-9a0f-5b025d8110cd" />

And let's try and connect with `ssh -i` (if you get this warning `Permissions 0640 for 'sshkey.private' are too open.` just reduce the file permision with `chmod 700`)

<img width="727" alt="Screenshot 2025-04-01 at 10 00 10" src="https://github.com/user-attachments/assets/a12aa07d-965d-4e97-98ef-3512000f42f1" />

And we got in!
