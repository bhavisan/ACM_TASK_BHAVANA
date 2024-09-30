## SQL INJECTION (1) :

### GET/SEARCH

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
