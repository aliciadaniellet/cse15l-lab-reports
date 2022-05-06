# Topic: Tips and Tricks
## '3 Cool Tips and Tricks that Might Help You Out in the Future'

---
> ## Number 1:  Streamline ssh Configuration

The *.ssh/config* is a configuration file which can tell **ssh** what username to be used when logging in to specific servers. Here in my example, I am trying to change the username to login to my **ssh** account to a simpler username called 'ieng6', instead of 'cs15lsp22zz@ucsd.edu'.\
\
My *.ssh/config* file to change the username:

![Image](https://user-images.githubusercontent.com/86458122/167041062-35624501-41aa-4096-bcdb-7940c26b4a5e.png)


Logging in to the remote server just by typing the command line **ssh ieng6**:

![Image](https://user-images.githubusercontent.com/86458122/167041067-c8072ef9-507e-44a5-b0dc-d5c8d795a4c0.png)


This is an scp command that I successfully run to copy a file called *WhereAmI.java* to the remote server just by using the new username **ieng6**.

![Image](https://user-images.githubusercontent.com/86458122/167041059-9ac3bbd9-dd3c-44fc-8612-e9263e5ea91c.png)


---

> ## Number 2: Setup Github Access from ieng6

Location where I store my **public key** in Github:

![Image](https://user-images.githubusercontent.com/86458122/167042513-3dda8e3d-06b1-4cf7-82bc-1f560984c406.png)

Location of where I store my **public key** in my user account:
(You can see that I have two public keys in this case as public keys always ends with *.pub*)

![Image](https://user-images.githubusercontent.com/86458122/167042525-15093403-8ff7-4279-b7c9-261c619eae4f.png)

Location of where I store my **private key** in my user account:
(You can see that I have two key-pairs public/private keys in this case as private keys is similar to the public key but without *.pub*)

![Image](<https://user-images.githubusercontent.com/86458122/167042576-a1fb920f-ccc6-4ba6-97c6-422f1b5a680d.png)

Git commands to commit and push a change while logged into my ieng6 account:
(In this case, I am trying to make a new file calles a.txt)

![Image](https://user-images.githubusercontent.com/86458122/167042812-9cceb4c0-ac3f-4a7e-9a53-304d5c86cfe0.png)

[Link](https://github.com/aliciadaniellet/SkillDemoOne/commit/36e879ab23fd2fb3fb8cfd4b6b3b2995d22bfd78) to see the resulting commit!

---

> ## Number 3: Copy whole directories with scp -r

Copying my whole markdown-parse directory to my ieng6 account:

![Image](https://user-images.githubusercontent.com/86458122/167042570-1c09dacb-2736-4fea-b6cf-ac12bef643c9.png)


Logging in to my ieng6 account to compile and run tests from my repository:

![Image](https://user-images.githubusercontent.com/86458122/167042807-6438daf9-5e0f-4771-a1ec-43d2dd86af6f.png)


Copying the whole directory and running the tests in just using one line: 

![Image](https://user-images.githubusercontent.com/86458122/167044869-79cd5b70-6bcb-4a76-a1c2-fdc52d0c0eb7.png)
