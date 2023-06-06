# Lab Report 2 - Debugging Scenario
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

# File and Directory Stucture:

Directory: lab3
Java file: ArrayExamples.java and ArrayTests.java
Bash file: testArrayExamples.sh


Contents of Each File Before Fixing the Bug:

Full Command Line to Trigger the Bug:

Description of the Bug and Solution:



