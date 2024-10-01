Solution: recr{H4s4d_is_t0_g00d}

How I solved it:

The challenge is:
![image](https://github.com/user-attachments/assets/9f7617df-49c2-4a03-9c32-f548e138c133)

![image](https://github.com/user-attachments/assets/8bd98b8d-4371-4db2-9e9f-052857b79597)

I figured the Chinese guy is too good was a hint towards some variation of RSA and after some research, I realised there's this method of solving RSA known as Chinese Remainder Theorem (CRT)
The given numbers match the criterion for CRT, we have three moduli values, three cipher values and one value of e = 3.

I have created a python code to solve the CRT: 

![image](https://github.com/user-attachments/assets/e93323f1-29be-4ca9-b2a9-f358e96ea4b7)

![image](https://github.com/user-attachments/assets/ae2d08b8-e484-46dd-b2f1-cb5ecafd7578)

