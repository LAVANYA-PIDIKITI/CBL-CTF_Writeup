# Wave
It has a file named id_rsa.xt
# Solution
I had no clue on how to proceed with this so i used https://null-byte.wonderhowto.com/how-to/crack-ssh-private-key-passwords-with-john-ripper-0302810/
to get an idea on how to solve this <br>
1 ) Firstly I installed  SSH2John on the Local Machine <br>
 &nbsp;&nbsp; &nbsp;&nbsp; `wget https://raw.githubusercontent.com/magnumripper/JohnTheRipper/bleeding-jumbo/run/ssh2john.py`<br>
2 ) Next Crack the Private Key on the Local Machine (Make sure you remove the .xt) <br>
  &nbsp;&nbsp; &nbsp;&nbsp; `python ssh2john.py id_rsa > id_rsa.hash` <br>
3 ) Download the wordlist <br>
 &nbsp;&nbsp; &nbsp;&nbsp; `wget https://raw.githubusercontent.com/danielmiessler/SecLists/master/Passwords/darkweb2017-top10.txt` <br>
4 ) Feed the same to John with the hash file <br>
  &nbsp;&nbsp; &nbsp;&nbsp; `john --wordlist=darkweb2017-top10.txt id_rsa.hash` <br>
5 ) View the result <br>
  &nbsp;&nbsp; &nbsp;&nbsp;`john --show id_rsa.hash`

  ![image](https://github.com/LAVANYA-PIDIKITI/CBL-CTF_Writeup/assets/98797256/60fe6cc3-e7c5-4908-a358-2dcae708f964)



