# Analyze text using basic regular expressions


## Regular Expressions
| Character |                Definition                |  Example   |        Result         |
| :-------: | :--------------------------------------: | :--------: | :-------------------: |
|     ^     |            Start of a string             |    ^abc    |    abc, abcd, abc1    |
|     $     |             End of a string              |    abc$    |  abc, rasabc, 2aabc   |
|     .     |       Any character except newline       |    a.c     |     abc, acc, a1c     |
|           |                                          | Alteration |           a           |
|   {...}   | Explicit quantity of preceding character |   ab{2}c   |         abbc          |
|   [...]   |   Explicit set of characters to match    |   a[bB]c   |        abc,aBc        |
| [a-z0-9]  |   One lower case characters or number    | a[a-z0-9]c |        aac,a1c        |
|   (...)   |           Group of characters            |  (abc){2}  |        abcabc         |
|     *     | Null or more of the preceding characters |    a*bc    | bc, abc, aabc, aaaabc |
|     +     |  One or more of the preceding character  |    a+bc    |       abc, aabc       |
|     ?     |  Null or one of the preceding character  |    a?bc    |        bc, abc        |
|    ^$     |               Empty string               |            |                       |

* Not all regular expressions are supported by `grep`. As alternative can be used `egrep`