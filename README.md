# Capstone_Backend
08-06-2019 02:48 AM 
CUSTOMERCONTROLLER => signup
                    =>login
                    =>logout
                    =>update
                    =>changepassword
                    -------------------------------------------
   SIGNUP=>                 
Update I => Draft version of the First API endpoint "signup - "/customer/signup" has been developed and added to repo.
Output looks like this as of now ., It is not upto the problem definition
![image](https://user-images.githubusercontent.com/44507567/59134112-c209cd00-8997-11e9-866f-2b940308320b.png)
Code has to be reviewed and changes has to be made to it to make it at par with the problem statement .
-------------------------------------------------------------------------------

![image](https://user-images.githubusercontent.com/44507567/59137271-a6f18a00-89a4-11e9-8d76-fd97c1956396.png)

Now API is working fine . ABLE TO CREATE USER USING SIGNUP SUCCESSFULLY.

But some work is pending in signup controller. i.e., checking for restrictions.
In the below picture , 
![image](https://user-images.githubusercontent.com/44507567/59137343-ffc12280-89a4-11e9-8138-1c02517b0b3c.png)

First two validations SGR-001 and SGR-005 are working fine.
As of now , SOME CODE HAS BEEN WRITTEN for rest three validations. CHECKING FORMAT OF EMAIL,CONTACT NUMBER AND PASSWORD.
----------------------------
Some one plz take up this (deepa) and use REGEX (Pattern/Matching) (suggested) or any other way to validate these three exceptions. LOOK BELOW for more details.PLZ HELP.
----------------------
![image](https://user-images.githubusercontent.com/44507567/59137441-8675ff80-89a5-11e9-84b6-a860177609bb.png)
------------
Input format for API Request body ..This is bcoz of @RequestBody(required = false) in customer controller
![image](https://user-images.githubusercontent.com/44507567/59137967-056c3780-89a8-11e9-8bef-314323cda798.png)
---------------------------
Pending tasks for signup: Three format validations code need to be written (assigned to deepa ) [08-06-2019 04:50 AM]
-----------------------------------------------------------------------------------------------------
LOGIN=> started looking into it ...
![image](https://user-images.githubusercontent.com/44507567/59139817-9563ae80-89b3-11e9-84f0-b51c3c4142bd.png)
Testing in progress[06:07AM]  ...Break ..=>
----------------------
Work resumes @ [06:31 AM]
-------------------------------
![image](https://user-images.githubusercontent.com/44507567/59140779-f2656180-89bf-11e9-8b9a-0c4d54e76307.png)
-----------------------------
Here contactNumber is used as username as per problem statement & password is "1234abcd56". So Base 64 encoding of contactnumber:password gives the below code which is used for Basic authentication (when user logsin for the first time)
![image](https://user-images.githubusercontent.com/44507567/59140798-0f019980-89c0-11e9-95df-c43905d874c8.png)
------------------------------
![image](https://user-images.githubusercontent.com/44507567/59140814-39ebed80-89c0-11e9-9766-2f6c84e68260.png)
Plz note accesstoken displayed in response header at the bottom ..(This accesstoken is used till user logsouts or when ever he signsin for second time or any other time.)

-----------------------------
![image](https://user-images.githubusercontent.com/44507567/59140974-c39cba80-89c2-11e9-925d-178c15e6c47f.png)
Two out of three exceptions are taken care of. Some one please write the code for third ATH-003 exception(@deepa).
![image](https://user-images.githubusercontent.com/44507567/59140988-f0e96880-89c2-11e9-9d59-254fc266b2d3.png)
----------------
First two exception working output result as below:
![login_excp_1](https://user-images.githubusercontent.com/44507567/59140996-15dddb80-89c3-11e9-839b-fd2f15fe42c1.JPG)
![login_excp_2](https://user-images.githubusercontent.com/44507567/59140998-1a09f900-89c3-11e9-81c1-7860e3afcb39.JPG)
LOGIN DONE => 1 pending task for deepa , plz define code for exception ATH-003 [07:59 AM]
------------------------------------------------------------------------------------