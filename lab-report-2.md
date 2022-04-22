## Week 4 Lab Report 2 <br>
**Code Change 1**<br>
---

Image of code change:
![image](https://user-images.githubusercontent.com/99768694/164589639-52785807-4a86-4219-8bae-ebb49c23b6d1.png)
Link to test file with failure-inducing input:<br>
[File with failure-inducing input](https://github.com/brandonszeto/markdown-parser/blob/master/test-file.md)<br>
Symptom of failure-inducing input:<br>
![image](https://user-images.githubusercontent.com/99768694/164587751-d2097fbc-6660-40b0-b62c-2e8d9b4f02b8.png)<br>
2-3 sentence description:<br>
The while loop never broken because currentIndex is never greater than markdown.length(). As a result, 
a java.lang.OutofMemoryError: Java heap space is thrown. The failure-inducing input is a completely valid input,
and this is problem can be attributed to a bug in the getLinks() method.


**Code Change 2**<br>
---

**Code Change 3**<br>
---
