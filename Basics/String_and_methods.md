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
8. **isWellFormed()** (Added in 2023): The isWellFormed() method of String values  returns a boolean indicating whether this string contains any lone surrogates. **What are surrogates?**<br> Surrogate pairs are used in UTF-16 encoding to represent Unicode characters outside the Basic Multilingual Plane (BMP), i.e.,      characters with code points above U+FFFF (from U+10000 to U+10FFFF). <br>
   * **High surrogate**: Code units in the range U+D800 to U+DBFF.
   * **Low surrogate**: Code units in the range U+DC00 to U+DFFF.<br>  Together, a high surrogate and a low surrogate form a single Unicode character. <br>
   Ex:   const str1 = "Hello, world!"; <br>
         console.log(str1.isWellFormed()); <br>
         Output: true <br>

      const str2 = "Invalid \uD800 string"; <br>
      console.log(str2.isWellFormed()); <br>
      Output: false

      const str3 = "Valid \uD83D\uDE00 string"; <br>
      console.log(str3.isWellFormed()); <br>
      Output: true
9. **replace()**: takes a pattern and replacement as argument and return a new string with first occurence of pattern replaced. To replace all occurences use **replaceAll()**. If the pattern is a regex then we must set global flag, otherwise error thrown. <br><br>
Ex: let st1="aabbcc"<br>
console.log(st1.replace("b","d")) <br>
OUTPUT: aadbcc <br> <br>
let st1="aabbcc"<br>
console.log(st1.replaceAll("b","d")) <br>
OUTPUT: aaddcc <br><br>
let st1="aabbcc"<br>
console.log(st1.replaceAll(/b/g,"d")) <br>
OUTPUT: aaddcc <br><br>
10. **split()**: takes a seprator as argument an returns an array of strings which was made by seperating strings around the seperator. <br>
Ex: let str1="universe" <br>
console.log(str1.split("")) <br>
OUTPUT: [
  'u', 'n', 'i',
  'v', 'e', 'r',
  's', 'e'
] <br><br>
let str1="universe" <br>
console.log(str1.split("v")) <br>
OUTPUT: [ 'uni', 'erse' ] <br><br>

11. **substring()**: takes startindex and endindex(optional) as arguments and return a new string which is part of mainstring from start to end index. <br>
Ex: let str1="universe" <br>
console.log(str1.substring(2,6))<br>
OUTPUT: iver<br><br>

12. **toLowerCase()**: converts all alphabets of string to lowercase.

13. **trim()**: returns a string after removing whitespaces from both ends. To return a new string with whitespace trimmed from just one end, use **trimStart()** or **trimEnd()**.
