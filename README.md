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









Findings from the Reverse Engineering Lab Activity
1.Objective: 
The aim was reverse engineering a binary application called password_app in order to access a test website that required a username and password.

2.Analysis Method: 
We reversed the binary file, which we used Ghidra, a popular reverse engineering tool.

3.Initial Step - Default Scan:

Put the “password_app” binary into Ghidra and load it.
We did a default scan and extracted the source code so we can further analyze the application.

4.Analyzing the 'main' Function:

We tried navigate inside the main function so we can examine the logic behind that function.
It was identified that the application checks a so called password before granting access.

5.Extracting the Password:

Instead, we found the hardcoded password in the decompiled source code.

6.Testing the Credentials:

Put the extracted password into the test website’s login page.
Successfully logged in and confirmed correctness of the extracted credentials.

7.Conclusion:

To bypass login requirement, we can do reverse engineering using Ghidra.
This lab helped us to appreciate how important it is to practice secure coding practices, i.e. making sure that when implementing an application, we’re not storing passwords in hard coded strings.
Security testing and vulnerability assessment cannot do without understanding reverse engineering techniques.


Learnings: 

1.Understanding Reverse Engineering:
We learned to decompile and analyse binary files using Ghidra.
Got a better understanding on how compiled applications store and handle sensitive information.

2.Importance of Secure Coding Practices:

Understood that hardcoded passwords can be a problem in apps.
These should be implemented by developers in the use of secure authentication mechanisms such as hashing, encryption, and environment variables for credentials.

3.Binary Analysis & Code Inspection:

Learned how to work through a disassembled code and find main().
Was able to understand how to determine the functionality of authentication in a compiled program.

4.Hands-on Experience with Ghidra:

Using the default scan, function navigation, and decompiler tools of Ghidra.
Better ability to read and understand reverse C code.


5.Practical Ethical Hacking Knowledge:

Become exposed to actual software security vulnerabilities in the wild.
It was understood how attackers may use insecure code, as well as how security professionals can detect such flaws.

6.Critical Thinking & Problem-Solving:

Had developed skills to analyze an unknown codebase which could have exploitable weakness.
This further improved my thinking on debugging and troubleshooting the software security issues.

7.Legal & Ethical Considerations:

We learned to reverse engineer only in ethical and legal environments like security testing and academic research.
Realized that security vulnerabilities should be responsible disclosed.

Reinforcing the importance of software and ethical hacking, secure coding and reverse engineering, and both of these were demonstrated through hands on experience in the lab.
