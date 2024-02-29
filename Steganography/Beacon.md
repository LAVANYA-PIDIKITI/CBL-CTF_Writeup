# Beacon
There's a file which had the name Beacon.png.txt

# Solution
I opened the same file using a hex editor and changed the header value to png header value. Next up i saved the same as png<br>
Process:
1) Find out the PNG Header<br>
![image](https://github.com/LAVANYA-PIDIKITI/CBL-CTF_Writeup/assets/98797256/ded2ffb1-a589-41e0-bc03-21ae9114173e)<br>
```code
89 50 4E 47 0D 0A 1A 0A
```
2) Next open a hex editor and change the values to png header
![image](https://github.com/LAVANYA-PIDIKITI/CBL-CTF_Writeup/assets/98797256/0227f897-f7c7-4893-a7ab-30c3c9e2404e) <br>
![image](https://github.com/LAVANYA-PIDIKITI/CBL-CTF_Writeup/assets/98797256/8cb49de0-e6cf-40a9-8072-6bf26f7e0026)<br>
Now save the above as with .png format <br><br>
![image](https://github.com/LAVANYA-PIDIKITI/CBL-CTF_Writeup/assets/98797256/e71443e7-b369-4321-8108-4badfac687c7)




