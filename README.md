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

   userName: shane_billy
   
4. **var** : please forget that it exists. Use this carefully.
   it was used initially but because of the issues in block and functional scope, devs don't recommend using it. Suppose you have used a variable called 'state' in one file and assigned a value to it,
    there is one more dev who used 'state' and assigned it a different value. Now there will be inconsistency with the values.

    
# Some datatypes
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
