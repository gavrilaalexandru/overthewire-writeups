# Bandit Wargame - Level 6 -> Level 7

### Objective  
The password for the next level is stored somewhere on the server and has all of the following properties:
> owned by user bandit7
> 
> owned by group bandit6
> 
> 33 bytes in size

I feel like after the last level this is self explanatory, if you don't know what options you should use, just check `man find` and search for keywords such as `user` and `owner`

<img width="809" alt="Screenshot 2025-03-29 at 14 53 18" src="https://github.com/user-attachments/assets/967716ba-fa29-44e2-9639-112503315d53" />

The user and group options are self explanatory, so let's talk about `2>/dev/null`

`2` is file descriptor ([fd](https://en.wikipedia.org/wiki/File_descriptor)) for `stderr (Standard Error`. But why does that matter? Because we search the whole server for a file owned by another user, and we may find some files we don't have access to, and we will get a `permission denied` error. So basically we are redirecting all those errors to `/dev/null` which is like a black hole. Just like that, we are keeping our terminal clean and only with the information we need.

Let's get that password:

<img width="802" alt="Screenshot 2025-03-29 at 14 58 23" src="https://github.com/user-attachments/assets/aba05797-64a7-44ce-b495-ff09098b5989" />

**New Password:** `morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj`
