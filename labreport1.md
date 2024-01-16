# LAB REPORT #1
---
## Using cd
1. Share an example of using the command with no arguments. \
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/78613d71-1e7c-4be3-bbd1-11549a15b180) 
* When the command was ran the working directory was the `/home` directory.
* Having no argument meant that I did not specify what directory I wanted to switch to. Therefore the output that I got was empty because I stayed in the directory I was in.
* The output is not an error because the directory was not changed and nothing was printed as expected.

2. Share an example of using the command with a path to a directory as an argument. \
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/4f1722ce-ab06-4eaf-841e-a349fc0a4513)
* When the command was ran the working directory was the `/home` directory which then switched to the '/home/lecture1` directory after it ran.
* The output was empty, however the prompt changed from `~` to `~/lecture1` indicating that I am now in the lecture1 directory because `cd` switched the current directory to the given path which in this case is lecture1.
* The output is not an error because the `cd` command worked as expected meaning it successfully changed the directory to the one in the argument.

3. Share an example of using the command with a path to a file as an argument. \
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/9ca058ca-9dc1-4d46-8fbf-4b3fd53f4f3d)
* When the command was ran the working directory was the `/home` directory.
* When using a file as an argument in this case the output was an error stating that the specified file in not located in the directory I was in.
* The output is an error because the file in my argument was not able to be located resulting in the `cd` command to fail.

---
## Using ls
1. Share an example of using the command with no arguments. \
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/f14c8e4a-97cc-4165-a204-7d45c2ce64ac) 
* When the command was ran the working directory was the `/home` directory.
* The `ls` command lists out the files and folders that are in the given path. Therefore the output I got was the only folder in `/home` which is the lecture1 folder because no argument regarding what path to be in was given.
* The output is not an error because the files and folder in the given path were successfully listed. 
  
2. Share an example of using the command with a path to a directory as an argument. \
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/416acdc4-2a3a-422e-b3fa-f60b09bf5458)
* When the command was ran the working directory was the `/home` directory.
* By using a directory as an argument, the output was a list of all the files and folders in the lecture1 path. This was the output since `ls` lists the files in the given path.
* The output is not an error because the files and folders in the lecture1 directory were listed as expected. 

3. Share an example of using the command with a path to a file as an argument. \
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/e8378825-f59b-4358-9d6c-d08977987007)
* When the command was ran the working directory was the `/home/lecture1/messages` directory because in order to use a file as an arguement I had to be in the directory where the file I want to use is in.
* The output I received was the name of the file I used in my argument which I did not expect since there are no files or folders in "es-mx.txt/"
* The output is an error because `ls` is suppose to list the files and folders in the given path but "es-mx.txt" does not have an files or folders in it.

---
## Using cat
1. Share an example of using the command with no arguments. \
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/55ab4994-c4fc-407a-bebe-0ac2e162623a)
* When the command was ran the working directory was the `/home` directory.
* Having no argument meant that I did not specify what content I wanted to be printed given by using paths. Therefore the output that I got was empty because I did not specify the file or files that I wanted the contents of to be printed.
* The output is not an error because the file was not specified therefore nothing can be printed and an empty output was expected. 

2. Share an example of using the command with a path to a directory as an argument. \
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/a76ba8bc-2606-484a-9439-582457a6fe88)
* When the command was ran the working directory was the `/home` directory.
* The `cat` command needs to be given a path in order to print the contents of one or more files. However 'lecture1' is a directory and not a path which is specified in the output.
* The output is an error because the `cat` command needs a path as an argument not a directory. Therefore having a directory as an argument causes `cat` to fail.

3. Share an example of using the command with a path to a file as an argument. \
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/c56c7e5e-62f0-4db8-a674-04116ade9cf7)
* When the command was ran the working directory was the `/home/lecture1` directory.
* The output is the content in the 'README' file which is located in the lecture1 directory. This is the output because `cat` prints the content in the 'README' file which is specified in the argument.
* The output is not an error because `cat` works as expected which is all the contents in the 'README' file printed into the terminal.

