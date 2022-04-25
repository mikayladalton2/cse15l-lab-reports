# Lab Report 2

## Code Change 1

![Code Change Difference from Github](Code%20Change%201.png)



[Link to testfile that caused error](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-file.md)



![Symptom of failure inducing output](symptom%20of%20failure-inducing%20input%201.png)

Essentially, the file got stuck in an infinite loop because it was searching for the next index of `[` however there was none at the end of the file. So the bug was infinite loop. To resolve this issue, I had the loop finish at the last index of a `)` to ensure the loop would stop before it had to search for an element that wasn't there. I used the `lastIndexOf()` method to acheive this.



## Code Change 2



![Code Change Difference from Github](Code%20Change%202.png)



[Link to testfile that caused error](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-file.md)



![Symptom of failure inducing output](symptom%20of%20failure-inducing%20input%201.png)



Honestly, the only issue I could find with the original code was the issue I described in code change 1. And so, I worked out different ways to resolve this issue. I attempted to change the code in this way at first, however I quickly noticed this was not a good fix because although it fixed the issue of the continous loop, it resulted in an `IndexOutOfBoundsException` when there were no parenthesis in the file. 



## Code Change 3



![Code Change Difference from Github](Code%20Change%203.png)



[Link to testfile that caused error](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-file.md)



![Symptom of failure inducing output](symptom%20of%20failure-inducing%20input%201.png)



Going off of what I tried for code change 2, I realized I needed to account for any of the variables invoking the `indexOf()` because any has the possiblity to cause `IndexOutOfBoundsException`(if element not found 'indexOf()' will return -1). I also realized I need to check this before I add it to the `toReturn` variable. This code change resulted in all the test files to produce the intended result. 