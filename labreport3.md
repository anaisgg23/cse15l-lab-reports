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
**... all the files in `/technical` (way too many to fit nicely in lab report so I cut it down)**
```
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
**3: find -empty**
**4: find -ipath**
**find -mtime**
Citation: [https://opensource.com/downloads/linux-find-cheat-sheet?intcmp=701f20000012ngPAAQ]
