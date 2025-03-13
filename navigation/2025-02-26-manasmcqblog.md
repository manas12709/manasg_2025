---
layout: post 
search_exclude: true
show_reading_time: false
permalink: /manasmcqblog
title: Manas's MCQ Blog
comments: true
categories: [Manas Final Retrospective]
---


# 2020 Practice Exam 1 MCQ Blog/Reflection

My score on this MCQ was a 62/67.

I completed this test on Sunday, 3/02 

I spent 1 hour 54 minutes on this test. The MCQ section of the AP test is 2 hours, and the increased stress/pressure that comes with the AP test, I am not happy with this time and I need to improve my speediness. 

 Below are a list of topics with respect to the number of questions on the test, and a percentage of my performance. For space and time purposes, I will display the topics where I failed to get 100% on.

![Final Score](https://github.com/user-attachments/assets/ce340ee0-e1de-40c4-9e7b-4f941973f11b)


| **Number** | **Name**                                  | **Topic** | **Skills** |
|------------|-------------------------------------------|-----------|------------|
| Q55        | Average height algorithm                  | 3.8       | 2.A        |
| Q50        | Reasonable time algorithms                | 3.17      | 1.D        |
| Q35        | Generalization of MaxTwo and MaxThree     | 3.13      | 3.C        |
| Q28        | Swap alpha and beta                       | 3.1       | 4.B        |
| Q16        | Word List Traversal                       |           |            |

# Q55 Average height algorithm
![Q55.png]({{site.baseurl}}/images/Sprint5/2020mccorrections/q55.png)

*Why Option A is Correct:*
Step 2 needs to establish the initial values for the algorithm to work properly. By having each person write their height at the top of the card and the number 1 at the bottom, we are:
- Tracking the sum of heights (top number)
- Tracking how many people's heights are included in that sum (bottom number)

*Why the Option I picked is Incorrect:*
Option C: "Each person writes the number 1 at the top of the card and writes their height, in centimeters, at the bottom of the card."
- This is incorrect because the top number needs to represent the sum of heights, not the count.

# Q50 Reasonable time algorithms
![Q50.png]({{site.baseurl}}/images/Sprint5/2020mccorrections/q50.png)

*Why Option D is Correct:*
All three algorithms run in reasonable time:
- Algorithm I accesses each element twice (2n)
- Algorithm II accesses each element n times (n^2)
- Algorithm III only accesses the first 10 elements (10)
- All of these are algebraically considered to run in reasonable time.

*Why the Option I picked is Incorrect:*
Option B: "III only"
- This is incorrect because algorithms I and II also run in reasonable time.

# Q35 Generalization of MaxTwo and MaxThree
![Q35.png]({{site.baseurl}}/images/Sprint5/2020mccorrections/q35.png)

*Why Option B is Correct:*
The `Max(numList)` procedure is a proper generalization of both `MaxTwo` and `MaxThree` because:
- It can handle any number of values, including exactly two or three
- It performs the same function (finding the maximum value) but generalizes to lists of any size
- The essential functionality of finding a maximum is preserved

*Why the Option I picked is Incorrect:*
Option C: "Procedure `MaxFour(w, x, y, z)`, which returns the greatest of its four integer parameters"
- This is incorrect because while it extends the concept to four parameters, it's not a true generalization. It's just another specific case rather than handling an arbitrary number of values.

# Q28 Swap alpha and beta
![Q28.png]({{site.baseurl}}/images/Sprint5/2020mccorrections/q28.png)

*Why Option B is Correct:*
To properly swap two variables, we need a temporary variable to hold one value while we overwrite it with the other. Looking at the code segments:

I (temp ← alpha, alpha ← beta, beta ← temp):
- Correctly saves alpha in temp
- Assigns beta's value to alpha
- Assigns the original value of alpha (saved in temp) to beta

III (temp ← beta, beta ← alpha, alpha ← temp):
- Correctly saves beta in temp
- Assigns alpha's value to beta
- Assigns the original value of beta (saved in temp) to alpha

Both I and III properly swap the values.

*Why the Option I picked is Incorrect:*
Option A: "I and II only"
- This is incorrect because II does not properly swap the values. In II, alpha's value is lost when beta is assigned alpha.
