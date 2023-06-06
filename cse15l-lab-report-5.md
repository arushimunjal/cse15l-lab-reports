# Lab Report 5 - Debugging Scenario
Arushi Munjal, Lab B03

---

# Part 1: Student EdStem Post

![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/bf850e59-dd88-43a0-a24f-4b92291a1b1c)

![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/0ced687c-45d1-47d6-96b5-88ef90bec8f9)

![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/013fe218-e105-4324-8832-3748d3409a50)

![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/1475c975-2e6f-4a3e-98d9-0190e5239226)


# Part 2: TA Response

```

Hi, have you considered whether the elements are being properly swapped during the reverse operation? What happens to the values in the array when arr[i] is assigned arr[arr.length - i - 1] in each iteration?

I think you are on the right track, but should review whether all values of the array need to be swapped, or only a certain amount. Hint: if you swap the entire array, it will end in the original array.

```

# Part 3: New Student Output

New code:

![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/e63f8c10-8bde-4df4-8723-3e7b5747cf46)

New output:

![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/e64f3964-2e44-4bd6-a474-3be0688b0bb4)

```
The TA's response helped me understand that the previous code overwrites the original value at arr[i] without correctly reversing the elements, since the for loop traverses through the entire array. Instead, the loop should traverse to ensure that the swapping operation only occurs up to the midpoint of the array. Swapping elements beyond the middle point would result in reversing the elements back to their original order. Also, a temporary variable should be added to the code in order to hold the original value of arr[i] before swapping the elements.

```

# Part 4: SetUp Information

**File and Directory Stucture:

1. Directory: lab3
2. Java file: ArrayExamples.java and ArrayTests.java
3. Bash file: testArrayExamples.sh

**Contents of Each File Before Fixing the Bug:

1. ArrayExamples.java ![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/d4c40a31-f206-4b14-9879-b6e7ffd38433)

2. ArrayTests.java ![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/6b02426e-910b-4622-aa94-65b3217c117a)

3. testArrayExamples.sh ![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/e9948f5a-5cc6-456f-98f1-7bff456e1f20)


**Full Command Line to Trigger the Bug: `bash testArrayExamples.sh`

![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/76accf61-b41a-4622-b079-ca81b88e65e8)


**Description of the Bug and Solution:

The bug in this scenario is that the reverseInPlace method incorrectly assigns the values from the end of the array to each element in a sequential manner without preserving the original values. As a result, the array does not get reversed as intended. To fix the bug, you need to traverse only the first half of the array, rather than the entire array. Also, you must introduce a temporary variable to hold the original value of arr[i] before swapping the elements. This ensures that the original values are preserved during the reverse operation.

# Part 5: End of the Year Reflection

Thank you so much for holding a great quarter of CSE 15L. I learned so much throughout this course and believe I understand the necessary skills of bash, vim, debugging, and moving throughout my directories. I think the most valuable skill I learned what `cd` and `ls` because I now use them so often outside of this class, especially in CSE 12. I also found commands like `find` and `grep` to be very helpful, as they reduce my time searching for certain things and allow me to be a faster coder.
