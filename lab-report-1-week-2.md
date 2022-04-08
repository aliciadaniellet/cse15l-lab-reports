[Github](lab-report-1-week-2.html)

# Topic: Remote Access
## ‘How to log into a course-specific account on ieng6’


>Part 1: Installing VS Code

Head to this [link](https://code.visualstudio.com/) and follow the guidelines on how to install Visual Studio Code according to the operating system your computer is using (ex. MacOS, Windows). Once you have installed it properly, it should look like the screenshot below when you open the VScode application. 

---

>Part 2: Remote Connectivity

Remotely connecting means connecting your computer(*the client*) to a remote computer(*the server*) where you can upload and do your work there, whilst being in any location. This is an important concept because in many companies, remote connectivity allows employees to access important files from a remote computer in whichever location they are. Thus, working becomes more efficient as it is easily accessible.

Here are a few steps that you can take to connect your computer to a remote computer for the CSE15L course (if this is your first time):

1. Windows users must install the OpenSSH program provided in this [link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) to be able to connect the users’ computer to other computers.

2. Look up for your CSE15L course-specific account through this [link](https://sdacs.ucsd.edu/~icc/index.php). Take note of your course-specific account and password.

3. Go to your VScode and open a new terminal. Insert this command, but replace the zzz by the letters provided in your course-specific account: 
    ssh cs15lsp22zzz@ieng6.ucsd.edu

4. After entering the command above, you will receive a message like this:

        ⤇ ssh cs15lsp22zz@ieng6.ucsd.edu

        The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.

        RSA key fingerprint is SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.

        Are you sure you want to continue connecting (yes/no/[fingerprint])?

5. Answer ‘**yes**’ and press enter to the question above. You will then be asked to enter your password. Insert your **password** (your password will now show) and press **enter**. You are now logged in to the system. It will show something like the screenshot below (this example does not have a yes/no question because that only happens during your first time logging in):


---

>Part 3: Trying Some Commands

You can now try running some commands as you are already logged in! Here are some common useful commands that you can try:

```
* cd ~
* cd
* ls -lat
* ls -a
```

There are still many other commands that you can use, but these are just a few examples that we usually use. Take a look at what happens when you run the different commands. Here below is a screenshot of what I see when I run those commands on my account:


---

>Part 4: Moving files with scp

The most important thing in working remotely is to be able to copy your files back and forth between your computer and the remote computers. The scp command is useful to copy your files from your computer to a remote computer. Here is the command that you can use to copy your file to the remote computer, you can just change ‘filename.java’ to the name of the file you want to copy:
```
scp filename.java cs15lsp22zz@ieng6.ucsd.edu:~/
```
Don’t be shocked if you’re asked to enter a password, just enter the same password that you use for the ssh. After this, login back to your course-specific account using the ssh command which I have explained in **Part 2**. 

Run the *ls* command on the terminal and you will see the file you just previously copied if you run it correctly. Here below are screenshots of what I see when I copy a file called WhereAmI.java, and that I can run the javac and java commands once the file is copied:



---

>Part 5: Setting an SSH Key

An SSH key is useful so that you do not need to enter your password when you run the ssh or scp commands. Thus, making it more efficient and less time consuming. Here below are the commands or things that you should follow/see to set the SSH key:

***(on your computer)**
```
$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/<user-name>/.ssh/id_rsa): /Users/<user-name>/.ssh/id_rsa
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /Users/<user-name>/.ssh/id_rsa.
Your public key has been saved in /Users/<user-name>/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:jZaZH6fI8E2I1D35hnvGeBePQ4ELOf2Ge+G0XknoXp0 <user-name>@<system>.local
The key's randomart image is:
+---[RSA 3072]----+
|                 |
|       . . + .   |
|      . . B o .  |
|     . . B * +.. |
|      o S = *.B. |
|       = = O.*.*+|
|        + * *.BE+|
|           +.+.o |
|             ..  |
+----[SHA256]-----+
```
Two new files are created on your system; the private key ( id_rsa) and the public key ( id_rsa.pub), stored in the .ssh directory on your computer.
Now we need to copy the public key to the .ssh directory of your course-specific account on the server.
```
$ ssh cs15lsp22zzz@ieng6.ucsd.edu
<Enter your password>
```
***(now on server)**
```
$ mkdir .ssh
$ <logout>
```
***(back on your computer)**
```
$ scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zzz@ieng6.ucsd.edu:~/.ssh/authorized_keys
# You use your username and the path you saw in the command above
```

Once you complete these steps, you do not need to enter a password again when running ssh or scp commands, just like the screenshot below.

 ---

>Part 6: Optimizing Remote Running

Here are some hints on the commands that can make your remote running more efficient!
1. You can use semicolons to run multiple commands on the same line.
2. Press the up-arrow button to recall the last command.
3. You can add a command in quotes(“”) at the end of the ssh command to directly run it on the remote computer.

---

