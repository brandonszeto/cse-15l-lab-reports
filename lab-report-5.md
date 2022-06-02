# Lab Report 5 <br>

How I found tests with different results:<br>
Because I have a windows machine, the make and bash files were not running properly. As a result, I decided to manually run ```MarkdownParse.java``` with all the test files randomly ```1.md```. I did this for both files: my own and the implementation from lab 9. <br>
<br>

## First file with a difference: [Link to file 1](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/1.md) <br><br>

The expected output of this file should be ```[]```. <br>

Output of my ```MarkdownParse.java```:
![image](https://user-images.githubusercontent.com/99768694/171528488-a1fe37c6-7e1c-438b-85ac-f904e44b297c.png)

Output of Lab9 Implementation of ```MarkdownParse.java```:
![image](https://user-images.githubusercontent.com/99768694/171528537-2d706c9e-411c-4d6a-bb9e-f1b605df0ef5.png)

The Lab9 Implementation of ```MarkdownParse.java``` is correct, as it properly lists no files and returns the expected output (no files are found in ```1.md```). On the other hand, my implementation of ```MarkdownParse.java``` returns an index out of bounds exception. This is because my implementation of ```MarkdownParse.java``` generates links based on the existence of closed and open parentheses and closed and open brackets. Because I am only stopping the while loop once the index of the parentheses is found, the while loop will run indefinitely until the index that I am searching for is out of bounds.
<br><br>
What should be fixed (highlighted):
![image](https://user-images.githubusercontent.com/99768694/171534741-c3940074-a966-4825-b223-0ea8ca6324d6.png)


## Second file with a difference: [Link to file 2](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/510.md) <br><br>

The expected output of this file should be ```[/uri]```. <br>

Output of my ```MarkdownParse.java```:
![image](https://user-images.githubusercontent.com/99768694/171530721-153a78b4-f5eb-44eb-b88f-4ca020ecfb57.png)

Output of Lab9 Implementation of ```MarkdownParse.java```:
![image](https://user-images.githubusercontent.com/99768694/171530846-ffc2d28e-1c2a-4030-892a-d0bc1eae104a.png)

The Lab9 Implementation of ```MarkdownParse.java``` is correct, as it properly lists the text in the file format ```[]()```, which was ```[/uri]```. On the other hand, my implementation of ```MarkdownParse.java``` returns only ```[]```, as it did not detect that there was text. This is because my implementation of ```MarkdownParse.java``` does not add the link to the toReturn ArrayList() when there is a space in the text that it is searching. Because there was a space between [link] and (/uri), my implementation ignored the link to be added.
<br><br>
What should be fixed (highlighted):
![image](https://user-images.githubusercontent.com/99768694/171534588-82756036-c526-434a-9196-24c6c569fc4a.png)
