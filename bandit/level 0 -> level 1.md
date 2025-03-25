# Bandit Wargame - Level 0 -> Level 1 

### Objective  
Find the "hidden" password!
PS: Create a dedicated file for notes and passwords on your local machine!

**Server Details:**  
- **Host:** `bandit.labs.overthewire.org`  
- **Port:** `2220`  
- **Username:** `bandit0`  
- **Password:** `bandit0`  

After we ssh into the server we can use the ls command ([list](https://en.wikipedia.org/wiki/Ls)) to list all the files in our current directory.

<img width="570" alt="Screenshot 2025-03-26 at 00 15 42" src="https://github.com/user-attachments/assets/a123d456-4f54-4979-b488-c543806ac1d8" />

So we can see that the only available file is an auto-suggestive readme file.
Let's use the cat command ([cat](https://en.wikipedia.org/wiki/Cat_(Unix))) to examine the contents of the file.

<img width="565" alt="Screenshot 2025-03-26 at 00 17 35" src="https://github.com/user-attachments/assets/35eb65c4-1b73-4654-88a0-90dfbaead388" />

And like that we made our first steps into the bandit game!

**New Password:** `ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If`
