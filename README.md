# Javascript_tutorial
A guide for basics to intermediate Javascript

# defining variables
There are three keywords which helps us to define a container in memory to store the values we want:
1. **const** : if you define anything with const, the value inside that will be immutable if anyone tries to change it from somewhere else.
ex: const accountNumber: 123456
    accountNumber: 654321

    Error: Assignment to constant varibale
2. **let** : you can redefine the values within the scope of it.
ex: let userName= "shane02"
    userName= "shane_billy"
    console.log(userName)
    OUTPUT: userName: shane_billy
   
4. **var** : please forget that it exists. Use this carefully.
    it was used initially but because of the issues in block and functional scope, devs don't recommend using it. Suppose you have used a variable called 'state' in one file and assigned a value to it,
    there is one more dev who used 'state' and assigned it a different value. Now there will be inconsistency with the values beacuse with 'var' values are available globally.

    
# Some datatypes
The datatypes are characterized on the basis of memory they are using. The datatype that uses **Stack memory** and when it is called a **<i>copy</i>** of the variable is given, so the changes made in copy doesn't effect the 
original are called **primitve datatype**.
The datatype which use **heap memory** and its <i>**reference**</i> is given when called by program are **Non primitive datatypes**
* Primitive datatype : means the program will return a copy of the value to you for the operations
1. number -> ranging from min -(2^53 -1) and max 2^53 -1
2. string -> group of ascii characters
3. bigint
4. boolean -> true/false
5. symbol -> introduced in ES6 and used to add a unique property keys to an object
6. undefined -> undefined is a datatype
7. null -> itis a standalone value and its datatype is object
   
* Non Primitive datatype : the program will refer to the variable in the memory
  1. Array
  2. Object
  3. Functions

* Premitive Datatypes

                  Type                                   typeof

                 Number                                   number
                 String                                   string
                 Boolean                                  boolean
                 Bigint                                   bigint
                 Symbol                                   symbol
                 Null                                     object
                 undefined                                undefined


* Non-Premitive OR Referance OR Object datatype

                  Type                                   typeof
  
                  Array                                 object
                  Object                                object
                  Function                            function object

# Conversion of datatypes

* **Converting to Number** <br />
1. let score = "50" <br />
   let scoreConverted = Number(score) <br />
   console.log(scoreConverted) <br />
   OUTPUT : 50
2. let score = "50abc" <br />
   let scoreConverted = Number(score) <br />
   console.log(scoreConverted) <br />
   OUTPUT: NaN <br />
3. let score = "" <br />
   let scoreConverted = Number(score) <br />
   console.log(scoreConverted) <br />
   OUTPUT: 0 <br />
4. let score = true <br />
   let scoreConverted = Number(score) <br />
   console.log(scoreConverted); <br />
   OUTPUT: 1 <br />
5. let score = null <br />
   let scoreConverted = Number(score) <br />
   console.log(scoreConverted); <br />
   OUTPUT: 0 <br />
6. let score = undefined <br />
   let scoreConverted = Number(score) <br />
   console.log(scoreConverted); <br />
   OUTPUT: NaN <br />
* **Converting to Boolean** <br />
1. let score = "50" <br />
   let scoreConverted = Boolean(score) <br />
   console.log(scoreConverted) <br />
   OUTPUT : true
2. let score = "" <br />
   let scoreConverted = Boolean(score) <br />
   console.log(scoreConverted) <br />
   OUTPUT : false
3. let score = 50 <br />
   let scoreConverted = Boolean(score) <br />
   console.log(scoreConverted) <br />
   OUTPUT : true
4. let score = null <br />
   let scoreConverted = Boolean(score) <br />
   console.log(scoreConverted) <br />
   OUTPUT : false
5. let score = undefined <br />
   let scoreConverted = Boolean(score) <br />
   console.log(scoreConverted) <br />
   OUTPUT : false

**Popular questions**: Interviewers just asks these to check if you have read the guidelines. Otherwise these questions are of no use because why in this world you wanna add a number to string.

1. console.log(2 + 2) OUTPUT : 4
2. console.log(2 + "2") OUTPUT: 22
3. console.log(1 + 2 + "2") OUTPUT: 32
4. console.log("1" + 2 + 2) OUTPUT: 122

# Popular Comparisions

1. console.log(1>2<2) OUTPUT: true
2. console.log(1<2==1) OUTPUT: true
3. console.log("2" < 1) OUTPUT: false
4. console.log("2" == 2) OUTPUT: true type conversion happened
5. console.log("2" === 2) OUTPUT: false strict type checking
6. console.log(null > 0) OUTPUT: false
7. console.log(null == 0) OUTPUT: false When comparing "2" == 2, the string "2" is coerced to a number, resulting in 2 == 2, which is true. However, null == 0 evaluates to false because the == operator handles       null and undefined specifically. It considers them loosely equal to each other but not to any other value, including 0. This behavior is part of the language specification.
8. console.log(null >= 0) OUTPUT: true because conversions convert null to a number so it is equivalent to checking if 0>=0
9. console.log(undefined >= 0) OUTPUT: false

# String and its methods
You already know what a string is so let's just move to **String interpolation**.
In early days we used '+' operator to concat strings. But there is one more way to concat wihout '+' is using backticks (``). If you want to insert variables in between a string, you can do that using '${}'. <br>
Ex: let name = "Sushi" <br>
    let age = 25 <br>
    console.log(`Hi! My name is ${name} and am ${age}y old.`) <br>
    OUTPUT: Hi! My name is Sushi and am 25y old. <br>

* String Methods
1. **at()**: takes an integer value and returns a new string with the character located at that specified value. <br> Ex: let str1= "universe" <br> console.log(str1.at(3)) <br> OUTPUT: v <br> let str1= "universe" <br> console.log(str1.at(-3)) <br> OUTPUT: r
2. **charAt()**: takes an integer value and returns a new string with the character located at that specified value. Now you must be thinking the difference between at() and charAt(), so charAt() doesn't give results with negative indices. If the index is not present in the string it will return empty string.
3. **concat()**: takes strings as arguments and return a new string by concating the argument strings with the current string that called the method. <br> Ex: let str1="universe" <br> console.log(str1.concat(" ","is"," ","beautiful")) <br> OUTPUT: universe is beautiful.
4. **endsWith()**: takes a string as argument (not regex) and endPosition as integer (optional), returns true or false. <br> Ex: let str1="universe is beautiful" <br> console.log(str1.endsWith("beautiful")) <br> OUTPUT: true
5. **includes()**: performs a case-sensitive search whether the argument string is present in the main string, return true or false accordingly. <br> Ex: let str1="universe is beautiful" <br> console.log(str1.includes("best")) <br> OUTPUT: false
6. **indexOf()**: takes a string and position(optional) as argument and return the index of first occurence of the search string greater than or equal to the position, which is by default 0.<br> This means that if you haven't given any position as arg, then it will put 0 autmatically and search if the search term is present at any index which is greater than or equal to 0.<br> Ex: let str1="universe is beautiful" <br> console.log(str1.indexOf("is")); <br> OUTPUT: 9<br> <br> let str1="universe is beautiful" <br> console.log(str1.indexOf("is",6)) <br> OUTPUT: 9 <br><br> let str1="universe is beautiful" <br> console.log(str1.indexOf("is",13)) <br> OUTPUT: -1 <br><br> let str1="universe is beautiful" <br> console.log(str1.indexOf("is",-9)) <br> OUTPUT: 9  <i>if you give negative position, it will behave as if position is 0</i>
7. **lastIndexOf()**: takes a string and position(optional) as argument and return the index of last occurence of the search string greater than or equal to the position.
8. **isWellFormed()** (Added in 2023): The isWellFormed() method of String values returns a boolean indicating whether this string contains any lone surrogates. **What are surrogates?**<br> Surrogate pairs are used in UTF-16 encoding to represent Unicode characters outside the Basic Multilingual Plane (BMP), i.e., characters with code points above U+FFFF (from U+10000 to U+10FFFF). <br>
* **High surrogate**: Code units in the range U+D800 to U+DBFF.
* **Low surrogate**: Code units in the range U+DC00 to U+DFFF. Together, a high surrogate and a low surrogate form a single Unicode character. <br>
 Ex: const str1 = "Hello, world!"; <br>
     console.log(str1.isWellFormed()); <br>
     Output: true <br>

    const str2 = "Invalid \uD800 string"; <br>
    console.log(str2.isWellFormed()); <br>
    Output: false

    const str3 = "Valid \uD83D\uDE00 string"; <br>
    console.log(str3.isWellFormed()); <br>
    Output: true
9. 
