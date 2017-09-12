# myProject
Use the makefile to compile the c++ file and run the test with googleTest.

Follow the steps to complete settings. You need to setup the compile environment on your PC to run the project with test, and add webhook that can trigger CI server to do the building and running.

## 1. How to set up everything on your PC

#### Prerequisites

* [Windows 10](https://blog.gtwang.org/windows/how-to-get-ubuntu-and-bash-running-on-windows-10/)

### Install GoogleTest in different platforms

* [Windows 10 / Ubuntu](https://www.eriksmistad.no/getting-started-with-google-test-on-ubuntu/)
* [Mac](https://gist.github.com/massenz/41bb2c8375294f4d9927)
* [Windows 7](https://github.com/iat-cener/tonatiuh/wiki/Installing-Google-Test-For-Windows)

### Running the tests
```shell
cd <your/project/path>
make
./exp
```

After run the exp file, you should get the result like that: 
![Imgur](https://i.imgur.com/BEPHs86.png)


## 2. How to set up everything for CI server

You already have an account on [the CI server](http://140.124.181.114:8080/). 
Username and password is your student id, so your need to reset password first.
![Imgur](https://i.imgur.com/GoYBxXp.png)

### Need a new repository
https://github.com/new

Place this project to your own repository. Be careful not to overwrite the .git folder.

### Add WebHook to repository

On repository page -> Settings -> Webhooks -> Add webhook -> set Payload URL :
```
http://140.124.181.114:8080/buildByToken/build?job=<studentId>&token=<studentId>
```
And it should show the green tick.

![Imgur](https://i.imgur.com/wbjjetV.png)

### Email your repository url to TA
Email to posd2017f@gmail.com. Just need subject, no content required.

```
Subject: <studentId>, <repositoryURL>
```
![Imgur](https://i.imgur.com/dEkZk1Q.png)


### After email
Wait TA for setting, your CI job will be triggered to run test after every push.

## Done

If you have some problems that u really don't know why and how to solve it, email us: posd2017f@gmail.com or come to 1321 in office hours (Fri. 2pm to 4pm).
