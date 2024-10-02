Solution:

Unopenable og.pdf shows the base64 code: 

Rm9yZW5zaWNzIGlzIGZ1bg==

Decoding it gives:

Forensics is fun

Explanation: 


The challenge requested that the zip file be cracked using a script rather than relying on external tools. Initially, I approached this by exploring possible methods to brute-force or dictionary-attack the zip file using a custom script in Python. However, after several attempts, I came across two problems:

1. For brute force attack, the script takes too much time, and my script only managed to check up until 4 characters. I realised this method was too impractical and time consuming.

2. The second method I could use was a dictionary attack, however no wordlists were provided and there were no hints to what could potentially be the words either. I tried using commonly known wordlists like rockyou.txt, but that didn't work. I also tried to use potential words based on the information I had, like Unopenable og, trybreakingme and more of its combinations.



When both these methods gave me negative responses, I ultimately turned to John the Ripper.

While this deviates from the original requirement, using John the Ripper allowed me to complete the challenge successfully.
