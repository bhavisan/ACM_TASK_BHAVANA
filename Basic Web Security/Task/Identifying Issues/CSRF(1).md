## CSRF (1)
### CHANGE PASSWORD

In this case, we can see there is a potential vulnerability in the change password fields. Using burp suite, I intercepted the request to change password. I changed the initial password from 'bugs' to 'time'

<img width="944" alt="image" src="https://github.com/user-attachments/assets/92b090d8-394e-47af-9bba-380bd13f4fed">


<img width="457" alt="image" src="https://github.com/user-attachments/assets/771fa0a4-a0d2-40f3-9d3b-68f1efeae628">

Hence, I managed to change the password of a user using CSRF
