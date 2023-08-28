##### 1. Suppose, you wish to print a file "draft" with 60 lines on a page. What **command** would you use? 

The command for this purpose is 
```bash
pr -l60 draft
```

**NOTE:** The default page length for `pr` command is 66 line. The `-l` options specifies custom length 

##### 2. What is **LD_LIBRARY_PATH**?

`LD_LIBRARY_PATH` is an environment variable used for debugging a new library or a non-standard library. It is also used to identify the directories that need to be searched for; In order to do this, the path to search for the directories needs to be specified 

It can be set using following command 
```bash
setenv-LD_LIBRARY_PATH--$PATH
```

It is used to search for the shared objects/dynamic libraries by the operating system for extendable functionality at the runtime 

##### 3. 