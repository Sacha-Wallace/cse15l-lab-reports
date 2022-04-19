# CSE 15L Lab Report 1
## Sacha Wallace

**How to Log On to a Course Specific Account on ieng6**

1. **Installing VSCode**

You must click this link, [Link](https://code.visualstudio.com/), and follow the instructions within the installer. 

After, you should be able to open up to a screen like this.

[Image](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/LR-1.png)



2. **Remotely Connecting**

If you are on Windows you will need to install OpenSSH: 
[Link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)

Open a terminal window in VSCode, and type the command

`$ ssh *CourseSpecificAccount*@ieng6.ucsd.edu`

If any messages come up, just say yes and press enter. Then proceed to enter your password
You should end up getting an output similar to this, meaning you have successfully connected.

[Image]()

3. **Trying Some Commands**

Here is a cheat sheet with a list of basic terminal commands:

[Link](https://www.guru99.com/linux-commands-cheat-sheet.html)

You can try to mess around with a few of these commands.

Here you can see I used the ls command to help navigate as I created a folder, testfolder, and then proceeded to enter it and create a text file named testtext.txt.

[Image]()

4. **Moving Files With scp**

Scp is a command that will copy a file from a client to a remote computer. 

Once you have a file created on your computer and are logged out of the server, type

`$ Scp *FileName* *CourseSpecificAccount*@ieng6.ucsd.edu:~/`

After inputting your password, the file should be copied!

Here’s an example of the expected output in the console.

[Image]()

5. **Setting an SSH Key**

Setting an SSH key will allow you to run commands between the client and the server without having to type in your password every single time.

First type in:

`$ ssh-keygen`

And then when prompted to pick which file to save in type:

`/Users/*UserName*/.ssh/id_rsa`

Skip entering a password to the file, and now copy the public key to the server with the following commands:

```
$ ssh *CourseSpecificAccount*@ieng6.ucsd.edu

$ mkdir .ssh
```

Logout of the server, and then:

`$ scp /Users/*UserName*/.ssh/id_rsa.pub CourseSpecificAccount*@ieng6.ucsd.edu:~/.ssh/authorized_keys`

Now you should be able to use commands such as scp without having to enter your password like below!

[Image]()

6. **Optimizing Remote Running**

There are two little additional syntax tricks that will help when working in the terminal.

Adding quotes to the end of an ssh line will automatically log in and out of the server, while running the command in the quotes in between. 

Adding semicolons on a line will let you run multiple commands within the same line. 

For example, below I am disconnected from the server but I can run the ls command within quotes with the ssh command to view the contents of the main directory. 

[Image]()

