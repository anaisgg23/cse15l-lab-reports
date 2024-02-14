# LAB REPORT #3 Bugs and Commands
---
## Part 1
The bug that I have chosen from week 4's lab is the `reversed` method in `ArrayExamples.java`

**Failure-inducing input for the buggy program:**
```
@Test
  public void testReversed() {
    int[] input1 = {9,23,4};
    assertArrayEquals(new int[]{4,23,9}, ArrayExamples.reversed(input1));
  }
```

**An input that doesn't induce a failure**
```
@Test
  public void testReversed() {
    int[] input1 = {0,0,0,0,0};
    assertArrayEquals(new int[]{0,0,0,0,0}, ArrayExamples.reversed(input1));
  }
```

**The symptom, as the output of running the tests**
Output with failing-inducing input:
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/45677411-a1c8-4ff6-8c99-45004bfca206)

Output with input that doesn't induce a failure:
![image](https://github.com/anaisgg23/cse15l-lab-reports/assets/156368955/56b55dab-5502-46ce-ad64-ec4bf9731a65)

**The bug, as the before-and-after code change required to fix it**

Code before:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```
Code after:
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
