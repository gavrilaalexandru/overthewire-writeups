# Bandit Wargame - Level 3 -> Level 4

### Objective  
The password for the next level is stored in a hidden file in the inhere directory.

To traverse the directories, the “change directory” command exists: cd <path>.

The path for the command can be an absolute path (path from root directory /) or a relative path (path from the current working directory).

First let's use ls:

<img width="560" alt="Screenshot 2025-03-29 at 14 16 19" src="https://github.com/user-attachments/assets/edb48c68-9d3f-4a96-8c97-782ba83b7fa5" />

If we are not sure if `inhere` is a file or a directory we can use `ls -l` which displays file details (permissions, owner, group, size, modification date):

<img width="362" alt="Screenshot 2025-03-29 at 14 18 12" src="https://github.com/user-attachments/assets/1eed1c1c-687c-4ecd-8c11-3c35fbcff250" />

The `d` there means directory, so let's `cd` into `inhere`:

<img width="558" alt="Screenshot 2025-03-29 at 14 18 58" src="https://github.com/user-attachments/assets/c6293353-8711-4fe9-9b3e-fa8a3d11e04c" />

So the directory is empty, but we can check for one more thing, hidden files. Let's use `ls -lah`:

<img width="489" alt="Screenshot 2025-03-29 at 14 20 06" src="https://github.com/user-attachments/assets/50a08b20-fbc2-41a3-952c-9b83a67134bd" />

Interesing file down there, let's use `cat`:

<img width="421" alt="Screenshot 2025-03-29 at 14 20 40" src="https://github.com/user-attachments/assets/04acb52f-7424-46dd-a050-9ce882931b9b" />

**New Password:** `2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ`
