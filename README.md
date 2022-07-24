# Bypass Authentication in web applications

- ## Difinition of Authentication 

- Authentication is the process of verifying the identity of an individual. A user can interact with a web application using multiple actions. Access to certain actions or pages can be restricted using user levels. Authorization is the process of controlling user access via assigned roles & privileges

- ## Some ways to bypass authentication in web applications
- ### Bypass Authentication using sql injection 
 ![image info](https://raw.githubusercontent.com/ADNXB/test/main/owasp_injection_10.png)
##### first we need to check for potential SQL injection vulnerability we have entered a single quote in to the Name field and submitted the request 
.
 ![image info](https://raw.githubusercontent.com/ADNXB/test/main/owasp_injection_11.png)

##### so we generated an SQL error message , let's exploit this 
![image info](https://raw.githubusercontent.com/ADNXB/test/main/owasp_injection_12.png)
##### Enter some appropriate syntax to modify the SQL query into the "Name" input.In this example we used ```' or 1=1 -- .This causes the application to perform the query:SELECT * FROM users WHERE username = '' OR 1=1-- ' AND password = 'RandomPassword'```Because the comment sequence (--) causes the remainder of the query to be ignored, this is equivalent to ```SELECT * FROM users WHERE username = ' ' OR 1=1```

![image](https://raw.githubusercontent.com/ADNXB/test/main/owasp_injection_13%20(1).png)
##### As we can see, we successfully log in as administrator


- ### 
