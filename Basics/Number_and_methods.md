# Numbers and methods

Yes 1234 is a number. Let's get into its methods.
1. **toFixed()**:takes an integer value and returns a string with the specified number of decimal values.<br>Ex: let num1=1234.567<br>console.log(num1.toFixed(2))<br> OUTPUT:1234.56
2. **toLocaleString()**: returns a string with a language-sensitive representation of this number.<br>
Ex: let num1= new Number(1000000)<br>
console.log(num1.toLocaleString())<br>
OUTPUT: 1,000,000<br><br>
let num1= new Number(1000000)<br>
console.log(num1.toLocaleString(en-IN))<br>
OUTPUT: 10,00,000 <i>(Indian Standards of representation)</i><br><br>

3. **toPrecision()**: returns a string representing this number to the specified number of significant digits.<br>
Ex: num = 1234.5;
console.log(num.toPrecision(1)); // '1e+3'
console.log(num.toPrecision(2)); // '1.2e+3'
console.log(num.toPrecision(6)); // '1234.50'

# Math library
I am assuming you are a PCM student so you'll understand.<br>
1. **abs()**:takes any integer but returns positive integer.<br>
Ex: console.log(Math.abs(-16)) // 16
2. **round()**:gives a round off of given number.<br>
Ex:console.log(Math.round(4.6)) // 5
3. **ceil()**:gives a round-off to its higher side.<br>
Ex:console.log(Math.ceil(4.2)) // 5
4. **floor()**:gives a round-off to its lower side.<br>
Ex:console.log(Math.ceil(4.7)) // 4
5. **min()**:gives the minimum from a group of numbers.<br>
Ex:console.log(min(3,2,1,6)) // 1
6. **max()**:gives the maximum from a group of numbers.<br>
Ex:console.log(min(3,2,1,6)) // 6
7. **random()**:gives a random number between 0 t0 1.<br>
Ex: const min=10<br>
const max=20<br>
console.log(Math.floor(Math.random()*(max-min+1))+min) // 14 <br>
