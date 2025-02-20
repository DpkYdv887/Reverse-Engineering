# Reverse-Engineering



Here is a website that asks for username and password for login. For now, we don’t have the credentials to log in.



![image alt](https://github.com/DpkYdv887/Reverse-Engineering/blob/main/images/Picture1.png)


![image alt](https://github.com/DpkYdv887/Reverse-Engineering/blob/main/images/Picture2.png)

And in order to find the contents of the source code, we find the source code from the binary file, in this case it’s password_app and then import that file in ghidra for source code analysis.



![image alt](https://github.com/DpkYdv887/Reverse-Engineering/blob/main/images/Picture3.png)



After running the default scan in this file we get this in the ghidra dashboard:


![image alt](https://github.com/DpkYdv887/Reverse-Engineering/blob/main/images/Picture4.png)



Now we are exploring the ‘functions’ tree in the left tab: we choose the main function for analysis.


![image alt](https://github.com/DpkYdv887/Reverse-Engineering/blob/main/images/Picture5.png)


Here, we can see that the functions allows login access to the password “letmein123” and denies any other password besides this.


![image alt](https://github.com/DpkYdv887/Reverse-Engineering/blob/main/images/Picture6.png)

 
After entering the password “letmein123” in the login page, we successfully log in to the website and even without entering anything in the username in this case.




![image alt](https://github.com/DpkYdv887/Reverse-Engineering/blob/main/images/Picture7.png)






