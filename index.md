---
layout: home
search_exclude: true
---
# Test Corrections

## Question 66

### Original Question:

In mathematics, a perfect number is a type of integer. The procedure IsPerfect (num) returns true if num is a perfect number and returns false otherwise.

The following program is intended to count and display the number of perfect numbers between the integers start and end, inclusive. Assume that start is less than end. The program does not work as intended.
~~~
Line 1:  currentNum 
 start

Line 2:  count 
 0

Line 3:  REPEAT UNTIL (currentNum > end)

Line 4:  {

Line 5:     count 
 count + 1

Line 6:     IF (IsPerfect (currentNum))

Line 7:     {

Line 8:        count 
 count + 1

Line 9:        currentNum 
 currentNum + 1

Line 10:    }

Line 11:    currentNum 
 currentNum + 1

Line 12: }

Line 13: DISPLAY (count)
~~~

Which two lines of code should be removed so that the program will work as intended?

### Chosen Answer:

Line 5 and Line 9

### Explanation:
Line 5 should be removed otherwise, count would go off twice in the case of a perfect number. But what's worse, is that count stands for the number of perfect numbers not the actual number. With this code, it would count every number and double every perfect number.(Line 5)

There are two redundant lines of increasing currentNum. If I don't remove one of them, in the case of the a perfect number, counter would go off twice.(Line 9)

### Correct Answer:

Line 5 (Correctly answered) and Line 9 (I got this wrong)

### Explanation of Correct Answer (College Board):

This line should be removed. The variable count should increase by 1 when currentNum is a perfect number, so it should only be incremented in the body of the IF statement. (Line 5)

This line should be removed. Every integer from start to end should be checked, so currentNum should only be incremented inside the loop but outside the body of the IF statement. (Line 9)

### Explanation of Why My Answer Was Wrong?

I removed the wrong line of currentNum, which caused the current num only to be updated if it was a perfect num.
---
## Question 67

### Original Question:
The procedure NumOccurrences is intended to count and return the number of times targetWord appears in the list wordList. The procedure does not work as intended.

For which of the following code segments will the call to NumOccurrences NOT return the intended value?
~~~
Procedure NumOccurences (wordList, targetWord):
count <-- 0
for EACH word IN wordList
    IF word = targetWord
       count <-- count + 1
return count
~~~

Which two lines of code should be removed so that the program will work as intended?

### Chosen Answer:
A
~~~
treeList <-- "birch", "maple, "birch"
numOccurences(treeList, "maple")
~~~
B
~~~
treeList <-- "birch", "maple, "oak"
numOccurences(treeList, "spruce")
~~~

### Explanation:
Since the program (accidently) resets the count for each word, we need to take advantage of it with side test cases. I picked A because if the word shows up twice count would not be able to record it (it resets every word so max is 1). I picked B beacuse it was a side test case so I thought it would cause an error (because it has no matching tree).

### Correct Answer + Explanation (College Board):

A
~~~
treeList <-- "birch", "maple, "birch"
numOccurences(treeList, "maple")
~~~
For this code segment, count is increased to 1 the first time "birch" is encountered in the list. However, count is reset to 0 when the code segment moves to the next list element. The last time "birch" is encountered in the list, count is again increased to 1, causing the procedure to return 1 instead of the intended result 2.
B
~~~
treeList <-- "birch", "maple, "oak"
numOccurences(treeList, "maple")
~~~
For this code segment, count is increased to 1 the first time "maple" is encountered in the list. However, count is reset to 0 when the code segment moves to the next list element. This causes the procedure to return 0 instead of the intended result 1

### Explanation of Why My Answer Was Wrong?
If spruce never shows up and count keeps resetting to 0, even if there is no spruce, the code will work. 
---

## Question 50

### Original Question:

Consider the following algorithms. Each algorithm operates on a list containing n elements, where n is a very large integer.

- I. An algorithm that accesses each element in the list twice
- II. An algorithm that accesses each element in the list n times
- III. An algorithm that accesses only the first 10 elements in the list, regardless of the size of the list

Which of the algorithms run in reasonable time?

### Chosen Answer:

II only

### Explanation:
The other test cases would take much longer than n assuming n is very long. Taking the first 10 numbers ensures short base time (even in long testcases).

### Correct Answer:

I, II, and III

### Explanation of Correct Answer (College Board):

For an algorithm to run in reasonable time, it must take a number of steps less than or equal to a polynomial function. Algorithm I accesses elements *2n* times (twice for each of n elements), which is considered reasonable time. Algorithm II accesses 
 elements *n^2* (n times for each of n elements), which is considered reasonable time. Algorithm III accesses 10 elements, which is considered reasonable time.

### Explanation of Why My Answer Was Wrong?

Reasonable run time is when the run time doesn't increase faster than a polynomial function of n. Ex: n^2 is reasonable but 2^n or n! is not.

---
# Reflection
What went well: The quiz went very well, I only got 3 questions incorrect. Howvever, I know I did guess on a couple questions or was not a hundred percent confident in some of my questions so I will review them later. I think I did a good job on most of the theory questions from this team teach period and last team teach period because I reviewed my notebooks and vocab written down. I also think that I did a pretty good job with vizualizations of the robot questions because I used the college board annoatate tool. The anotate tool worked really well for long questions, finding keywords, and vizualizing code. 
What to study more of: Restudy time complexity and code vizaulization (especially for errors)
What to do in the future: I think I will manaage time beteer because the test took me more than 2 hours (around 3 hours). This is bad because the AP exam is timed. Also, I did not do the assignment in 1 sittin which is also mad for the AP exam.


# Posts
