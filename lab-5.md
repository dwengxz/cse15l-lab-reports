## Finding Mismatched Results

After running both my implementation and the provided implementation of MarkdownParser.java,
I manually compared the results of both implementations and noted any discrepencies.
From this method, I chose two tests that produced mismatched results:
[**Test 498**](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/498.md) and [**Test 573**](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/573.md)

![Image](https://dwengxz.github.io/cse15l-lab-reports/test498.PNG)

*Results of Test 498; Left is the provided implementation, Right is my implementation.*

**Both implementations are wrong**.
The provided implementation printed `[]`
My implementation printed `[<foo(and(bar]`
The expected print is `[foo(and(bar)]`

![Image](https://dwengxz.github.io/cse15l-lab-reports/test573.PNG)

*Results of Test 573; Left is the provided implementation, Right is my implementation.*

**The provided implementation is wrong**
The provided implementation printed `[/url]`
My implementation printed `[]`
The expected print is `[]`

## Solutions

In test 498, my implementation stopped printing from the first closing parentheses it found, rather
than from the final closing parentheses in the line. To fix this, we can change the search for the
closing parenthesis in highlighted section below to instead search for a closing parenthesis that is 
followed by a space. 

![Image](https://dwengxz.github.io/cse15l-lab-reports/section498.PNG)

In test 573, the provided implementation printed an extra section it should not have, as it still
does not check whether the link it is reading is actually supposed to be a link, or an image. To
fix this, we can add a new check in the highlighted section, to check whether the first closed
parenthesis is proceeded by an exclamation mark. If it is, we shopuld not print the proceeding
link. 

![Image](https://dwengxz.github.io/cse15l-lab-reports/section573.PNG)
