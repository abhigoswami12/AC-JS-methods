# String Methods

## Practice String Methods-writeTextAnswer

Go to this [link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charAt) and look for the name of method to learn about it.

**Write in your own way of understanding (dont copy paste)**

Only if you are done with step 1 you should go ahead.

1. Practice it by yourself in console (4-5 times to understand)
2. Data types of parameters
3. Return value type
4. Example (3)
5. In your words what this method does.

Example:

1. `charAt`

   - This method accepts one parameter (index) of number data type.
   - It returns the charater on specific index (provided through parameter)
   - Example:
     ```js
     let name = "Arya Stark";
     name.charAt(2); //"y"
     let sentance = "A quick brown fox jumped over a lazy dog";
     sentance(4); // "i"
     let houseName = "Starks";
     houseName.charAt(0); // "S"
     ```
   - `charAt` accepts a index (number data type) and return the character on that index.

2. `toUpperCase`

- This method does not take any parameter.

- It returns the uppercase result of the targeted string/letter.
```js
let name =  "abhishek";
name.toUpperCase();
let name = "ashik";
name[0].toUpperCase();
let address = "dharamsala";
address.toUpperCase();
```
- This method converts the targeted string/letter to uppercase.

3. `toLowerCase`

- This method does not take any parameter.

- It returns the lowercase result of the targeted string/letter.
```js
let name =  "ABHISHEK";
name.toLowerCase();
let name = "ASHIK";
name[0].toLowerCase();
let address = "DHARAMSALA";
address.toLowerCase();
```
- This method converts the targeted string/letter to lowercase.
4. `trim`
-This method removes whitespace (includes spaces, tabs etc) from both ends of the string.
- It does not take any parameter and returns the result as no start or end whitespace.
```js
let name =  " ABHISHEK ";
name.trim();
let name = " ASHIK";
name.trim();
let address = "DHARAMSALA ";
name.trim();
```

5. `trimEnd`
-This method removes whitespace (includes spaces, tabs etc) from the end side of the string.
- It does not take any parameter and returns the result with no  end whitespace.
```js
let name =  " ABHISHEK ";
name.trimEnd();
let name = " ASHIK";
name.trimEnd();
let address = "DHARAMSALA ";
name.trimEnd();
```
-We can also use `trimRight()` in place of `trimEnd`
6. `trimStart`

-This method removes whitespace (includes spaces, tabs etc) from the start  of the string.
- It does not take any parameter and returns the result with no start whitespace.
```js
let name =  " ABHISHEK ";
name.trimStart();
let name = " ASHIK";
name.trimStart();
let address = "DHARAMSALA ";
name.trimStart();
```

-We can also use `trimLeft()` in place of `trimStart`


7. `concat`
-This method takes string as parameter.Even if we don't give string, it will implicitly convert the arguments to string while concatanation.
-It returns the new string after concatanating the string given in the argument with the calling string.
```js
'Abhishek'.concat(' ',"Goswami");

let name = "Ashik";
let surname = 'Raj';
name.concat(' ', surname);

surname.concat(' ', name);
```
8. `endsWith`

-This method takes a string and a number type (length of the string which is optional) as  a parameter.
- It returns true if the string ends with the characters provided in the parameter, else it return false.
```js
let str = 'How are you'
str.endsWith('you', 11);

let str = 'How are you?'
str.endsWith('You', 11);

let str = 'How are you'
str.endsWith('?');
```
-This method determines whether or not the string ends with the specified string.

9. `includes`
-This method takes string and a number as a parameter.The number type is optional. It gives the index of the character from where the search is to be begin with.
- It returns true if the string includes the string given in the parameter or else it returns false.
```js
'widget with id'.includes('widget');//true
'widget'.includes('id', 3);//false
'hello'.includes('bye');//false
```
-This method checks if the string provided in the parameter is included in the string or not.

10. `indexOf`


- The parameters of this method are a string and a number(an integer).The number type is optional. It gives the index of the character from where the search is to be begin with.
- It returns the index of the position where the match is found, or else it returns -1.
```js
let str = "Widget with id";
str.indexOf('Widget');

str.indexOf('widget');

str.indexOf('id');

str.indexOf('id', 2);
```
- Syntax: str.indexOf(substr, pos).
  It look for the `substr` in the given string `str` starting from the position `pos` and returns the position where the match is found or else it returns -1.

11. `lastIndexOf`
-The parameters of this method are a string and a number(an integer)-The number type is optional. It gives the index of the character from where the search is to be begin with from the end side of the string.
-It returns the index of the position where the match is found, or else it returns -1.
```js
let str = "Widget with id";
str.lastIndexOf('id'); //12

str.lastIndexOf('id', 2); //1
 
'raja of raja'.lastIndexOf('raja').//8

```
- Syntax: str.lastIndexOf(substr, pos).
  It look for the `substr` in the given string `str` starting from the position `pos` from right to left and returns the position where the match is found or else it returns -1.

12. `padEnd`
-The padEnd() method  pads the current string with the given string to the end of the string so that the resultant string matches the given length .
-str.padEnd(targetlength [, string]);
 It takes a target length of number type and a string which is to be padded to give the target length.The string is optional. If nothing specified, the default value is " ".
 eg:
 ```js
 "Abhishek".padEnd(15, "Goswami")//AbhishekGoswami
 'abc'.padEnd(6,'def')//abcdef
 'abc'.padEnd(6)//"abc   "
 ```
-It returns a string of the specified length with the specified string being padded.

13. `padStart`
-The padStart() method  pads the current string with the given string at the start of the string so that the resultant string matches the given length .
-str.padEnd(targetlength [, string]);
 It takes a target length of number type and a string which is to be padded to give the target length.The string is optional. If nothing specified, the default value is " ".
 eg:
 ```js
 "Abhishek".padStart(15, "Goswami")//GoswamiAbhishek
 'abc'.padEnd(6,'de')//deeabc
 'abc'.padEnd(6)//"   abc"
 ```
-It returns a string of the specified length with the specified string being padded.
14. `repeat`
- This method returns a new string which conatins the specified number of copies of the string and concatanated together.
-str.repeat(count):
This method takes a number as parameter which is the count for the number of times the string is to be repeated. The count must be a non-negative value.
-It returns a new string containing the specified number of copies of the given  string.
eg:
```js
'abc'.repeat(3)//abcabcabc
'abhishek'.repeat(-1)//Error.cannot take negative parameter
'anhishek'.repeat(2)//abhishekabhishek
```

15. `replace`
Syntax: newStr = str.replace(substr, newSubstr|function)
-This method takes a part of the string to be replaced and a new string or a fuction which will replace the string.
-It returns the new resultant string .
-This method does not change the existing string; it just creates a new string with the specified changes.
eg:
```js
'abhishek goswami'.replace('goswami', 'giri')//abhishek giri
'ankit sinha'.replace('sinha', 'giri')// ankit giri
'ashik kumar'.replace('kumar', 'raj')//ashik raj
```

16. `slice`

str.slice(start, end)
-It takes two number types parameters
-It returns the part of the string from 'start' to 'end' but not including the 'end'
-If no second argument is given, then it goes till the end.
-negative value of parameters indicate that the position is counted from the string end.
eg:
```js
'abhishek'.slice(0,5)//abhis
'abhishek'.slice(2)//hishek
'abhishek'.slice(-4,7)//she. Four position from the end is 's' and '7' index is of 'k'.
```

17. `split`
str.split(separator, limit);

- This method takes a string and a number type as parameter.
- It returns an array of string, split at each point where the 'seaparator' occurs in the given string.
- This method divides a string into an ordered set of substrings and put these substrings into an array and returns the array.
eg:
```js
'abc'.split("")//["a", "b", "c"]
'abhi'.split()//["a", "b", "h", "i"]
"The quick brown fox jumps over the lazy dog".split(" ", 3)//["The" "quick" "brown"]
```
18. `substring`
str.substring(start, end)
- This method returns the part of the string from the start to the end but including the end.
- It takes two parameters of both number types. If negative number is given as parameter then it consider it as '0'.
eg:
```js
'abhishek'.substring(0,5)//abhis
'abhishek'.substring(2)//hishek
'abhishek'.substring(-4,7)//abhishe.
```

## writeCode

Using above methods you practiced above, do the following.

```js
let from = "Syrio Forel";
let quote = "There is only one thing we say to death: Not today";
let to = "Arya Stark";

/*
1. Find the index of the first 'is' in the variable quote. And store it in a new variable named indexOfIs

*/
// Your code goes here

let indexOfIs = quote.indexOf('is');

/*
2. Find the character at, the index indexOfIs (Problem 1) in quote.
*/
// Your code goes here
quote.charAt(indexOfIs);


/*
3. Log the message saying `The index of first is in quote is 7`
*/
// Your code goes here
console.log(`The index of first is in quote is ${indexOfIs}`);

/*
4. Log the message for first 6 characters of quote like this.
The character at index 0 is 'T'
The character at index 1 is 'h'
The character at index 2 is 'e'
The character at index 3 is 'r'
The character at index 4 is 'e'
The character at index 5 is ' '
*/
// Your code goes here
console.log(`The character at index 0 is '${quote.charAt(0)}'`);
console.log(`The character at index 1 is '${quote.charAt(1)}'`);
console.log(`The character at index 2 is '${quote.charAt(2)}'`);
console.log(`The character at index 3 is '${quote.charAt(3)}'`);
console.log(`The character at index 4 is '${quote.charAt(4)}'`);
console.log(`The character at index 5 is '${quote.charAt(5)}'`)

/*
5. Using the variable from , to and quote variable dispaly this message
"Syrio Forel said There is only one thing we say to death: Not today to Arya Stark." (use concat method)
*/
console.log(from.concat(' said ', `${quote}`, ' to ', `${to}`))
/*
6. Does from, to and quote ends with "rk". Check all three.


*/
from.endsWith('rk')
quote.endsWith('rk')
to.endsWith('rk')
/*
7. Does quote includes the word "Only"
*/
quote.includes('only')

/*
8. Does quote includes the word " we"
*/
quote.includes('we')

/*
9. Find the index of the the word `we` in quote
*/
quote.indexOf('we')

/*
10. Split the quote into individual word and store it in a variable name quoteSplitted
*/
var quoteSplitted = quote.split(' ');
console.log(quoteSplitted);

/*
11. Change the word "today" in quoteSplitted to "tomorrow" and join all the words to form a sentance.
*/
 quoteSplitted.replace('today', 'tomorrow')


/*
12. Find the index of second "o" in quote. Use indexOf
*/
quote.indexOf('o', 10)

/*
13. Find the last index of letter "a" in quote.
*/
quote.lastIndexOf('a')

/*
14. Find the second last index of letter "a" in quote.
*/
quote.lastIndexOf('a',47)

/*
15. Make the quote 70 character long. If it has less characters add rest as .......
Example: "Hello" (convert to 10 characters) => "Hello....."
*/
quote.padEnd(70, '.')

/*
16. Do same as (15) but the ... should come in start.
*/
quote.padStart(70, '.')

/*
17. Log the repeat of "Hello World!" 10 times.
*/
' Hello World '.repeat(10)

/*
18. Replace today to tomorrow in quote.
*/
quote.replace('today', 'tomorrow')

/*
19. Replace Stark to Lannister in quoteTo
*/
to.replace('stark', 'Lannister')

/*
20. Make the quote of length 30 and put ... at the end. (use slice)
*/
quote.slice(0, 30).padEnd(33, '.')

/*
21. Find out does quote, quoteFrom, quoteTo starts with "A"
*/
quote.startsWith('A')
to.startsWith('A')
from.startsWith('A')
```

## Practice Array Methods-writeTextAnswer

Go to this [link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#) and look for the name of method to learn about it.

**Write in your own way of understanding (dont copy paste)**

Only if you are done with step 1 you should go ahead.

1. Practice it by yourself in console (2-3 times to understand)
2. Data types of parameters
3. Return value type
4. Example (3)
5. In your words what this method does.
6. Does it mutate the original value (check https://doesitmutate.xyz)

Example:

1. `concat`

   - n(any) number of values (number, string, boolean, array, null, undefined, object and function.)
   - It returns a single Array consisting of by all the values passed as parameters in the same order.
   - Example:
     ```js
     let numbers = [1, 2, 3];
     numbers.concat(4); //[1,2,3,4]
     let sentanceArray = "A quick brown fox jumped over a lazy".split(" ");
     sentanceArray.concat("dog").join(" "); //"A quick brown fox jumped over a lazy dog"
     let colors = ["red", "green", "blue"];
     colors.concat("black", "red", 21, true); // ['red','green','blue','black', 'red', 21, true]
     ```
   - `concat` accepts n number of values and returns one array with all the values in same order. It doesnot change the original array.
   - No it doesnot mutate the original array

2. `join`
-arr.join(separator);
-This method concatanate all elements in the array using the separator provided by the user and returns the result.
- It takes a string as a parameter and uses it in between the strings of the array. If the separator is an empty string, the elements get concatanated without spaces.If nothing specified, then ',' is inserted between the elements.
- It returns a string with all elements of array concatanated and separated by 'saparator'.
eg:
```js
['abhishek', 'goswami', 157].join(' ');//'abhishek goswami 157'
['abhishek', 'goswami', 157].join('');//'abhishekgoswami157'
['abhishek', 'goswami', 157].join();//'abhishek,goswami,157'
```

3. `flat`
-arr.flat(depth);
- This method creates a new array with all sub-array elements concatanated together depending on the depth given.
- It accepts a numeric value as 'depth'. The default value is '1'.
- It returns a new array with the sub-array concanated to it.
eg:
```js
var arr = [1, 2, [3, 4, [5, 6]]];
arr.flat();//[1, 2, 3, 4, [5, 6]];
arr.flat(2);//[1, 2, 3, 4, 5, 6];
arr.flat(infinity)//[1, 2, 3, 4, 5, 6];

```
4. `push`
-arr.push(element1, element2, ....)
- This method adds one or more elements to the end of the array.
-Its parameter can be number, strings, boolean, NaN, undefined, object, array or function.
- It returns the new length property of the object upon which the method was called.
eg: 
```js
let arr = [1, 2, 3, 4, 5]
let count = arr.push(6, 7);
console.log(count)//7
console.log(arr)//[1, 2, 3, 4, 5, 6, 7];

let arr = ['abhi', 'ashik'];
console.log(arr.push('ankit'));//['abhi', 'ashik' 'ankit']

let arr = ['red', 'green', 'blue'];
console.log(arr.push('orange'));//['red', 'green', 'blue', 'orange']

```

5. `indexOf`
arr.indexOf(item, from)
-It looks for 'item'(string) starting from index 'from'(number type and is optional) and returns the first index of the element of the array where it was found, or else it returns '-1'.
Eg:
```js
let arr = ['widget','with', 'id'];
arr.indexOf('id');//2

let arr = [2, 9, 9]
arr.indexOf(9)//1
arr.indexOf(9, 2)//2
arr.indexOf(2, -1)//-1
arr.indexOf(2, -3)//0
```

6. `lastIndexOf`
arr.lastIndexOf(start, from)
-The parameters of this method are a string and a number(an integer)-The number type is optional. It gives the index of the character from where the search is to be begin with from the end side of the string i.e. from right to left.
-It returns the index of the position where the match is found, or else it returns -1.
Eg:
```js
let arr = [2, 5, 9, 2];

arr.lastIndexOf(2)//3
arr.lastIndexOf(7)//-1
arr.lastIndexOf(2, 3)//3
arr.lastIndexOf(2, 2)//0
arr.lastIndexOf(2, -2)//0
arr.lastIndexOf(2, -1)//3
```
7. `includes`
arr.includes(item, from)
-This method takes string and a number as a parameter.The number type is optional. It gives the index of the character from where the search is to be begin with.
- It returns true if the string includes the string given in the parameter or else it returns false.
Eg:
```js
let arr = [1, 2, 3];
arr.includes(2);//true
arr.includes(4);//false
arr.includes(3, 3);//false
arr.includes(3, -1);//true
[1, 2, NaN].includes(NaN);//true

```

8. `reverse`
- a.reverse();
- This method reverses an array i.e. the first element in the array becomes the last and the last element becomes the first.
-This method takes no parameters.
- It returns the reversed array.
eg:
```js
let arr = [1, 2, 3, 4, 5]
console.log(arr.reverse())//[5, 4, 3, 2, 1]


let arr = ['abhi', 'ashik', 'ankit'];
console.log(arr.reverse());//['ankit', 'ashik', 'abhi']

let arr = ['red', 'green', 'blue'];
console.log(arr.reverse());//['blue', 'green', 'red']
```
9. `every`
arr.every(callback_fn);
- This method takes a callback fn as parameter.
-It returns boolean value.It returns true if all elements in the array returns a truthy value or else false is returned.
- This method takes each element and tests if its truthy or not and returns a boolean value according to that.
eg:
```js
function isEven(n){
  return n % 2 == 0;
}
let arr = [34, 56, 93, 81];
console.log(arr.every(isEven));//false

function isEven(n){
  return n % 2 == 0;
}
let arr = [34, 56, 92, 88];
console.log(arr.every(isEven));//true

function isOdd(n){
  return n % 2 != 0;
}
let arr = [34, 56, 93, 81];
console.log(arr.every(isOdd));//false
```
10. `shift`
-arr.shift();
- This method removes the first element from the array and return that element. This method changes the length of the array.
- It takes no parameters.
- It returns the removed element from the array and undefined if the array is empty.
eg:
```js
[1, 2, 3].shift();//1
['abhi', 'ashik' 'ankit'].shift()//'abhi'
['blue', 'green', 'red'].shift()//'blue'

```
11. `splice`
-arr.splice(index, deleteCount, element1, element2,...)
- We can delete an element using delete.arr[] but this will delete the element but the length of the array will be some. In that case, splice comes to the rescue.
- It takes an index of number type which indicates the index position from which the deletion is to start. The second parameter 'deleteCount' is also a number type. It indicates the number of count of the elements which are to be deleted from the array. And the parameters element1/element2 are string data type which are supposed to be inserted after the deletion procedure.
- This method returns a new array containing the extracted elements.

Eg:
```js
let arr = ['I', 'go', 'home'];

arr.splice(2, 1, 'right', 'now')//['home']
arr;//["I", "go", "right", "now"]


let arr = ['I', 'go', 'home'];
arr.splice(2, 0,'right', 'now' )//start deletion from pos[2], delete 0 items and add 'right' 'now' starting from position 2.So, ans is []
arr//["I", "go", "right", "now", "home"]

let arr = [1, 2, 5];
arr.splice(-1, 0, 3, 4);//start from 1 position right from end, delete '0' items and add 3, 4 starting from position 1 right from the end.//[]//returns empty array

arr//[1, 2, 3, 4, 5]

```
12. `find`
-arr.find(fn);
-It accepts a callback function as a parameter wherein the callback function has elements, index and the array itself as its parameter.
-It returns the value of the first element in the array that satisfies the condition provided in the callback function or else, it returns 'undefined'.

Eg:
```js
var arr = [1, 2, 3, 4, 5];

arr.find(n =>n > 3);//4

arr.find(n=>n %3 == 0)//3

var arr = [
  {name: 'Abhishek', age: 28},
  {name: 'Ankit', age: 27},
  {name: 'Prashant', age: 27},
]

function details(student) {
  return student.age == 27;
}
arr.find(details);//{name: "Ankit", age: 27}



var heroes = [
	{name: "Batman", franchise: "DC"},
	{name: "Ironman", franchise: "Marvel"},
	{name: "Thor", franchise: "Marvel"},
	{name: "Superman", franchise:"DC"}
];

function details(hero) {
  return hero.franchise == "Marvel";
}

heroes.find(details);//{name: "Ironman", franchise: "Marvel"}
```

13. `unshift`
-arr.unshift(element1, element2,...);
- This method adds one or more elements to the beginning of the array.
- It takes any type value as parameter.
- This method returns the new length of the array.
eg:
```js
let arr = [1, 2, 5, 6];
arr.unshift(44, 57)//6; new length of the string
console.log(arr)//[44, 57, 1, 2, 5, 6]

let arr = ['abhi', 'ashik'];
console.log(arr.unshift('ankit'));//['ankit', 'abhi', 'ashik']

let arr = ['red', 'green'];
console.log(arr.unshift('blue'));//['blue', 'red', 'green']
```
14. `findIndex`
arr.findIndex(callback_fn)
-It accepts a callback function as a parameter wherein the callback function has elements, index and the array itself as its parameter.
-It returns the index of the first element in the array that satisfies the condition provided in the callback function or else, it returns -1.

Eg:

```js
var arr = [1, 2, 3, 4, 5];

arr.findIndex(n =>n > 3);//3, (index of 4)

arr.findIndex(n=>n %3 == 0)//2

var arr = [
  {name: 'Abhishek', age: 28},
  {name: 'Ankit', age: 27},
  {name: 'Prashant', age: 27},
]

function details(student) {
  return student.age == 27;
}
arr.findIndex(details);//1



var heroes = [
	{name: "Batman", franchise: "DC"},
	{name: "Ironman", franchise: "Marvel"},
	{name: "Thor", franchise: "Marvel"},
	{name: "Superman", franchise:"DC"}
];

function details(hero) {
  return hero.franchise == "Marvel";
}

heroes.findIndex(details);//1
```
15. `filter`
arr.filter(callback_fn)
-This method is similar to 'find' but it returns an array of all truthy elements.
-It accepts a callback function as a parameter wherein the callback function has elements, index and the array itself as its parameter.
-It returns a new array with all the truthy elements in it and no truthy element is found, it returns an empty string.

Eg:
```js
var arr = [1, 2, 3, 4, 5];

arr.filter(n =>n > 3);//[4, 5]

arr.filter(n=>n %3 == 0)//[3]

var arr = [
  {name: 'Abhishek', age: 28},
  {name: 'Ankit', age: 27},
  {name: 'Prashant', age: 27},
]

function details(student) {
  return student.age == 27;
}
arr.filter(details);//[{name: "Ankit", age: 27}, {name: 'Prashant', age: 27}]



var heroes = [
	{name: "Batman", franchise: "DC"},
	{name: "Ironman", franchise: "Marvel"},
	{name: "Thor", franchise: "Marvel"},
	{name: "Superman", franchise:"DC"}
];

function details(hero) {
  return hero.franchise == "Marvel";
}

heroes.filter(details);//[{name: "Ironman", franchise: "Marvel"},{name: "Thor", franchise: "Marvel"}]
```

16. `flat`
-arr.flat(depth);
- This method creates a new array with all sub-array elements concatanated together depending on the depth given.
- It accepts a numeric value as 'depth'. The default value is '1'.
- It returns a new array with the sub-array concanated to it.
eg:
```js
var arr = [1, 2, [3, 4, [5, 6]]];
arr.flat();//[1, 2, 3, 4, [5, 6]];
arr.flat(2);//[1, 2, 3, 4, 5, 6];
arr.flat(infinity)//[1, 2, 3, 4, 5, 6];

17. `map`
arr.map(fn)
-It accepts a callback function as a parameter wherein the callback function has elements, index and the array itself as its parameter.
-It returns a new array of same length.
-For Each element of the array 'arr', call the callback function 'fn' and returns a new array  .

Eg:
```js
//double
var arr = [1, 2, 3, 4, 5];
function double(num) {
    return num * 2;
}
arr.map(double);

//square
function cb(x) {
    var square = x * x;
    return (square);
}
arr.map(cb);//[1, 4, 9, 16, 25]

//cube
function cb(x) {
    var cube = x * x;
    return cube;
}
arr.map(cb);//[1, 4, 9, 16, 25]
```
18. `forEach`
arr.forEach(fn)
-It accepts a callback function as a parameter wherein the callback function has elements, index and the array itself as its parameter.
-It returns 'undefined'.
-For Each element of the array 'arr', call the callback function 'fn'.

Eg:
```js
//console number
let arr = [1, 2, 3, 4, 5]
var cb = (num, i) => console.log(num, i);
arr.forEach(cb);/*1 0
                  2 1
                  3 2
                  4 3
                  5 4*/

//even number

function cb(num) {
    if(num % 2 == 0) console.log(num)
}
arr.forEach(cb);//2,4

//odd number
function cb(num) {
    if(num % 2 != 0) console.log(num)
}
arr.forEach(cb);//1, 3, 5
```
19. `pop`
arr.pop()
- It does not take any parameter.
- It returns the removed element from the array, and if the element is empty it returns 'undefined'

Eg:
```js
let arr = [1, 2, 3, 4, 5]
arr.pop();//5
 
let name = ['ankit', 'abhi', 'ashik'];
name.pop()//'ashik'

let arr = ['a', 'b', 'c'];
arr.pop();//'c'
```

20. `reduce`
arr.reduce(callbackfn(acc, element, index, array), intitialValue);
- It takes a callback function (which has one extra parameter i.e. accumulator) and an intial value of Number, string, array, object data type as a parameter.If initial value is not provided, then the first element of the array is stored in initial value and the next element becomes the first element.
-It returns the value that is resulted from the reduction.
-For every element in the array 'arr' call the callback function 'callbackfn' with the initial value given and return the result.
Eg
```js
let arr = [1, 2, 3, 4, 5];
var sum = arr.reduce((elm,acc) => acc+elm, 0);//15


let arr =[[1,2], [3, 4], [5, 6]].reduce((acc,elm)=> acc.concat(elm), [])//[1, 2, 3, 4, 5, 6]

21. `slice`
arr.slice(start, end)
-Accepts two parameters of number type each. If 'end' is not given then it goes till the end of the array.
-Returns a new array starting from index 'start' to 'end' (not including end).
Eg:
```js
let arr = ['t', 'e', 's', 't'];

arr.slice(1, 3)//["e", "s"]

arr.slice(-2)//["s", "t"], start from 2nd position from the end (right to left) and go till the end of the array.

arr.slice()//['t', 'e', 's', 't'], create a copy of the array
```

22. `some`
arr.some(fn)
--It accepts a callback function as a parameter wherein the callback function has elements, index and the array itself as its parameter.
-It returns 'true' if the callback function return a truthy value for atleast one element in the array, or else it returns 'false'

Eg:
```js
var arr = [1, 2, 3, 4, 5]
function greater(num) {
  return num >3;
}
arr.some(greater);//true


var arr = [1, 2, 3, 4, 5]
function greater(num) {
  return num >5;
}
arr.some(greater);//false


var arr = [1, 2, 3, 4, 5]
function even(num) {
  return num % 2 == 0;
}
arr.some(even);//true
```


## writeCode

Using above methods you practiced above, do the following.

```js
// Use the below two arrays and practice array methods
var numbers = [1, 12, 4, 18, 9, 7, 11, 3, 101, 5, 6, 9];
var strings = ["This", "is", "a", "collection", "of", "words"];

// - Find the index of `101` in numbers
numbers.indexOf(101)

// - Find the last index of `9` in numbers
numbers.lastIndexOf(9)

// - Convert value of strings array into a sentance like "This is a collection of words"
strings.join(' ')

// - Add two new words in the strings array "called" and "sentance"
strings.concat(' called',' sentence' )

// - Again convert the updated array (strings) into sentance like "This is a collection of words called sentance"
strings.concat(' called',' sentence' ).join(' ')

// - Remove the first word in the array (strings)
strings.shift()

// - Find all the words that contain 'is' use string method 'includes'
for(i = 0; i < strings.length; i++) {
  if(strings[i].includes('is')) {
    console.log(strings[i])
  }
}

// - Find all the words that contain 'is' use string method 'indexOf'
for(i = 0; i < strings.length; i++) {
  if(~(strings[i].indexOf('is'))) {
    console.log(strings[i])
  }
}

// - Check if all the numbers in numbers array are divisible by three use array method (every)
function div3(n) {
  return (n % 3 == 0);
}
console.log(numbers.every(div3))

// -  Sort Array from smallest to largest
strings.sort();
numbers.sort((a, b) => a - b);

// - Remove the last word in strings
strings.pop()

// - Find largest number in numbers
var largest= 0;
for(i = 0; i < numbers.length; i++) {
  if (numbers[i] > largest) {
    largest = numbers[i];
  }
}
console.log(largest);


//method-2
numbers.sort((a, b) => a - b).pop()


// - Find longest string in strings
var longest = "";
for(i = 0; i < strings.length; i++) {
   if (strings[i].length > longest.length) {
    longest = strings[i];
  }
}
console.log(longest);


// - Find all the even numbers
for(i = 0; i < numbers.length; i++) {
  if (numbers[i] % 2 == 0) {
    console.log(numbers[i])
  }
}

// - Find all the odd numbers
for(i = 0; i < numbers.length; i++) {
  if (numbers[i] % 2 != 0) {
    console.log(numbers[i])
  }
}

// - Place a new word at the start of the array use (upshift)
strings.unshift('Hi')

// - Make a subset of numbers array [18,9,7,11]
numbers.slice(3, 7)

// - Make a subset of strings array ['a','collection']
strings.slice(2, 4)

// - Replace 12 & 18 with 1221 and 1881
numbers.splice(1, 1, 1221)
numbers.splice(3, 1, 1881)

// - Replace words in strings array with the length of the word
var arr = [];
for(i = 0; i < strings.length; i++) {
  arr.push(strings[i].length);
  
}
console.log(arr);


//m-2
strings.map(x=> x.length);

// - Find the sum of the length of words using above question
var arr = [];
var sum = 0;
for(i = 0; i < strings.length; i++) {
  arr.push(strings[i].length);
  sum = sum + strings[i].length;
  
}
console.log(arr);
console.log(sum);

//m-2
strings.map(x=> x.length).reduce((acc, num) => acc = acc + num, 0)

// - Customers Array
var customers = [
  { firstname: "Joe", lastname: "Blogs" },
  { firstname: "John", lastname: "Smith" },
  { firstname: "Dave", lastname: "Jones" },
  { firstname: "Jack", lastname: "White" }
];
// - Find all customers whose firstname starts with 'J'
for(i = 0; i < customers.length; i++) {
  if(customers[i].firstname.startsWith('J')) {
    console.log(customers[i])
  }
}
//method - 2
customers.filter(c =>c.firstname.startsWith('J'))

// - Create new array with only first name
var arr = [];
for(i = 0; i < customers.length; i++) {
  arr.push(customers[i].firstname);
}
console.log(arr);

//method-2
customers.map(c=> c.firstname);

// - Create new array with all the full names (ex: "Joe Blogs")
var arr = [];
for(i = 0; i < customers.length; i++) {
  arr.push(customers[i].firstname + ' ' + customers[i].lastname)
}
console.log(arr);

//method-2
customers.map(x => x.firstname.concat(" ",x.lastname))

// - Sort the array created above alphabetically
customers.map(x => x.firstname.concat(" ",x.lastname)).sort();

// - Create a new array that contains only user who has at least one vowel in the firstname.
var arr = [];
for(i = 0; i < customers.length; i++) {
  if(customers[i].firstname.includes('a') || customers[i].firstname.includes('e') ||customers[i].firstname.includes('i')  || customers[i].firstname.includes('o')  || customers[i].firstname.includes('u') ) {
    console.log(customers[i].firstname);
    arr.push(customers[i].firstname);
  }
}
console.log(arr);


//method-2
customers.map.filter(word => {
  for (i = 0; i < word.length; i++) {
    if (word[i] == 'a'|| word[i] == 'e'|| word[i] == 'i'|| word[i] == '0'|| word[i] == 'u' ) {
      return word;
    }
  }
}
);

```
