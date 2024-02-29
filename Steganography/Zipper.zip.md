# Zipper.zip
There's a zip file
# Solution
I downloaded the zip file and tried extracting the `CONFIDENTIAL.pdf` but it was pwd protected.
So used the fcrackzip tool
Installed it using `sudo apt install fcrackzip` <br>
Next utilization is `fcrackzip -D -p rockyou.txt -v -u zipper.zip` <br>
![image](https://github.com/LAVANYA-PIDIKITI/CBL-CTF_Writeup/assets/98797256/d5492eef-aa23-47c0-bf7d-f120badde790) <br>
Now i entered the password and saw the flag in the pdf

