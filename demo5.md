# Docker volume on Windows

1. Switch to Windows container mode

2. Run following commands to create new Named volume

```
$ docker volume create vol101
$ docker volume inspect vol101  
```

3. Launch a new Win Container with CMD prompt

```
$ docker run --name w9 -it -v vol101:C:\apps mcr.microsoft.com/windows/nanoserver:1903 cmd    
$ cd apps
$ echo "Hello There!" > file1.txt
$ exit
```

4.  Open path C:\ProgramData\Docker\volumes\vol101\_data and check if it contains the file "file1.txt"

5.  Delete all

```
$ docker volume rm vol101
$ docker rm w9
$ docker volume rm vol101
```