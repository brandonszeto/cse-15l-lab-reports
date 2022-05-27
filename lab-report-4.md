# Lab Report 4 <br>

Link to reviewed MarkdownParser repository:
https://github.com/mikayladalton2/markdown-parser

Link to personal MarkdownParser repository:
https://github.com/brandonszeto/markdown-parse 

---

## Expected Output of MarkdownParser: <br>

Snippet 1 Expected Output: ```[`google.com, google.com, ucsd.edu]``` <br>
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/169625893-b2894655-03c0-4929-b8ed-49e81b99ecd9.png" alt="image" width="1000"/>
</p>

Snippet 2 Expected Output: ```[a.com, a.com(()), example.com]```<br>
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/169625948-da7ab63d-1bee-4e1c-87b5-ab8e24f850ed.png" alt="image" width="1000"/>
</p>

Snippet 3 Expected Output: ```[https://www.twitter.com, https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule, https://cse.ucsd.edu/]```<br>
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/169625973-c59251c7-b643-4ba2-a8c0-b347c72eaa97.png" alt="image" width="1000"/>
</p>

## MarkdownParseTest.java Code Testing for Expected above input:<br>
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/169626289-1b96c216-bd7e-49ab-9fdf-df4ab90a8afb.png" alt="image" width="800"/>
</p>



## Reviewed Implementation of MarkdownParser:

<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/169626567-ce34f34e-a2f5-45fa-b47c-611659e71c55.png" alt="image" width="1000"/>
</p>

## Personal Implementation of MarkdownParser:

<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/169626620-15215e77-110b-4998-8322-6d83c68c49c5.png" alt="image" width="1000"/>
</p>

## Questions:

### Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change. <br>

- Yes. The code will look for pairs of backticks, and delete all characters, including the backticks. Then the code will run as usual. 

### Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change. <br>

- No. There is no easy way to differentiate parentheses, brackets, and escaped brackets from those that define a link. There will be a multitude of determing factors to check for within the code to determine whether a bracket or parentheses is not a part of a link which could include finding all pairs of brackets or parentheses.

### Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change. <br>

- Yes. There is simply an indexOutOfBoundsException() that my code is running into, which can be avoided by tracing the root of the error. However, I must consider how newlines affect the character count on Windows as opposed to Linux/MacOs based systems.
