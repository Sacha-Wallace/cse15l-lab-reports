# CSE 15L Lab Report 3
## Sacha Wallace

**Lab 5 Group Options**

1. **Streamlining ssh Configuration**

First we navigate over to the .ssh file, mine being located in the root directory. Within this file, if it doesn't exist, create a text file titled config. Then paste this text in using any text editor ( I used NotePad ), filling in your course account logon.


```

Host ieng6
    HostName ieng6.ucsd.edu
    User (use your username)

```

![1-1](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/1-1.png?raw=true)

Now we can just use the ssh command to easily connect to the server.

`$ssh ieng6`

![1-2](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/1-2.png?raw=true)

We can also use this trick in the scp command as shown below.

`scp filename ieng6:~/`

![1-3](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/1-3.png?raw=true)



2. **Setup Github Access from ieng6**

In the settings menu on Github there is a button to click which will add an ssh public key to your account.

![2-1](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/2-1.png?raw=true)

The private key is located on your local computer within the .ssh directory.

![2-2](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/2-2.png?raw=true)





3. **Copy whole directories with scp -r**

We can use the command scp-r to copy whole directories with one single line, replacing the file path.

`scp -r (filepath) ieng6:~/MarkdownParse`

![3-1](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/3-1.png?raw=true)

Now we can log into the ieng6 account, and compile and run the test on the server.


![3-2-1](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/3-2-1.png?raw=true)

![3-2-2](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/3-2-1.png?raw=true)

This can all be accomplished in one line using semicolons as shown below

```
$ scp -r ~/src/MarkdownParse ieng6:~/markdownAll; ssh ieng6; cd markdownAll; javac MarkdownParse.java; java MarkdownParse test-file.md

```

![3-3](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/3-3.png?raw=true)




