# Blue-THM
Walkthrough on exploiting a target vulnerable to the eternal blue exploit. 

#Important info ip address of attacker is 10.113.186.148 and that of target is 10.113.158.252

<h1>STEP 1</h1>

After turning on both machines, I run an nmap scan to identify which port were open on the target host. From the screenshot I can see that <strong>netbios-ssn</strong> is open that means the eternal blue exploit can be used

<img width="489" height="311" alt="image" src="https://github.com/user-attachments/assets/10a33f91-4105-450c-8404-d14950c9cdc6" />

<h1>STEP 2</h1>

I started the metasploit framework and search for the eternal blue exploit

<img width="469" height="368" alt="image" src="https://github.com/user-attachments/assets/98b0f090-344d-4a1f-8f63-599dc253c6ec" />

<h1>STEP 3</h1>

<img width="497" height="408" alt="image" src="https://github.com/user-attachments/assets/594b622a-7cf7-41dc-828e-9478b0415585" />

<h1>STEP 4</h1>

I set the value of RHOST to the ip address of the target machine

<img width="535" height="383" alt="image" src="https://github.com/user-attachments/assets/13f5cbd8-9030-481b-afd0-2e704c110a8a" />

My first failed run of the exploit

<img width="467" height="309" alt="image" src="https://github.com/user-attachments/assets/5c382268-8bc3-46ca-b587-c511b920ee40" />


<h4>SUCCESS</h4>

Able to accesss the shell of target machine

<img width="494" height="376" alt="image" src="https://github.com/user-attachments/assets/4647bf13-169a-4fa8-9b14-f35f3f93caed" />

<h1>STEP 5</h1>

In this step, i was looking at upgrading a standard command shell to a Meterpreter session in Metasploit. <h5>Why?</h5>

<img width="469" height="167" alt="image" src="https://github.com/user-attachments/assets/0341e86e-8089-44f1-86b7-fb9358c17a64" />

<h4>Identifying the session id of the background process</h4>

<img width="494" height="396" alt="image" src="https://github.com/user-attachments/assets/6c5fdaf6-0fd0-4f2e-a655-8de759b4b6b5" />

<h1>STEP 6</h1> From this moment i am running a different session so there would be a change in the ip addresses

run the exploit

<img width="518" height="254" alt="image" src="https://github.com/user-attachments/assets/6ce6072c-1858-448b-b205-f0bfacf62760" />

I was able to get a meterpreter shell

<img width="545" height="334" alt="image" src="https://github.com/user-attachments/assets/c95d0615-1568-48fe-ae04-daa469b5e1c4" />

I verify escalation to NT AUTHORITY\SYSTEM

<img width="497" height="112" alt="image" src="https://github.com/user-attachments/assets/16420543-ab6d-452b-a5fa-668d30682964" />

<img width="635" height="321" alt="image" src="https://github.com/user-attachments/assets/820c8c22-4e00-4121-b552-79fa6e794b40" />
