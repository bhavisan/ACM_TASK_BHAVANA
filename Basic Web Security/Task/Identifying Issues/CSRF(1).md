## CSRF 
#### CHANGE PASSWORD

<i> In this case, we can see there is a potential vulnerability in the change password fields. Using burp suite, I intercepted the request to change password. I changed the initial password from 'bugs' to 'time' </i>


<img width="944" alt="image" src="https://github.com/user-attachments/assets/92b090d8-394e-47af-9bba-380bd13f4fed">



<img width="457" alt="image" src="https://github.com/user-attachments/assets/771fa0a4-a0d2-40f3-9d3b-68f1efeae628">


<i> Hence, I managed to change the password of a user using CSRF </i>

#### CHANGE SECRET

<i> Here also, I can change the secret message by intercepting the request and forwarding the modified secret. </i>

#### TRANSFER AMOUNT

<img width="476" alt="image" src="https://github.com/user-attachments/assets/d32ebda0-eaf0-46a2-9834-7c6f117e30f5">


<img width="286" alt="image" src="https://github.com/user-attachments/assets/fb056a7d-08a7-4142-9589-5083abb7cc94">


<img width="473" alt="image" src="https://github.com/user-attachments/assets/ff463b6b-3076-4527-9761-be9dfb28c663">


<img width="365" alt="image" src="https://github.com/user-attachments/assets/d31143d9-e1dc-4a38-ab13-a2043e6dfdcb">


<img width="472" alt="image" src="https://github.com/user-attachments/assets/6d7393c4-644b-4890-bb58-4fab3ee4a61d">


<i> In this case, the page source code was available, thus it ended up being a vulnerability such that I can manipulate the transfer amount </i>
