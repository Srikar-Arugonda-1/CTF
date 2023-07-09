# Flag: kludgeCTF{h3y_my_1ir5t_CTF_Qu3sn}
## Step-1: Getting encrypted text
Look at the end of the hex of the image, You'll notice "Here you go>" copy the hex and convert them to ASCII text and store it in a file.

The hex code:- `53616c7465645f5fcf1fa75c2da8ed41d2ae4c4101b9f2371c59eb885acc4f2c9f28cda8e9dc11284025cb7b19fe94ba45834d73b72607465c44a9b2bef85a63`.

Store it in a file. Convert it into ASCII using the command and store it in another file `xxd -r -p <hexfile> > <ascii-file>`.
## Step-2: Decode
From hints we can say the it is encrypted using **AES**. If we go to regular used encrypted algorithm it is **aes-256-cbc**.

Decode the ascii file using this command `openssl aes-256-cbc -d -in <ascii-file> -out flag.txt`. Use password: "sea" (without double quotes).

open the flag.txt and we got the flag.
