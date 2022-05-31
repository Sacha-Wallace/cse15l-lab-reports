# CSE 15L Lab Report 4
## Sacha Wallace

**Testing 3 Snippets in MarkdownParser**

1. **Snippet 1**

This is what Snippet 1's expected output looks like:

![LR4-1-1](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/LR4-1-1.png?raw=true)

This is the code to test whether the links are properly written in the snippet.

![LR4-1-2](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/LR4-1-2.png?raw=true)

The test fails, as per the output below:

![LR4-1-3](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/LR4-1-3.png?raw=true)

I was absent from the Week 7 lab so I will be unable to observe the tests on another implementation.

Yes there is a simple fix to be able to pass the test. On the first line in the snippet, the tick marks around the caption break the syntax and should be removed. 


2. **Snippet 2**

This is what Snippet 's expected output looks like:

![LR4-2-1](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/LR4-1-1.png?raw=true)

The code below tests if the link properly contains parentheses, as dictated by the caption in the snippet.

![LR4-2-2](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/LR4-1-2.png?raw=true)

The test passes.

The nested link doesn't work because markdown ignores the open bracket when it is looking for the closed bracket, so it would be a more involved change.

3. **Snippet 3**

This is what Snippet 3's expected output looks like:

![LR4-1-1](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/LR4-1-1.png?raw=true)

This is the code to test whether the links are properly titled within the snippet, even with the line breaks.

![LR4-1-2](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/LR4-1-2.png?raw=true)

The test fails, as per the output below:

![LR4-1-3](https://github.com/Sacha-Wallace/cse15l-lab-reports/blob/main/LR4-1-3.png?raw=true)

Yes there is a simple fix to be able to pass the test. On the first line in the snippet, the line break is the thing that messes up the syntax. If you remove the empty line, it'll run.


