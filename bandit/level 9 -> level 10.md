# Bandit Wargame - Level 9 -> Level 10

### Objective  
The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

You already know the drill, one text file with a few human-readable strings in it. Now we will use `strings` because it can be used to extract and display readable character sequences from binary files. 

It is especially useful for finding hidden text in executables, libraries, memory dumps, or other binary files.

And because we know our string is preceded by several '=' chars we will pipe the output to `grep`:

<img width="507" alt="Screenshot 2025-03-29 at 15 20 07" src="https://github.com/user-attachments/assets/c06faec4-9edf-43f1-93a4-6ea08ec552e5" />

**New Password:** `FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey`

