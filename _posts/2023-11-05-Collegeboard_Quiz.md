---
toc: true
comments: true
layout: post
title: Collegeboard 2014 Practice Exam MCQ
description: Corrections for the Tri 1 final FRQ
type: tangibles
courses: { compsci: {week: 12} }
---

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/0f12f522-7a7d-4458-aefb-8dbc0e81115a)

## Questions I Got Wrong

### Q6

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/35496d79-ac9f-4193-a792-70d52babc3e6)

 To determine the positive distance between two values, we need to take the absolute value of the difference using Math.abs. Once the difference is calculated, the method should return true if this difference is less than or equal to the tolerance and false otherwise.

### Q7

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/48f585e2-867f-4818-925c-8cd326835258)

The setName method is non-static and must be called with the dot operator and an object of Person. It cannot be called with the class name, Person. To change the private instance variable myName, a call to the mutator method setName needs to be made. This non-static method is called using the dot operator and the name of the object, which is student, and passes the name we want to update myName to as a parameter.

### Q9

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/4b2a7fbd-6857-4655-9824-1f60d23eae84)

The element at index 0 will be excluded from the sum, since i starts at 1 instead of 0. When i is key.length an ArrayIndexOutOfBoundsException will be thrown.

### Q14

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/12580225-5a60-4991-b89f-bb6c76b735b3)

The access being used here is what would be used if myVehicles was an array instead of an ArrayList and v was an index of the myVehicles array. However, in this case an enhanced for loop is being used, which accesses the elements of myVehicles directly and assigns v the value of the elements.

### Q15

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/9116f7e7-6988-44db-a4d3-51289b2bef5b)

Choice III has a loop control variable k that starts at 0, increments by 1, and will terminate the loop when k has the value data.length – 1. In each iteration, there is a check to see if the current value is larger than the subsequent value. If it is, false is returned because elements would not be nondecreasing, otherwise true is returned. As a result, only data[0] and data[1] are examined. The remaining elements in data are not checked because the method will stop once a return statement is reached. This means that the method could return true even when there are consecutive elements in data that are nondecreasing.

### Q17

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/c4f974fa-c4ef-4fea-8710-275bb0fc25da)

The for loop control variable k starts with the value 3, is incremented by 1 and terminates the loop when its value is arr.length – 1. In the first iteration, when k is 3, arr[3] is assigned the value arr[4]. The contents of the arr have been updated to {1, 2, 3, 5, 5, 6, 7}. In the second iteration, when k is 4, arr[4] is assigned the value arr[5]. The contents of arr have been updated to {1, 2, 3, 5, 6, 6, 7}. In the third iteration, when k is 5, arr[5] is assigned the value arr[6]. The contents of arr have been updated to {1, 2, 3, 5, 6, 7, 7}. Then k is incremented to 6 and the loop terminates.

### Q19

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/038ace38-4272-457e-8842-381fbff01db4)

```By applying De Morgan’s Law to this expression, we negate the first expression !(!(a !=b)) and the second expression !(b >7) to form !(!(a != b)) || !(b > 7). In the first expression the two consecutive not operators (!) cancel each other out giving us (a != b). In the second expression, the opposite of > is <= giving us (b <= 7). The equivalent expression is (a != b) || (b <= 7).
```

### Q21

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/5c840074-2c5c-46b9-a0c0-bab7505c6127)

To find the value that is closet to val, the algorithm needs to calculate the positive difference between num and val.

### Q22

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/ff62c614-fdbe-41bd-b453-cd0a49efba47)

Since the books array has been declared of type Book, at compile time all objects stored in books are considered Book object regardless of their actual type. Therefore, any methods that are called on elements of books must be declared in Book. In order to call the pagesPerMinute() method on Book[0], we would need to use typecasting to let the compiler know that the object stored in the books array at this index is actually an AudioBook object.

### Q23

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/b70246de-b52a-4762-8bef-d50b43cb8f68)

This would be the correct answer if the remove occurred before the size was calculated in the statement animals.add(animals.size()-k, animals.remove(k)); and only one iteration of the loop occurred.

### Q25

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/e56043e8-44eb-4d98-9ae5-8653dddb511b)

Choice I provides the user access to the height, width, and depth of a box through the accessor methods getHeight, getWidth, and getDepth. This allows comparisons to be made in each of the three dimensions to determine if one box can fit inside another box.

### Q27

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/59771eeb-79eb-4cf6-bef2-39f40043a851)

x = 2 and y = 1 --> x = 3 and y = 2 --> x = 5 and y = 3 --> x = 8 and y = 5. The variable n is decremented by 1 and has the value 2. At this point the while loop terminates since n is no longer greater than 2 and the value 8 is returned.

### Q30

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/e3f006ea-bacd-4454-8d6c-1c96fd9371bd)

This would be the value if the second call to substring was word.substring(0, howFar + 1). The substring of “compiler” beginning at 3 + 1 or 4 and ending at 8 – 1 or 7. The value of word.substring(0, howFar) is “com”.

### Q32

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/3d99a510-9ca1-4452-9a92-50745bea935e)

Consider the example when n is assigned the value 2 and k is assigned the value 3. The for loop has a loop control variable i that starts at 1, increments by 1 and terminates when i is k + 1. Therefore, the loop iterates k times. During each iteration of the loop, answer, which was initialized to 1, is multiplied by n. In our example, that means answer is multiplied by 2, three times. Or answer is assigned 1 * 2 * 2 * 2, which is equivalent to 2 raised to the power 3.

### Q34

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/da7edb09-9334-4037-982a-2dd3253bcdfc)

Choice III uses the default Point constructor to assign center a new Point with x and y both equal to 0. It attempts to update x and y, however since they are private instance variables in Point, they are not able to be accessed directly in Circle. This code will cause a compile time error.

### Q35

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/b38ded04-75c3-4a7f-bf77-5243f619d80a)

The modulus operator (%) evaluates to the remainder when the first operand is divided by the second operand. For example, 2574 % 10 evaluates to 4 the remainder when 2574 is divided by 10. In the first iteration of the loop, result is assigned 0 * 10 + 2574 % 10 or 0 + 4 or 4. The value of num is updated to 257 since the division is integer division between two int values. In the second iteration, result is assigned 4 * 10 + 257 % 10 or 40 + 7 or 47 and num is assigned 25. In the third iteration, result is assigned 47 * 10 + 25 % 10 or 470 + 5 or 475 and num is assigned 2. In the fourth iteration, result is assigned 475 * 10 + 2 % 10 or 4750 + 2 or 4752 and num is assigned 0. At this point the loop will terminate and 4752 will be printed to the screen.

## Questions I Found Difficult

### Q1

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/cdc7e78d-2a2d-40f1-8736-c70feca61682)

The for loop sets the loop control variable k to 0 and then increments by 2, until k is greater than or equal to the length of the arr. When the method mystery is called with the actual parameter nums, arr is assigned a reference to the same array that is referenced by nums. During the loop the values of k are 0, 2, 4, 6 and when k has the value 8 the loop terminates since the length of arr is 7. Prior to the loop x is assigned 0 and then in the body of the loop, the value of arr at index k is added to x. In the first iteration of the loop when k has the value 0, nums[0] (which is 3) is added to the value of x and x is assigned 3. In the second iteration of the loop when k has the value 2, num[2] (which is 1) is added to the value of x and x is assigned 4. In the third iteration of the loop when k has the value 4, num[4] (which is 1) is added to the value of x and x is assigned 5. In the fourth iteration of the loop when k has the value 6,  num[6] (which is 2) is added to the value of x and x is assigned 7. The value 7 is returned from mystery(nums).

### Q13

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/a3bad8d9-5616-4a4c-9ff4-34ddd2e0e6f5)

k has the value 0, arr[0] is 7 which is greater than arr[1] which is 2, therefore 0 7 is printed. In the second iteration, k has the value 1, arr[1] is 2 which is not greater than arr[2] which is 5. Nothing is printed. In the third iteration, k has the value 2, arr[2] is 5 which is greater than arr[3] which is 3, therefore 2 5 is printed. In the fourth iteration, k has the value 3, arr[3] is 3 which is greater than arr[4] which is 0, therefore 3 3 is printed.  In the fifth iteration k has the value 4, arr[4] is 0 which is not greater than arr[5] which is 10. Nothing is printed. The value of k is incremented and has a value of 5, which is equal to arr.length – 1 and the loop terminates.

### Q16

![image](https://github.com/Ishi-Singh/AP-CSA/assets/82348259/fba4bccb-9f07-4052-967a-1ec4d7a941b1)

In the first for loop, all the values from a1 are copied over to result at corresponding indices. At this point, the elements at index 0 through a1.length – 1 are full. The first index where the first element of a2 should be copied into is a1.length. We can use the loop control variable k to access all the elements in a2 and k + a1.length to access the corresponding elements in result.