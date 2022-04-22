## Week 4 Lab Report 2 <br>
**Code Change 1**<br>
---

Image of code change:<br>
![image](https://user-images.githubusercontent.com/99768694/164589639-52785807-4a86-4219-8bae-ebb49c23b6d1.png)<br><br>
Link to test file with failure-inducing input:<br>
[File with failure-inducing input](https://github.com/brandonszeto/markdown-parser/blob/master/test-file.md)<br><br>
Symptom of failure-inducing input:<br>
![image](https://user-images.githubusercontent.com/99768694/164587751-d2097fbc-6660-40b0-b62c-2e8d9b4f02b8.png)<br><br>
2-3 sentence description:<br>
The while loop never broken because currentIndex is never greater than markdown.length(). As a result, 
a java.lang.OutofMemoryError: Java heap space is thrown. The failure-inducing input is a completely valid input,
and this is problem can be attributed to a bug in the getLinks() method.


**Code Change 2**<br>
---

Image of code change:<br>
![image](https://user-images.githubusercontent.com/99768694/164593333-d34c3bd7-24ca-4ca4-b067-fd607e37f5f9.png)<br><br>
Link to test file with failure-inducing input:<br>
[File with failure-inducing input](https://github.com/brandonszeto/markdown-parser/blob/master/test-file2.md)<br><br>
Symptom of failure-inducing input:<br>
![image](https://user-images.githubusercontent.com/99768694/164590738-c023587b-0e5d-4903-8299-30fbaa2a8d57.png)<br><br>
2-3 sentence description:<br>
The code prints out image files, as image files in markdown use a similar format as links. The  failure-inducing input
is simply a file that includes images. As a result, the markdown string must be checked for an exclamation mark every 
loop to filter out images.

**Code Change 3**<br>
---

Image of code change:<br>
![image](https://user-images.githubusercontent.com/99768694/164593333-d34c3bd7-24ca-4ca4-b067-fd607e37f5f9.png)<br><br>
Link to test file with failure-inducing input:<br>
[File with failure-inducing input](https://github.com/brandonszeto/markdown-parser/blob/master/test-file2.md)<br><br>
Symptom of failure-inducing input:<br>
![image](https://user-images.githubusercontent.com/99768694/164594235-11ddbd14-2ac0-4cc0-ae7d-60d797a53156.png)<br><br>
2-3 sentence description:<br>
The code prints out empty image links. The failure-inducing input is simply a file that includes brackets and
parentheses that do not contain any content. As a result, before being added to the output, a string must be checked
for content.
