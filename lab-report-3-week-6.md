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



2. **Setup Github Access from ieng6**



![LR-2](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/LR-2.png?raw=true)

3. **Copy whole directories with scp -r**



![LR-3](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/LR-3.png?raw=true)




`$ ssh-keygen`

And then when prompted to pick which file to save in type:

`/Users/*UserName*/.ssh/id_rsa`


```
$ ssh *CourseSpecificAccount*@ieng6.ucsd.edu

$ mkdir .ssh
```

Logout of the server, and then:

`$ scp /Users/*UserName*/.ssh/id_rsa.pub CourseSpecificAccount*@ieng6.ucsd.edu:~/.ssh/authorized_keys`


