# port 5432

We will use metasploit for postgres penetration as well.
![alt text](<msg1709277568-34902 (1).jpg>)

First thing to do is always search for vulnerability
![alt text](<msg1709277568-34903 (1).jpg>)

![alt text](<msg1709277568-34904 (1).jpg>)
The **postgres_payload** module exploits a vulnerability where the PostgreSQL service account may write to the /tmp directory allowing execution of arbitrary code.

The next step to the process is to configure for necessary changes.
![alt text](<msg1709277568-34906 (1).jpg>)

The error arises because **LHOST** has not been updated.
![alt text](<msg1709277568-34905 (1).jpg>)
![alt text](<msg1709277568-34907 (1).jpg>)

The similar situation has occured. So we basically get into nmap like we did before and gain root access like before.
![alt text](<msg1709277568-34908 (1).jpg>)
![alt text](<msg1709277568-34910 (1).jpg>)

This is how it will look like at the end. As you can see i have the authorization to create a file/folder.
