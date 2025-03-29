# Bandit Wargame - Level 2 -> Level 3

### Objective  
The password for the next level is stored in a file called spaces in this filename located in the home directory

Like in the previous level, it is unconventional and goes against best practice to include spaces in a filename (as well as a directory name). Instead, you can use an underscore (_) or a dash (-).

We have several methods in which we can solve this challenge.

First we use ls:

<img width="563" alt="Screenshot 2025-03-29 at 14 07 57" src="https://github.com/user-attachments/assets/fb79fb61-1c77-462b-b80d-8e193208f4f4" />

One way to solve this is to wrap the whole name of the file with `" "` but the way I like to do it is using backslashes:

<img width="567" alt="Screenshot 2025-03-29 at 14 11 26" src="https://github.com/user-attachments/assets/9a1a5bc0-33bb-4c16-9823-98fdce66ce7e" />

(Or you could just type `cat s` and press tab, the autocomplete will do its thing.)

**New Password:** `MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx`

[Next level](https://github.com/gavrilaalexandru/overthewire-writeups/blob/main/bandit/level%203%20-%3E%20level%204.md)
