# Bandit Wargame - Level 11 -> Level 12

### Objective
The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

This already sounds like a substitution cypher ([ROT13](https://en.wikipedia.org/wiki/ROT13)) in which a letter is replaced (substituted) with the 13th letter after it.


The Linux `tr` ([tr](https://en.wikipedia.org/wiki/Tr_(Unix))) command, which stands for ’translate’, allows replacing characters with others.

Let's dig in:

<img width="561" alt="Screenshot 2025-04-01 at 09 10 01" src="https://github.com/user-attachments/assets/de40f2f7-dc13-491c-9b7d-56e2db461693" />

And let's use `tr`:

<img width="559" alt="Screenshot 2025-04-01 at 09 15 37" src="https://github.com/user-attachments/assets/a109f7e4-d0ab-4a3b-b04c-eb326470673d" />


**New Password:** `7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4`

