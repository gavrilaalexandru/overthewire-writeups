# Bandit Wargame - Level 12 -> Level 13

### Objective
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed.

For this level it may be useful to create a directory under /tmp in which you can work. 

Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

Let's dig in:

<img width="532" alt="Screenshot 2025-04-01 at 09 18 19" src="https://github.com/user-attachments/assets/d7f02adc-eaa9-4afe-a399-155d850581cc" />

And this already looks like a hexdump. We will use [xxd](https://man.archlinux.org/man/xxd.1.en) for analyzing.

First, let's do as the objective says, and create a temporary folder (with [mktemp](https://en.wikipedia.org/wiki/Mktemp)). 

Be aware that this folder will not be automatically deleted, this is a useful command in bash scripts.

<img width="539" alt="Screenshot 2025-04-01 at 09 22 22" src="https://github.com/user-attachments/assets/e1b7c9d4-4b3c-42ba-8b37-2e50d1c2f534" />

The `-d` option specifies to create a directory.

Let's `cd` into our newly created folder and let's copy our file:

<img width="557" alt="Screenshot 2025-04-01 at 09 25 25" src="https://github.com/user-attachments/assets/19dff904-6481-4e46-86e0-d0f939f09de5" />

And let's rename our file:

<img width="571" alt="Screenshot 2025-04-01 at 09 26 40" src="https://github.com/user-attachments/assets/9b52f249-48ca-4080-b5c2-f80ad6e8eec8" />

From the objective we know that the file has been repeatedly compressed.

So let's start decompressing our lovely file. To figure out what decompression we need to use, we will analyze the first bytes in the hexdump and search for the file type in [here](https://en.wikipedia.org/wiki/List_of_file_signatures)



**New Password:** `7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4`

