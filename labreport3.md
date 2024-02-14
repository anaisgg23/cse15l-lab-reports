# LAB REPORT #3 Bugs and Commands
---
## Part 1
The bug that I have chosen from week 4's lab is the `reversed` method in `ArrayExamples.java`

**1. Failure-inducing input for the buggy program:**
```
@Test
  public void testReversed() {
    int[] input1 = {9,23,4};
    assertArrayEquals(new int[]{4,23,9}, ArrayExamples.reversed(input1));
  }
```

**2. An input that doesn't induce a failure**
```
@Test
  public void testReversed() {
    int[] input1 = {0,0,0,0,0};
    assertArrayEquals(new int[]{0,0,0,0,0}, ArrayExamples.reversed(input1));
  }
```

**3. The symptom, as the output of running the tests**

**Output with failing-inducing input:**

![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/45677411-a1c8-4ff6-8c99-45004bfca206)

**Output with input that doesn't induce a failure:**

![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/56b55dab-5502-46ce-ad64-ec4bf9731a65)


**4. The bug, as the before-and-after code change required to fix it**

**Code before:**
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
**Code after:**
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```
* This fix addresses the issue as before the for-loop was not changing newArray and instead was setting the original array to be equal to `newArray` which was all zeros. Now with the fix that I made, the for-loop changes the values of `newArray` to be the values of `arr` at reversed indices and returns `newArray` instead of `arr`.

---
## Part 2
The command that I have chosen is the `find` command

**1: find -name**

1. What this command is doing is finding all the `.txt files` that have `"chapter"` in them. This is useful for when I need to find files that contain a certain character or word in it.
```
anais@anais MINGW64 ~/OneDrive/Documents/GitHub/docsearch/technical (main)
$ find -name "chapter*.txt"
./911report/chapter-1.txt
./911report/chapter-10.txt
./911report/chapter-11.txt
./911report/chapter-12.txt
./911report/chapter-13.1.txt
./911report/chapter-13.2.txt
./911report/chapter-13.3.txt
./911report/chapter-13.4.txt
./911report/chapter-13.5.txt
./911report/chapter-2.txt
./911report/chapter-3.txt
./911report/chapter-5.txt
./911report/chapter-6.txt
./911report/chapter-7.txt
./911report/chapter-8.txt
./911report/chapter-9.txt
```

2. What this command is doing is finding all the `.txt files` that have `"1471-2202"` in them. This is useful for when I need to find files that contain a certain character or word in it or in this case a specific number sequence. 
```
anais@anais MINGW64 ~/OneDrive/Documents/GitHub/docsearch/technical (main)
$ find -name "1471-2202*.txt"
./biomed/1471-2202-1-1.txt
./biomed/1471-2202-2-1.txt
./biomed/1471-2202-2-10.txt
./biomed/1471-2202-2-12.txt
./biomed/1471-2202-2-14.txt
./biomed/1471-2202-2-15.txt
./biomed/1471-2202-2-16.txt
./biomed/1471-2202-2-17.txt
./biomed/1471-2202-2-18.txt
./biomed/1471-2202-2-19.txt
./biomed/1471-2202-2-2.txt
./biomed/1471-2202-2-20.txt
./biomed/1471-2202-2-3.txt
./biomed/1471-2202-2-5.txt
./biomed/1471-2202-2-6.txt
./biomed/1471-2202-2-7.txt
./biomed/1471-2202-2-8.txt
./biomed/1471-2202-2-9.txt
./biomed/1471-2202-3-1.txt
./biomed/1471-2202-3-10.txt
./biomed/1471-2202-3-11.txt
./biomed/1471-2202-3-14.txt
./biomed/1471-2202-3-16.txt
./biomed/1471-2202-3-17.txt
./biomed/1471-2202-3-19.txt
./biomed/1471-2202-3-20.txt
./biomed/1471-2202-3-3.txt
./biomed/1471-2202-3-4.txt
./biomed/1471-2202-3-5.txt
./biomed/1471-2202-3-7.txt
./biomed/1471-2202-3-8.txt
./biomed/1471-2202-4-10.txt
./biomed/1471-2202-4-11.txt
./biomed/1471-2202-4-12.txt
./biomed/1471-2202-4-16.txt
./biomed/1471-2202-4-17.txt
./biomed/1471-2202-4-2.txt
./biomed/1471-2202-4-3.txt
./biomed/1471-2202-4-5.txt
./biomed/1471-2202-4-6.txt
```
Citation: [https://www.computerhope.com/unix/ufind.htm]

**2: find -type**

1. What this command is doing is returning all the files in `/technical` since I did the command `-type f` and f stands for "file". This is useful for when I need to find all the files in my program.
```
anais@anais MINGW64 ~/OneDrive/Documents/GitHub/docsearch/technical (main)
$ find -type f

./biomed/1471-2334-2-6.txt
./biomed/1471-2334-2-7.txt
./biomed/1471-2334-3-10.txt
./biomed/1471-2334-3-11.txt
./biomed/1471-2334-3-12.txt
./biomed/1471-2334-3-13.txt
./biomed/1471-2334-3-15.txt
./biomed/1471-2334-3-9.txt
./biomed/1471-2350-2-11.txt
./biomed/1471-2350-2-12.txt
./biomed/1471-2350-2-2.txt
./biomed/1471-2350-2-8.txt
./biomed/1471-2350-3-1.txt
./biomed/1471-2350-3-12.txt
./biomed/1471-2350-3-7.txt
./biomed/1471-2350-3-9.txt
./biomed/1471-2350-4-2.txt
./biomed/1471-2350-4-3.txt
./biomed/1471-2350-4-4.txt
./biomed/1471-2350-4-6.txt
./biomed/1471-2369-3-1.txt
./biomed/1471-2369-3-10.txt
./biomed/1471-2369-3-6.txt
./biomed/1471-2369-3-9.txt
./biomed/1471-2369-4-1.txt
./biomed/1471-2369-4-5.txt
./biomed/1471-2377-1-2.txt
./biomed/1471-2377-2-4.txt
./biomed/1471-2377-2-6.txt
./biomed/1471-2377-3-4.txt
./biomed/1471-2407-1-13.txt
./biomed/1471-2407-1-15.txt
./biomed/1471-2407-1-19.txt
./biomed/1471-2407-1-6.txt
./biomed/1471-2407-2-11.txt
./biomed/1471-2407-2-12.txt
./biomed/1471-2407-2-15.txt
./biomed/1471-2407-2-16.txt
./biomed/1471-2407-2-17.txt
./biomed/1471-2407-2-18.txt
./biomed/1471-2407-2-19.txt
./biomed/1471-2407-2-22.txt
./biomed/1471-2407-2-23.txt
./biomed/1471-2407-2-3.txt
./biomed/1471-2407-2-31.txt
./biomed/1471-2407-2-33.txt
./biomed/1471-2407-2-8.txt
./biomed/1471-2407-2-9.txt
./biomed/1471-2407-3-14.txt
./biomed/1471-2407-3-15.txt
./biomed/1471-2407-3-16.txt
./biomed/1471-2407-3-18.txt
./biomed/1471-2407-3-3.txt
./biomed/1471-2407-3-4.txt
./biomed/1471-2407-3-5.txt
./biomed/1471-2415-3-1.txt
./biomed/1471-2415-3-3.txt
./biomed/1471-2415-3-4.txt
./biomed/1471-2415-3-5.txt
./biomed/1471-2431-2-1.txt
./biomed/1471-2431-2-11.txt
./biomed/1471-2431-2-12.txt
./biomed/1471-2431-2-4.txt
./biomed/1471-2431-3-3.txt
./biomed/1471-2431-3-4.txt
./biomed/1471-2431-3-5.txt
./biomed/1471-2431-3-6.txt
... all the files in /technical (way too many to fit nicely in lab report so I cut it down)
```

2. What this command is doing is returning all the directories in `/technical` since I did the command `-type d` and d stands for "directories". This is useful for when I need to find all the directories in my program.
```
anais@anais MINGW64 ~/OneDrive/Documents/GitHub/docsearch/technical (main)
$ find -type d
.
./911report
./biomed
./government
./government/About_LSC
./government/Alcohol_Problems
./government/Env_Prot_Agen
./government/Gen_Account_Office
./government/Media
./government/Post_Rate_Comm
./plos
```
Citation: [https://www.youtube.com/watch?v=skTiK_6DdqU]

**3: find -empty**

1. What this command is doing is returning all the files and the directory in `/technical` that are empty. This is useful for when I need to find any empty files that exist in my program.
```
anais@anais MINGW64 ~/OneDrive/Documents/GitHub/docsearch/technical (main)
$ find -empty
```

2. What this command is doing is returning all the files and the directory in `/technical` that are empty. To show how `-empty` works since there is originally no empty files in `/technical`, I created an empty file inside the `911report` folder in the `/technical` directory to see if it returned the empty file and it did as seen below. This is useful for when I need to find any empty files that exist in my program.
```
anais@anais MINGW64 ~/OneDrive/Documents/GitHub/docsearch/technical (main)
$ find -empty
./911report/emptyFile
```

Citation: [https://www.redhat.com/sysadmin/linux-find-command]

**4: find -mtime**

1. What this command is doing is returning all the files `/technical` that have been modified in last 365 days/ in the last year. This is useful for when I need to find all the files that were modfied by a certain date in my program.
```
anais@anais MINGW64 ~/OneDrive/Documents/GitHub/docsearch/technical (main)
$ find -mtime -365
... all files modified within the last 365 days
(... way too many files to fit nicely in lab report so I cut it down)
./plos/pmed.0020082.txt
./plos/pmed.0020085.txt
./plos/pmed.0020086.txt
./plos/pmed.0020088.txt
./plos/pmed.0020090.txt
./plos/pmed.0020091.txt
./plos/pmed.0020094.txt
./plos/pmed.0020098.txt
./plos/pmed.0020099.txt
./plos/pmed.0020102.txt
./plos/pmed.0020103.txt
./plos/pmed.0020104.txt
./plos/pmed.0020113.txt
./plos/pmed.0020114.txt
./plos/pmed.0020115.txt
./plos/pmed.0020116.txt
./plos/pmed.0020117.txt
./plos/pmed.0020118.txt
./plos/pmed.0020120.txt
./plos/pmed.0020123.txt
./plos/pmed.0020140.txt
./plos/pmed.0020144.txt
./plos/pmed.0020145.txt
./plos/pmed.0020146.txt
./plos/pmed.0020148.txt
./plos/pmed.0020149.txt
./plos/pmed.0020150.txt
./plos/pmed.0020155.txt
./plos/pmed.0020157.txt
./plos/pmed.0020158.txt
./plos/pmed.0020160.txt
./plos/pmed.0020161.txt
./plos/pmed.0020162.txt
./plos/pmed.0020180.txt
./plos/pmed.0020181.txt
./plos/pmed.0020182.txt
./plos/pmed.0020187.txt
./plos/pmed.0020189.txt
./plos/pmed.0020191.txt
./plos/pmed.0020192.txt
./plos/pmed.0020194.txt
./plos/pmed.0020195.txt
./plos/pmed.0020196.txt
./plos/pmed.0020197.txt
./plos/pmed.0020198.txt
./plos/pmed.0020200.txt
./plos/pmed.0020201.txt
./plos/pmed.0020203.txt
./plos/pmed.0020206.txt
./plos/pmed.0020208.txt
./plos/pmed.0020209.txt
./plos/pmed.0020210.txt
./plos/pmed.0020212.txt
./plos/pmed.0020216.txt
./plos/pmed.0020226.txt
./plos/pmed.0020231.txt
./plos/pmed.0020232.txt
./plos/pmed.0020235.txt
./plos/pmed.0020236.txt
./plos/pmed.0020237.txt
./plos/pmed.0020238.txt
./plos/pmed.0020239.txt
./plos/pmed.0020242.txt
./plos/pmed.0020246.txt
./plos/pmed.0020247.txt
./plos/pmed.0020249.txt
./plos/pmed.0020257.txt
./plos/pmed.0020258.txt
./plos/pmed.0020268.txt
./plos/pmed.0020272.txt
./plos/pmed.0020273.txt
./plos/pmed.0020274.txt
./plos/pmed.0020275.txt
./plos/pmed.0020278.txt
./plos/pmed.0020281.txt
```

2. What this command is doing is returning all the files `/technical` that have been modified more than 10 days ago but no more than 20 days ago. This is useful for when I need to find all the files that were modfied by a certain time-line in my program. In this case no files have been modified more than 10 days ago but no more than 20 days ago so nothing is returned. 
```
anais@anais MINGW64 ~/OneDrive/Documents/GitHub/docsearch/technical (main)
$ find -mtime +10 -mtime -20
```
Citation: [https://opensource.com/downloads/linux-find-cheat-sheet?intcmp=701f20000012ngPAAQ]
