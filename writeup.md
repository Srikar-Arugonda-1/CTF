# Flag: kludgeCTF{h3y_my_1ir5t_CTF_Qu3sn}
## Step-1: Getting encrypted text
Look at the end of the hex of the image, You'll notice "flag:" copy the hex and convert them to ASCII text and store it in a file.

The hex code:- `53616c7465645f5fd5caecf785873ca2aed02e7db510f53192f192882b698404e587b28b051c03f4cedbd293df0785e3`.

Store it in a file. Convert it into ASCII using the command and store it in another file `xxd -r -p <hexfile> > <ascii-file>`.
## Step-2: Decode
From hints we can say the it is encrypted using **AES**. If we go to regular used encrypted algorithm it is **aes-256-cbc**.

Decode the ascii file using this command `openssl aes-256-cbc -d -in <ascii-file> -out flag.txt`. Use password: "sea" (without double quotes).

open the flag.txt and we got the flag.
