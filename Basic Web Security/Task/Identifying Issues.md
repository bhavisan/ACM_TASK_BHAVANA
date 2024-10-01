#### CHANGE PASSWORD

<i> In this case, we can see there is a potential vulnerability in the change password fields. Using burp suite, I intercepted the request to change password. I changed the initial password from 'bugs' to 'time' </i>


<img width="944" alt="image" src="https://github.com/user-attachments/assets/92b090d8-394e-47af-9bba-380bd13f4fed">



<img width="457" alt="image" src="https://github.com/user-attachments/assets/771fa0a4-a0d2-40f3-9d3b-68f1efeae628">


<i> Hence, I managed to change the password of a user using CSRF </i>



#### TRANSFER AMOUNT

<img width="476" alt="image" src="https://github.com/user-attachments/assets/d32ebda0-eaf0-46a2-9834-7c6f117e30f5">



<img width="473" alt="image" src="https://github.com/user-attachments/assets/ff463b6b-3076-4527-9761-be9dfb28c663">


<img width="365" alt="image" src="https://github.com/user-attachments/assets/d31143d9-e1dc-4a38-ab13-a2043e6dfdcb">


<img width="472" alt="image" src="https://github.com/user-attachments/assets/6d7393c4-644b-4890-bb58-4fab3ee4a61d">


<i> In this case, the page source code was available, thus it ended up being a vulnerability such that I can manipulate the transfer amount </i>



<img width="942" alt="image" src="https://github.com/user-attachments/assets/156d738b-cda2-456c-b791-e6bd67ec5d70">


 Let's try and enter ' in the search bar 
 

<img width="441" alt="image" src="https://github.com/user-attachments/assets/b15f2e1e-eaec-4353-bc3b-1750dd3b0640">


Lets try and use ' order by 1 -- -


<img width="593" alt="image" src="https://github.com/user-attachments/assets/ef1604ac-9eed-42cf-8c70-7c328b06f5e6">


Lets check if there's any users table


<img width="448" alt="image" src="https://github.com/user-attachments/assets/920635fd-988c-4171-b43b-57ad9d596499">


Yup, now let's try to find the users


<img width="440" alt="image" src="https://github.com/user-attachments/assets/75e2ee06-b078-4aa7-b146-655b286f73bd">


Now that we know all this, let's try to get user credentials


<img width="491" alt="image" src="https://github.com/user-attachments/assets/690f6738-7686-4382-980d-2d8b13c096f1">


So, in this case, we were able to extract information about user through an input field. Improper Input Validation can lead to many vulnerabilities like SQL Injection. In the Documentation.md, I have explained how to solve this issue



