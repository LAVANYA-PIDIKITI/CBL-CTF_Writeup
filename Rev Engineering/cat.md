# cat
There's a file
# Solution 
Run the below provided script to get the key and enter the same for the flag
```python
import subprocess

# Loop from 1 to 1000
for i in range(1, 1001):
    # Construct the command to run the executable and pass the key as input
    command = f'echo "{i}" | ./infant'

    # Execute the command in the terminal
    process = subprocess.Popen(command, shell=True, stdout=subprocess.PIPE, stderr=subprocess.PIPE, text=True)

    # Capture the output
    stdout, stderr = process.communicate()

    # Print the output
    print(f"Key: {i}, Output: {stdout.strip()}, Error: {stderr.strip()}")
```
![image](https://github.com/LAVANYA-PIDIKITI/CBL-CTF_Writeup/assets/98797256/1ac1bde2-038d-430b-994b-2eb143a3bb8b)
