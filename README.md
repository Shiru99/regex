# Regular Expressions

### Some basic concepts : 

#### 1. Basic Tags 

    g : global
    i : insensitive (case insensitive)
    m : multiline (Causes ^ and $ to match the begin/end of each line (not only begin/end of string))
    e : extended (ignores whitespaces)

#### 2. Meta Characters

    /d : any digit [0-9]
    /w : word character [a-z,A-Z,0-9,_]
    /s : whitespace characters (space,tab,newline,etc)
    /t : only tab

#### 3. Special Characters 

     ?  : 0-or-one qunatifier (makes preceding char optional) 
     +  : 1-or-more qunatifier
     *  : 0-or-more qunatifier
     .  : any char other than newline
     \  : the escape char
    [ ] : character set
    [^] : negate symbol in character set

    special chars can be used as normal char by adding \ before them e.g. : abc\. => abc.

---

### Basics patterns : (Java)

```
1.  "game"gm                - matches all "game"
2.  "[gl]ame"gm             - matches all "game or lame"                //  [g or l]
3.  "[^gl]ame"gm            - matches all other than "game or lame"     //  not [g or l]
4.  "[a-h]ame"gm            - [abcdefgh]ame
5.  "[a-zA-Z0-9]ame"gm      - [(a to z) OR (A to Z) OR (0 to 9)]ame
6.  "[0-9]+"gm              - matches everything with min 1 char bet. (0 to 9)
7.  "[0-9]{10}"gm           - matches all 10 digit numbers
8.  "[0-9]{10,13}"gm        - matches all 10-13 digit numbers
9.  "[0-9]{10,}"gm          - matches all numbers with min. 10 digit numbers
10.  "\d\s\w\t"gm           - matches all "digit + whitespace + character + tab"

11.  ".+"gm                 - matches non-empty string
12.  "car.?"gm              - matches car or (car + any char)
13.  "^[0-9]"gm             - matches starting with 0-9
14.  "[0-9]$"gm             - matches ending with 0-9
15.  "^[a-z]{5}$"igm        - matches 5-lenth strings only : '^' : starting of string) & '$' : end of string
16.  "^(A||non-)sense$"igm  - matches sense or non-sense or Asense
```