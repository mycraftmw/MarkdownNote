# 软件工程师的成长
&emsp;&emsp;我从小学开始接触电脑，但是高中之前的我基本都是停留在玩电脑游戏的层面上。高中之后我才接触到了OI，接触到了编程，这里不得不感谢我的母校南山中学给我提供的条件。当我抱着尝试的心态第一次使用Pascal语言写出一段可以画出一堆星星的程序时，我被她深深的迷住了。但我当时也没有想到我会在这条路上越走越远。

&emsp;&emsp;到了高考填报志愿的时候，我几乎没有任何其他想法的就选择了计算机这个专业。从此正式从一名OIer更新为一只程序猿。对比起做OI题时的用算法解决一些给定的问题的答案，在项目里解决实际问题更加让我喜欢和热爱计算机。

&emsp;&emsp;在之后的岁月中，我可能会读研或者去一家IT公司就业，继续 ***code the world***。
# 代码复审

## General
- Does the code work? Does it perform its intended function, the logic is correct etc.
    - Yes.
- Is all the code easily understood?
    - Yes.
- Does it conform to your agreed coding conventions? These will usually cover location of braces, variable and function names, line length, indentations, formatting, and comments.
    - Yes.
- Is there any redundant or duplicate code?
    - Yes.
- Is the code as modular as possible?
    - Yes.
- Can any global variables be replaced?
    - No.
- Is there any commented out code?
    - Yes.
- Do loops have a set length and correct termination conditions?
    - Yes.
- Can any of the code be replaced with library functions?
    - No.
- Can any logging or debugging code be removed?
    - No.

## Security
- Are all data inputs checked (for the correct type, length, format, and range) and encoded?
    - Yes.
- Where third-party utilities are used, are returning errors being caught?
    - No.
- Are output values checked and encoded?
    - No.
- Are invalid parameter values handled?
    - Yes.

## Documentation
- Do comments exist and describe the intent of the code?
    - No.
- Are all functions commented?
    - No.
- Is any unusual behavior or edge-case handling described?
    - Yes.
- Is the use and function of third-party libraries documented?
    - No.
- Are data structures and units of measurement explained?
    - No.
- Is there any incomplete code? If so, should it be removed or flagged with a suitable marker like ‘TODO’?
    - No.

## Testing
- Is the code testable? i.e. don’t add too many or hide dependencies, unable to initialize objects, test frameworks can use methods etc.
    - Yes.
- Do tests exist and are they comprehensive? i.e. has at least your agreed on code coverage.
    - No.
- Do unit tests actually test that the code is performing the intended functionality?
    - Yes.
- Are arrays checked for ‘out-of-bound’ errors?
    - No.
- Could any test code be replaced with the use of an existing API?
    - No.