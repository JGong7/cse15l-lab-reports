# Week 8 Lab Report: Markdown Snippets Testing
## By Jerry Gong

[My repository](https://github.com/JGong7/markdown-parse-1)

[Reviewed repository](https://github.com/sallada1/markdown-parse)

**Snippet 1**

The output of CommonMark Demo Site:
![image](4pic2.png)
According to the output above, the expected output of running MarkdownParse on this snippet should be **["`google.com", "google.com", "ucsd.edu"]**.

I turned the snippet into a test for both my program and the program I reviewed by writing the codes below.
![image](4pic4.png)

For my own implementation, the test failed.
![image](4pic11.png)

For the implementation I reviewed, the test failed as well.
![image](4pic6.png)

**Snippet 2**

The output of CommonMark Demo Site:
![image](4pic7.png)
According to the output above, the expected output of running MarkdownParse on this snippet should be **["a.com", "a.com(())", "example.com"]**.

I turned the snippet into a test for both my program and the program I reviewed by writing the codes below.
![image](4pic8.png)

For my own implementation, the test failed.
![image](4pic9.png)

For the implementation I reviewed, the test failed as well.
![image](4pic10.png)

**Snippet 3**

The output of CommonMark Demo Site:
![image](4pic12.png)
According to the output above, the expected output of running MarkdownParse on this snippet should be **["https://ucsd-cse15l-w22.github.io/"]**.

I turned the snippet into a test for both my program and the program I reviewed by writing the codes below.
![image](4pic15.png)

For my own implementation, the test seemed to run into a infinite loop and failed.
![image](4pic13.png)

For the implementation I reviewed, the test failed as well.
![image](4pic14.png)


**Answering Questions**

**Snippet 1**

I don't think a change below 10 lines will be able to make my program work for snippet 1 and other backticks related issues. That is because the fourth link in the snippet triggered another bug caused by a feature of my program. My program tends to check if the ending bracket is next to the open parenthesis to determine if it's a valid link, and since the fourth link has a backtick after the first bracket, the program will categorize it as an invalid link. Therefore, debugging this will require a more involved change than 10 lines of codes, as we'll need to reinvestigate our feature to check for ending bracket adjacent to open parenthesis.

**Snippet 2**

I think it is possible to fix the program to work for snippet 2 and similar issues. I can add an if statement to check if there's another closing bracket or parenthesis right after the first closing bracket or parenthesis. If yes, then nextCloseBracket or nextCloseParen should be set to the ones that appear last. That way, the entire contents within the bracket/parenthesis can be included. I think my code will be able to pass snippet 2 after the changes described above.

**Snippet 3**

I think it'll be hard to fix the program with 10 lines of code changes. The JUnit tests were not able to run, and it's likely caused by an infinite loop. I explored through my code, and the code was able to compile after I deleted an if-statement used to detect whitespace within parenthesis. However, it would throw an index-out-of-bounds exception. Therefore, this is not an easy issue to be solved within 10 lines of codes. After fixing the index-out-of-bounds exception, we'll even need to think about how to fix the code to give the right outpout. Overall, it will be a more involved change than 10 lines of codes.
