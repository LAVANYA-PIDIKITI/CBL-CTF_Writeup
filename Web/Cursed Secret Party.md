# Cursed Secret Party
There's a web link
# Solution
Now this challenge was difficult of all(To me :))). So to begin , once i clicked the webpage it said file parameter missing , so i added the payload to url `?file=flag.txt` , nothing worked out and I almost spent
couple of hours thinking what exactly has to be done. That's when I thought I'll use dirb and check the paths existing in that URL 
![image](https://github.com/LAVANYA-PIDIKITI/CBL-CTF_Writeup/assets/98797256/74631e79-0025-431c-b215-136c97409b4a)

I passed the url in two ways where it normally checks if there are any subdirectories and one more with .php extension . `index.php` was the result it gave and on opening the index.php it said
![image](https://github.com/LAVANYA-PIDIKITI/CBL-CTF_Writeup/assets/98797256/493cde69-863e-426d-a631-744b50cbba29) <br>
This is where things started to confuse me , I understood that it was hardcoded text and I gotta do something. I checked the subdirectories but nothing popped . I was exploring the path and understood that w2 is directory 
and I gotta pass the right command to view the file . I browsed internet about this situation and found out that it's <h5>Local File Inclusion - php vulnerability</h5>

Now i passed the index.php as filter using: `http://174.129.132.216:5004/w2?file=php://filter/convert.base64-encode/resource=index.php`
Main part : `php://filter/convert.base64-encode/resource=index.php`
Now after doing this, It gives a base 64 encoded string and after decoding it you get the file at the end.


