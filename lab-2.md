# **Code Change 1**
![Image](https://dwengxz.github.io/cse15l-lab-reports/chang1.PNG)
[Failure-inducing Input](https://github.com/dwengxz/markdown-parser/blob/main/test-file2.md)

![Image](https://dwengxz.github.io/cse15l-lab-reports/infiniteLoopCMD.PNG)

This change implements the secondary markdown link format to the markdown parser; now, links can be implemented with the format:
```
[Link][1]
[1]:<the-link>
```
The original markdown parser only had code to parse links in the form `[Link](<the-link>)`. Inputting the above test file would cause the code to forever search for a  non-existant char '(', which would result in a run-time error. 

---

# **Code Change 2**
![Image](https://dwengxz.github.io/cse15l-lab-reports/chang2.PNG)
[Failure-inducing Input](https://github.com/dwengxz/markdown-parser/blob/main/test-file3.md)

![Image](https://dwengxz.github.io/cse15l-lab-reports/infiniteLoopCMD.PNG)

The implementation of the second markdown link format resulted in a new infinite loop bug. Inputting a test file that ended with any characters other than a markdown link, such as the newline in the above inputted file, would cause the program to loop infinitely between different `[` indexs, as the variable `currentIndex` was unable to be larger than the size of the inputted file. 

---

# **Code Change 3**
![Image](https://dwengxz.github.io/cse15l-lab-reports/chang3.PNG)
[Failure-inducing Input](https://github.com/dwengxz/markdown-parser/blob/main/test-file.md)

![Image](https://dwengxz.github.io/cse15l-lab-reports/repeatedLine.PNG)

The implementation of the infinite-loop fix in Code Change 2 resulted in a new bug, where test files with more than one link, such as the test file above, would print out the first link in the file twice; once at the beginning, and once at the end. Code Change 2 added a new variable, `previousIndex`, which would keep track of the previous index of the loop. The code used this new variable to detect when the program had looped back to a previously registered link, and would terminate the loop. However, this detection was implemented at the end of the loop; so, one previously registed link would be re-inputted, and thus would be printed again. 
