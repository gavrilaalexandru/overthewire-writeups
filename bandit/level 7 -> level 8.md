# Bandit Wargame - Level 7 -> Level 8

### Objective  
The password for the next level is stored in the file data.txt next to the word millionth

Let's see what we have here:

<img width="556" alt="Screenshot 2025-03-29 at 15 03 42" src="https://github.com/user-attachments/assets/d5de5f4e-8ce8-495b-90d2-a98d5f7e841e" />

Only one text file, let's try and cat the contents:

<img width="781" alt="Screenshot 2025-03-29 at 15 04 27" src="https://github.com/user-attachments/assets/14bbd69a-c0fb-4156-bcf6-ae417365afd1" />

That was not very helpful, just as it doesn't help us to try every string that looks like a password.

Instead let's print the contents of `data.txt` and let's use the `|` symbol ([pipe](https://www.geeksforgeeks.org/piping-in-unix-or-linux/)) and pipe the output into `grep` ([grep](https://www.geeksforgeeks.org/grep-command-in-unixlinux/))
**New Password:** `morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj`
