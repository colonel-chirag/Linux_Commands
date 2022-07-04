# Linux_Commands
Introduction
Linux is a very famous, open-source operating system. Many developers use Linux for development purposes because of its high throughput. As a student or even a professional in the software industry, it is very essential to have knowledge of the Linux OS. Many programmers prefer Linux over Windows OS for development purposes due to a variety of reasons such as the security of the Linux Operating System is better than Windows, the Linux terminal is way superior to the windows command line in many ways, etc.

What is Linux and Why use it?

Before we jump into studying a lot of Linux commands, it is very important to address this question What is Linux and why is it preferred over Windows OS. Linux is an open-source operating system whose source code is available for modification and commercial and non-commercial distribution under the guidelines of the GNU General Public License.

Linux has a number of advantages over the Windows operating system and is used widely because of these advantages Below are a few listed:

The major advantage of the Linux Operating System is that it is a freely available open-source OS. This means that the source code of the Linux Operating System is available openly in the market (on the internet) and anyone can study it, modify it and even send it forward for commercial uses too. However, the major use case of it being an Open Source OS is the study of the Operating System itself. If anyone has to understand the Operating System as a core subject, it's working, and what are the things kept in mind while designing an operating system, you can simply look up the code of Linux OS and get a plethora of ideas.
Privacy and Security are very important for the users, especially nowadays, when hacking and other cyber malpractices have become so common. Linux maintains the privacy of the user and is a lot more secure than Windows OS. However, this does not mean that Linux is completely secured and can never be attacked. This simply means that it is more secure than Windows and it does not even require any antivirus software to be installed within it.
Linux Operating System is highly stable and does not hang or requires to be restarted again and again.
Linux is fast and easy to install and can be installed very easily from the internet.
Linux is network friendly.
So, now that we have a fair idea about the Linux Operating System and its advantages over the Windows OS, let us now move on to the Linux Cheat Sheet and study the Linux Commands.

Here, we have a cheat sheet prepared for you to refer to all the important Linux Commands with Examples.
Linux Commands Tutorial: Basics to Advanced
1. File and Directory CRUD Navigation Commands
CRUD stands for Create, Read, Update, and Delete. CRUD operations are said to be the basic operations on any file or directory or database. Even if you are not a Linux User, file and directory CRUD operations are something that you should be comfortable with.![image](https://user-images.githubusercontent.com/59536110/177052099-35167a46-8066-4a0e-929e-2d338087ca35.png)
![image](https://user-images.githubusercontent.com/59536110/177052326-21a68077-7a76-4eaf-add4-5276ca1d930b.png)
![image](https://user-images.githubusercontent.com/59536110/177052341-77c0ea0f-4759-425f-9971-e8cc577c1325.png)
![image](https://user-images.githubusercontent.com/59536110/177052362-0ad1bb2e-fb46-493a-a8e0-8e4d8c38368c.png)
![image](https://user-images.githubusercontent.com/59536110/177052399-d6a87e97-4fb7-4279-86ed-538f57955f83.png)
The diagram shows that there are 3 types of people accessing a file and they are:

User (u)
Group (g)
Others (o)
Also, the access that we want to give to each of them is of three types:

Read (r)
Write (w)
Execute (x)
So, each of them can have 0 or more out of these 3 permissions. Now let us understand the Linux commands that help us give these permissions to the files.
One important thing to note here is that before these 9 slots of the user, group and others (read, write and execute permissions), there is also one another slot. This slot is for special files. For instance, if you something as drwxr--r--, here ‘d’ shows that it is a directory of which you are viewing the permissions. Further, rwx means that the user has all the three permissions where as r-- means that the group has only read permission and the write and execute permissions are not there with the group. The same is the case for others (another r--).

The chmod Command:
Before we jump into the Linux file permission commands and see some examples, it is very important to understand this chmod command in detail first as understanding this command completely will clear the entire concept of file permission commands. The chmod command stands for “change-mode” which means that using this command, we can change the mode in which some user is able to access the file. This command is used to change the file permissions. The syntax can be either using symbols (characters) or numbers. We will see that in detail.

Symbolic Method for granting permissions:
This is the first method of chmod command using which we can give permissions. The basic syntax is as follows:

chmod [ugoa…][-+=]perms…[,....] FILE….

Let us understand this syntax in detail.

The first set means the type of person to give access to. Here:

u → Stands for User
g → Stands for Group
o → Stands for Others
a → Stands for All the users i.e. instead of writing ugo, we can just write a.
If the user's flag is not included in the command i.e. we do not mention for which kind of people out of u, g and o, are we changing the permissions for, by default, it takes a i.e. all the users.

The second set is the set of operators. Let us see what they mean.

- → removes the mentioned permission
+ → adds the mentioned permission
= → Changes the current permission to the mentioned permission. IF no permission is mentioned after using the = operator, all the permissions from the mentioned class are removed.
The perms stand for permission and ‘,’ is used to separate different permissions. Let us now see the Linux commands using the symbolic notation of chmod.


![image](https://user-images.githubusercontent.com/59536110/177052754-663fec2b-21d1-4ff4-af1d-808fc33447d2.png)
Numerical Method for granting file permissions
There are numeric codes for each permission. They are as follows:

r (read) = 4
w (write) = 2
x (execute) = 1
No permissions  = 0
The permissions number of a specific user class is represented by the sum of the values of all the permissions. For instance, if the user has read and executed permissions, but not the write permission, then the permissions number for the user will be read (4) + execute(1) = 5.

For instance, if we have to write a command to provide read and write permissions to the user, group and others, there can be many ways of doing so. Let us see one symbolic way:

Symbolic Way
$ chmod ugo+rw file1.txt

We can write this in a numeric way as shown below:

Numeric Way
$ chmod 666 file1.txt

Explanation: We have already studied that if we do not mention u/g/o then by default the permissions are applied to all. Also, read + write = 4 + 2  = 6. We have written 6 thrice because of applying the permissions to user, group and others. So, read and write permissions are applied to the user, group and others (666) for the file file1.txt.

![image](https://user-images.githubusercontent.com/59536110/177192202-7a5904ee-5d16-4ce8-9e0c-ea6c82847760.png)
![image](https://user-images.githubusercontent.com/59536110/177192532-82093e18-f48e-49d4-8798-fe81e32acb1f.png)
![image](https://user-images.githubusercontent.com/59536110/177192582-b9ccd8dc-8361-4bfe-891f-55c2f361888d.png)
![image](https://user-images.githubusercontent.com/59536110/177192630-9fb278a2-9de7-4f8f-b46e-dfcc7d0295e1.png)
![image](https://user-images.githubusercontent.com/59536110/177192682-9f696283-9fd1-4980-be1f-64a34f65e2b0.png)

