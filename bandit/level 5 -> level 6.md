# Bandit Wargame - Level 5 -> Level 6

### Objective  
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
> human-readable
> 
> 1033 bytes in size
> 
> not executable

After doing all the steps we did previously, we see that now we have 20 folders or so

<img width="569" alt="Screenshot 2025-03-29 at 14 37 09" src="https://github.com/user-attachments/assets/44c4da63-5d01-4332-babc-3192a05f2f01" />

Let's use `ls` on one of the folders:

<img width="536" alt="Screenshot 2025-03-29 at 14 37 58" src="https://github.com/user-attachments/assets/7c0bdaa3-f935-4fbf-978a-bc2de3d4f8c6" />

We can presume every folder has atleast the same number of files.

When dealing with many files, the `find` command can help us using its various options.

<img width="567" alt="Screenshot 2025-03-29 at 14 43 24" src="https://github.com/user-attachments/assets/e7ed5032-57ec-4fbb-986d-19def9567805" />

So `type f` for searching regular files, `-size 1033c` for searching files using exactly 1033 bytes and `! -executable` to search files that are not executable (self explanatory)

Let's find the password:

<img width="567" alt="Screenshot 2025-03-29 at 14 47 56" src="https://github.com/user-attachments/assets/321563b7-79ac-4e88-9e78-01e114bd0f92" />


**New Password:** `HWasnPhtq9AVKe0dmk45nxy20cvUa6EG`
