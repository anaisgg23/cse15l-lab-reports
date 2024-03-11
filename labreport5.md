# LAB REPORT #5 Putting It All Together
---
## Part 1: Debugging Scenario
  
🤷‍♀️<span style="color:blue">Student:</span> Hey! I am currently trying to run my grade server using a githib student submission url to run my grader and I received output saying that the clone finished but there was also an error message saying "no source files" I have included a screenshot of the output and my grade class.
of my termianal output, my guess is there is some sort of bug in my Grade class but I don't know what it is.

![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/be3bfd60-4bb7-42cd-8117-b677083535d1)

![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/08ae19b0-f219-4953-9b1b-2e8441dcb4ff)

🧑‍💻<span style="color:blue">TA:</span> Hello, it looks like you are specifically running the Grade class in you grade server so there is probably a bug somewhere in that file. Comparing your output and your grade class, we can see that the error is happing after "Finished cloning" is printed because there is no problem with that line in your output. "Error: no source file" is a problem with your javac command, why don't you try to print out the commands, you can do this by adding r += Arrays.toString(cmd) + "\n" in the for loop that is in your grade class.

🤷‍♀️<span style="color:blue">Student:</span> Thank you so much for your help! This is what I discovered from printing out the commands. I was able to see that the bug in my code was there was a missing space before the * in *.java because before CPATH and *.java were not seperate and instead were concatenated together.

![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/d2199e0c-e5a0-4020-84e8-d71e9afee052)

**All the information needed for setup:**
1. File and directory structure:
```
list-example-grader/
  lib/
    hamcrest-core-1.3.jar
    junit-4.13.2.jar
  GradeServer.java
  Server.java
  TestListExamples.java
  grade.sh
```

2. Contents before fixing bug:
```
class Grade {
  static String grade(String repo) throws IOException {
  String CPATH = ".:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar";
  String r = "";
  String[][] cmds = {
  
    {"rm", "-rf", "student-submission"},
  
    {"git", "clone", repo, "student-submission"},
  
    {"echo", "Finished cloning"},
  
    {"cp", "student-submission/ListExamples.java", "./"},
  
    {"bash", "-c", "javac -cp " + CPATH + "*.java"},
  
    {"java", "-cp", CPATH, "org.junit.runner.JUnitCore", "TestListExamples"}
  };
  for (String[] cmd: cmds) {
    r += ExecHelpers.exec(cmd);
  }
  return r;
}
  public static void main(String[] args) throws IOException {
    System.out.println(grade(args[0]));
  }
}
```

3. Command ran that triggered the bug:
```
$ java Grade "https://github.com/ucsd-cse15l-f22/list-methods-lab3"
```

4. Desciption of what to edit to fix the bug:
* In order to fix the bug, there needs to be a space added before "*.java" in the line that contains "bash" because if there is no space, CPATH and *.java are being concatenated together and we need them to be separated when compiling.
 
---
## Part 2: Reflection
