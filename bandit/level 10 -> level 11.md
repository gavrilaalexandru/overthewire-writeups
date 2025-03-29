# Bandit Wargame - Level 10 -> Level 11

### Objective  
The password for the next level is stored in the file data.txt, which contains base64 encoded data

Once more we have a text file but this time the contents are base64 encoded data. An easy task if you ask me, considering we have the built-in command `base64`

We can print out the contents of the text file and then piping the output to `base64 -d` (d for decoding) or we can directly use `base64 -d` with the name of the file.

<img width="627" alt="Screenshot 2025-03-29 at 15 23 58" src="https://github.com/user-attachments/assets/2dd1213f-9a32-41a9-aae0-77f35337db0c" />

**New Password:** `dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr`

