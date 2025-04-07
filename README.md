# Javascript_tutorial
A guide for know basics to intermediate Javascript

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

    
