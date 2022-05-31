[My markdown-parse Repository](https://github.com/dwengxz/markdown-parser)

[Their markdown-parse Repository](https://github.com/nidhidhamnani/markdown-parser)

## The Test Implementation of Each Snippet
![Image](https://dwengxz.github.io/cse15l-lab-reports/test.PNG)

## The Results of Running Each Test:

**My Implementation**

![Image](https://dwengxz.github.io/cse15l-lab-reports/myimplementation.PNG)


**Their Implementation**

![Image](https://dwengxz.github.io/cse15l-lab-reports/theirimplementation.PNG)

## Can these test failures be fixed easily?

### Test Snippet 1
```
I believe snippet 1 cannot be fixed with a small code change. My current implementation fails, 
as it is unable to differentiate brackets within backticks and brackets outside of backticks. To
fix this, I would need to create a new method, that, when a backtick is encountered, finds the
location of the next backtick. Using the location of the second backtick, we can compare that with 
the location of a second bracket; if a brackets location is smaller than the backtick, we then ignore
that given markdown link.
```
### Test Snippet 2
```
I believe snippet 2 can be fixed with a small code change. We can simply add a line of code to ignore
any brackets that immediately follow a '/'.
```
### Test Snippet 3
```
I believe snippet 3 can be fixed with a small code change. We can simply add a small method that checks
for newlines within brackets or parentheses. If two or more newlines are encountered in succession within
a pair of brackets or parentheses, we can ignore that given markdown link.
```
