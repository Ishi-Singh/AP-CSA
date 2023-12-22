---
toc: true
comments: true
layout: post
title: Collegeboard 2015 Practice Exam MCQ
description: Corrections for the Tri 2 Quiz
type: tangibles
courses: { compsci: {week: 12} }
---

## Questions I Got Wrong

### 4

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/d38a23e2-6a30-4621-933d-81907d404c96)

The answer is not E because the expression ``if (val > maxVal)`` will evaluate to false when val and maxVal are the same which will not cause any problems when running the code. Since maxVal is initialized to a value that is greater than all values in arr, maxVal will never be updated and 0 will be returned.

### 6

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/14317b5a-e043-46e8-bcae-b3b35954edf0)

This piece of code is combinig all of the strings which will cause "rattrap" "similar" and "today" to combine and form "rattrapsimilartoday". The combination of "similar" and "today" will form the word "art" which will cause these words to retun True even though "art" is not in these words

### 9

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/06c69a6a-7c73-4acf-a599-457955a44e57)

I was initally confused on how a person can get the value 6 from this, we assumed that multiplying by 6 automatically floors the values and this means that 5.999 is the highest possible value. And the problem solves this by adding 2 which can be broken into 1+1 which can go to each random value and cause the largest possible value to be 6.999 which would floor to 6.

### 15

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/fe30bf7c-c0ad-4e22-ad01-4267b661bddc)

When I was intially doing this problem I was confused on whether it was A or B since I knew that only one number gets printed out. But the answer is A because this is recursion and nothing is printed until the 10th call.

### 19

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/991b3ac9-59b8-40d7-a6b1-67df337618a2)

I understand why it's I and II. In III the x vars will be set to 1,3,5,7,9 (it will loop 5 times) and since the x is being incrimented by 2 each pass the x % 2 value will always be odd making it so no output will show.

### 22

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/fbb51818-b6a5-43a2-9085-90c52431b153)

This question is a 2D array, and in A the outer for loop iterates over every row of numbers and assigns each row to the array row. The first for loop checks for length of the number of occurrences in the outer array. That is the outer array. That's 2 occurrences. First occurence 1,2,3. Second occurence 4,5,6. The 'c' variable is used for the outer array and this would print 1,2,3,4,5,6

### 24

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/40be9636-7cbb-468a-80ce-488bdc9c71f3)

I read this question wrong. The reason that II and III are the correct answers is because they are new methods with new signatures. In the case of I that method it's really a change to an existing method so programs that use this class need to be recompiled.

### 27

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/1a300e78-1dff-4f22-9c20-698b2873921f)

This is a selection sort algorithm, it looks for the smalllest value in the list and swaps it with the value at j. So when iterating it would give the following list:
1. {1, 3, 2, 5, 4, 6} <-- 1 and 6 are swapped
2. {1, 2, 3, 5, 4, 6} <-- 2 and 3 are swapped
3. {1, 2, 3, 5, 4, 6} <-- 3 and 3 are swapped

### 33

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/1e188b1b-bd36-4b4a-9724-b5d69f145905)

I understand why this is II and III. The code given in I sets max to Integer.MIN_VALUE then it accesses each element in arr and assigns them value. If value is greater than max, max is assigned value since it is now the largest value so far which means that a new max is given.

### 39

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/f5c6d19f-c5ad-44cf-a471-d3fa74fd7d5c)

It's supposed to be reversed. The first "for" block is doing two things at once first, it's setting each existing slot in the students array to "Alex". When calling the "set" method on the students list the element that previously existed at the specified index is returned. This is why the first output that you see is "Bob" when it's replaced with "Alex" and "Carl" when it's replaced with "Alex". And this makes it so that "Alex Bob Carl" is first output you will see from this line