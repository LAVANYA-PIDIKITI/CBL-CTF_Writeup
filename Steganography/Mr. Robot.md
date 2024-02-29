# Mr.Robot
An image is present
# Solution
Now as I saw the image , i tried `binwalk` , `exiftool` , `strings` and `hex` , but nothing worked out . I tried steghide and it asked for passphrase , so i realized
that this was password protected and i need the key to extract the info.<br>
So i installed Stegseek with `sudo apt install stegseek`<br>
And i ran the command using the image file and rockyou.txt `stegseek chall2.jpeg rockyou.txt` the format is `stegseek [image-file] [wordlist.txt] [output.txt]`<br>


![image](https://github.com/LAVANYA-PIDIKITI/CBL-CTF_Writeup/assets/98797256/0dc5848f-f5bf-442e-9adb-f7cc7189ce15)
