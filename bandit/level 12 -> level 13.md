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

From the objective we know that the file has been repeatedly compressed. However, we want to operate on the actual data. Therefore, we revert the hexdump and get the actual data.

<img width="557" alt="Screenshot 2025-04-01 at 09 35 19" src="https://github.com/user-attachments/assets/c4b55c1c-9070-4cef-b78f-6dbefd937a92" />


So let's start decompressing our lovely file. To figure out what decompression we need to use, we will analyze the first bytes in the hexdump and search for the file type in [here](https://en.wikipedia.org/wiki/List_of_file_signatures).

<img width="510" alt="Screenshot 2025-04-01 at 09 30 21" src="https://github.com/user-attachments/assets/25f98647-bb6e-4402-a7d6-94d87c9d2f1a" />

We see that the first bytes are `1f 8b`. Let's search for it on the wiki page:

<img width="953" alt="Screenshot 2025-04-01 at 09 31 40" src="https://github.com/user-attachments/assets/286243cc-abf2-4d54-8c6d-40af8d45538e" />

And we found it! Let's rename our file and decompress it with `gzip -d`:

<img width="563" alt="Screenshot 2025-04-01 at 09 36 55" src="https://github.com/user-attachments/assets/ca1b6a11-9ac2-4dbd-8ad1-2512ec3b9f0e" />

And we can still see that the data is still not fully decompressed. Let's use `xxd` and look at the first bytes again:

<img width="531" alt="Screenshot 2025-04-01 at 09 38 23" src="https://github.com/user-attachments/assets/15d36f3d-e660-49ff-9d39-153fc7852cd1" />

And if we search on the wiki page, we can see that our first bytes matches bzi2. Let's rename and decompress it with `bzip2 -d`:

<img width="571" alt="Screenshot 2025-04-01 at 09 40 24" src="https://github.com/user-attachments/assets/bbfbbf3b-0184-4d71-be74-711855b1fcbf" />

Aaaand it's still not fully decompressed. Let's do it all over again:

<img width="505" alt="Screenshot 2025-04-01 at 09 41 18" src="https://github.com/user-attachments/assets/f4625067-3880-455d-8751-15db145d0853" />

And it's again gzip:

<img width="560" alt="Screenshot 2025-04-01 at 09 41 47" src="https://github.com/user-attachments/assets/5f8eb619-6532-4a2f-bc72-ab978a3a7403" />

Still not done yet:

<img width="573" alt="Screenshot 2025-04-01 at 09 43 17" src="https://github.com/user-attachments/assets/a339c2e7-9afc-4d26-bd75-d2d676c95143" />

If we only print the first 10 lines we can see `data5.bin` which is a sign of a tar archive. Also if u are looking into all the `xxd` output we can see `ustar` which is the POSIX standard form of TAr, Unix's tape archive format.

Let's rename and extract the files:

<img width="536" alt="Screenshot 2025-04-01 at 09 45 32" src="https://github.com/user-attachments/assets/d0107527-3932-4dfc-a26e-d2ae4adce412" />

Now let's analyze the new file:

<img width="532" alt="Screenshot 2025-04-01 at 09 46 53" src="https://github.com/user-attachments/assets/67aa9bd7-36d0-4b29-a520-ca968b19ed1e" />

And seems like we have another tar archive:

<img width="530" alt="Screenshot 2025-04-01 at 09 47 44" src="https://github.com/user-attachments/assets/e92992a8-02ec-4e69-acd8-dab367053780" />

And let's analyze our new file again:

<img width="538" alt="Screenshot 2025-04-01 at 09 48 15" src="https://github.com/user-attachments/assets/e4eeb68c-b6a7-451b-ad51-ec25594ec3da" />

And again bzip2:

<img width="501" alt="Screenshot 2025-04-01 at 09 48 45" src="https://github.com/user-attachments/assets/b49a00ef-3ca6-42ee-aa65-911328bac8f0" />

Analyzing the file wee see that we have another archive:

<img width="533" alt="Screenshot 2025-04-01 at 09 49 17" src="https://github.com/user-attachments/assets/fa5d3271-f53e-4725-baef-32ff7e2e1687" />

<img width="595" alt="Screenshot 2025-04-01 at 09 50 04" src="https://github.com/user-attachments/assets/ec581314-f014-4e67-8276-df394973e820" />


**New Password:** `7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4`

