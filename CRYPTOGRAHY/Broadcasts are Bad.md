Solution: recr{H4s4d_is_t0_g00d}

How I solved it:

The challenge is:
![image](https://github.com/user-attachments/assets/9f7617df-49c2-4a03-9c32-f548e138c133)

![image](https://github.com/user-attachments/assets/8bd98b8d-4371-4db2-9e9f-052857b79597)

I figured the Chinese guy is too good was a hint towards some variation of RSA and after some research, I realised there's this method of solving RSA known as Chinese Remainder Theorem (CRT)
The given numbers match the criterion for CRT, we have three moduli values, three cipher values and one value of e = 3.

I have created a python code to solve the CRT: 

![image](https://github.com/user-attachments/assets/a68004ba-64c6-45c5-a07e-feed7a041892)

![image](https://github.com/user-attachments/assets/036608a6-0f66-4d00-a7fe-586d729fd2fd)

![image](https://github.com/user-attachments/assets/f0c06488-674b-41fb-b36d-478a37717716)

