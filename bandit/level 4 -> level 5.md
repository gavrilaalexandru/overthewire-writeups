# Bandit Wargame - Level 4 -> Level 5

### Objective  
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

The file command gives us the type of data of the file. Some examples would be: ‘ELF’, ‘Perl script’, ‘ASCII text’, ‘data’ and more.

For this task, we are looking specifically for human-readable files. It means that the data is presented so that we can read the information.

First let's `cd` into the folder and use `ls`:

<img width="564" alt="Screenshot 2025-03-29 at 14 25 11" src="https://github.com/user-attachments/assets/82f9798f-a51c-4983-9d74-a1a9e08f46a6" />

We can use different methods, such as printing every file's content with `cat` or just use `file` with every file, but that's inefficient.

Therefore we can use the wildcard (`*` symbol) to get the type for all the files, making our lives easier:

<img width="554" alt="Screenshot 2025-03-29 at 14 30 38" src="https://github.com/user-attachments/assets/9c854a4b-7a9a-4906-960c-9af1fa3f597d" />

So the final command is to use `cat` and print the contents of the file that contains ASCII text:

<img width="566" alt="Screenshot 2025-03-29 at 14 32 03" src="https://github.com/user-attachments/assets/7c992e20-5632-4a0e-8ec0-176cc7a9527c" />

**New Password:** `4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw`
