## writeCode

```js
let words = [
  "mystery",
  "brother",
  "aviator",
  "crocodile",
  "pearl",
  "orchard",
  "crackpot",
  "rhythm"
];
// - Write a function findLongestWord that takes an array of words and returns the longest word from the array. (Use above array "words" to test it). If there are 2 with the same length, it should return the first occurrence.
var longest = "";
function findLongestWord(array) {
for(i = 0; i < array.length; i++) {
   if (array[i].length > longest.length) {
    longest = array[i];
  }
}
console.log(longest);
}

findLongestWord(words);

// - Convert the above array "words" into an array of length of word instead of word.
words.map(word => word.length )

// - Create a new array that only contains word with atleast one vowel.
words.filter(word => {
  for (i = 0; i < word.length; i++) {
    if (word[i] == 'a'|| word[i] == 'e'|| word[i] == 'i'|| word[i] == '0'|| word[i] == 'u' ) {
      return word;
    }
  }
})

//solve the same question using forEach
words.filter(word => {
  word.forEach(w => {
    if (word[i] == 'a'|| word[i] == 'e'|| word[i] == 'i'|| word[i] == '0'|| word[i] == 'u' ) {
      console.log(word) ;
    }
  })
  } )

// - Find the index of the word "rhythm"

words.indexOf('rhythm')

// - Create a new array that contians words not starting with vowel.
words.filter(word =>{
  if(word[0] !== 'a' && word[0] !== 'e' && word[0] !== 'i' && word[0] !== '0' && word[0] !== 'u' ) {
    return word;
  }
}
  )

// - Create a new array that contians words not ending with vowel
words.filter(word =>{
  if(word[word.length - 1] !== 'a' && word[word.length - 1] !== 'e' && word[word.length - 1] !== 'i' && word[word.length - 1] !== '0' && word[0] !== 'u' ) {
    return word;
  }
}
  )

let numbers = [6, 12, 1, 18, 13, 16, 2, 1, 8, 10];

// - Create a sumArray function that takes an array of number as a parameter, and calculate the sum of all its numbers
var sum = 0;
function sumArray(array) {
  for (i = 0; i < array.length; i++) {
    sum = sum + array[i]
  }
  return sum;
}

sumArray(numbers);
console.log(sum)

// - Make a new array that contains number multiplied by 3 like [6, 18, 27 ...]
numbers.filter(num => {
  if (num % 3 == 0) return num;
})

// - Create a new array that contains only even numbers
numbers.filter(num => {
  if (num % 2 == 0) return num;
})


// - Create  a new array that contains only odd numbers.
numbers.filter(num => {
  if (num % 2 !== 0) return num;
})


// - Create a new array that should have true for even number and false for odd numbers.
numbers.map(num => {
  if (num % 2 == 0) {
    return true;
  } else {
    return false;
  }
})

// - Sort the above number in assending order.
numbers.sort((a, b)=> a - b)

// - Does sort mutate the original array?
Yes, sort mutates. In the above example, after sort, array 'numbers[]' modified to ascending order //[1, 1, 2, 6, 8, 10, 12, 13, 16, 18]

// - Find the sum of the numbers in the array.
numbers.reduce((acc, num)=>acc + num, 0);


//- Write a function averageNumbers that receives an array of numbers and calculate the average of the numbers
var sum = 0;
function averageNumbers(array) {
  for (i = 0; i < array.length; i++) {
    sum = sum + array[i]
  }
  return (sum / array.length);
}

averageNumbers(numbers);

//method-2

function averageNumbers(array) {
  let sum = array.reduce((acc, num, i, array)=>acc + num);
  let avg = sum / array.length;
return avg;
}
  averageNumbers(numbers)



let strings = [
  "seat",
  "correspond",
  "linen",
  "motif",
  "hole",
  "smell",
  "smart",
  "chaos",
  "fuel",
  "palace"
];
// - Write a function averageWordLength that receives an array of words2 and calculate the average length of the words.

function averageWordLength(array) {
  var sum = array.map(x =>x.length).reduce((acc, num) => acc + num, 0);
  var avg = sum / array.length
return avg;
}

averageWordLength(strings);


```

## String Methods-writeCode

- Write a JavaScript function to check whether input value is a string or not.

```js
/* Requirements
  @name isString
  @parameter (any value) val
  @return Boolean
*/

// your code goes here

function isString(val) {
  if (typeof(val) == "string") {
    return true;
  } else {
    return false;
  }
}
isString('abhishek');

//m-2
function isString(val) {
  var value =val.endsWith("");
  return value;
}
isString('abhishek');

// Test
console.log(isString("tony stark")); // true;
console.log(isString([1, 2, 4, 0])); // false;
```

- Write a JavaScript function to check whether a string is blank or not.

```js
/* Requirements
  @name isBlank
  @parameter (any value) val
  @return Boolean
*/

// your code goes here
function isBlank(val) {
  if (val === "") {
    return true;
  } else {
    return false;
  }
}

// Test
console.log(isBlank("")); // true;
console.log(isBlank("abc")); // false;
```

- Write a JavaScript function to split a string and convert it into an array of words.

```js
/* Requirements
  @name stringToArray
  @parameter (string) text
  @return Array
*/
// your code goes here

function stringToArray(text) {
  var arr = [];
var a = "";
  for (i = 0; i < text.length; i++) {
    if(text[i] !== " ") {
       a = a + text[i];
    } else {
    arr.push(a);
    a = "";
    }
    if (i === (text.length-1)) {
      arr.push(a);
    }
  }
  return arr;
}

// Test
console.log(stringToArray("Hello World")); // ["Robin", "Singh"];
console.log(stringToArray("Lady Bird")); // ["Lady", "Bird"];
```

- Write a JavaScript function to return specified number of characters from a string.

```js
/* Requirements
  @name truncate
  @parameter (string, number) text, len
  @return String
*/
// your code goes here

function truncate(text, end) {
  return text.slice(0, end)
}
truncate("Robin Singh", 4)

// Test
console.log(truncate("Robin Singh", 4)); //"Robi";
```

- Write a JavaScript function to convert a `string` in abbreviated form.

```js
/* Requirements
  @name abbrevName
  @parameter (string) fullName
  @return String
*/
// your code goes here
function abbrevName(string) {
  for (i = 0; i < string.length; i++) {
    if(string[i] == " ") {
      return string.slice(0, i+2).concat(".");
    }
  }
}

//method-2
function abbrevName(string) {
  return string.split(" ")[0] + " " + string.split(" ")[1].slice(0, 1) + ".";
}


// Test
console.log(abbrevName("Robin Singh")); //"Robin S."
```

- Write a JavaScript function to hide email addresses to protect from unauthorized user.

```js
/* Requirements
  @name protect
  @parameter (string) email
  @return String
*/
// your code goes here
function protect(email) {
  return email.split("@")[0].slice(0, 5).padEnd(8, '.' ) + '@' + email.split("@")[1]
}

//method-2
function protect(email) {
  return email.split("@")[0].slice(0, 5).concat("...", "@" `${email.split("@")[1]}` )
}

// Test
console.log(protect("robin_singh@example.com")); // "robin...@example.com"
```

- Write a JavaScript function to parameterize a string.

```js
/* Requirements
  @name parameterize
  @parameter (string) str
  @return String
*/
// your code goes here
function parameterize(str) {
  return str.toLowerCase().split(' ').join('-')

}

// Test
console.log(parameterize("Robin Singh from USA.")); // "robin-singh-from-usa"
```

- Write a JavaScript function to capitalize the first letter of a `string`.

```js
/* Requirements
@name capitalizeFirst
@parameter (string, number) text, len
@return String
*/
// your code goes here
function capitalizeFirst(text) {
  return text.split("")[0].toUpperCase() + text.split("").slice(1).join('')
}

// Test
console.log(capitalizeFirst("js string exercises")); // "Js string exercises"
```

- Write a JavaScript function to capitalize the first letter of each word in a string.

```js
/* Requirements
  @name capitalizeWords
  @parameter (string) text
  @return String
*/
// your code goes here
function capitalizeWords(text) {
  // var a = text.split(" ");
  return text.split(" ").map(word => word.split("")[0].toUpperCase() + word.split("").slice(1).join('')).join(' ');
}

console.log(capitalizeWords("js string exercises")); // "Js String Exercises"
```

- Write a function that takes a string which has lower and upper case letters as a parameter and converts upper case letters to lower case, and lower case letters to upper case.

```js
/* Requirements
  @name swapcase
  @parameter (string) text
  @return String
*/
// your code goes here

function swapcase(text) {
  var swappedValue = text.split('').map( (char, i) => {
    if (char.charCodeAt() >= 65 && char.charCodeAt() <= 90) {
     var character = char.toLowerCase();
    } else {
      character = char.toUpperCase();
    }
    return character;
  }).join("");
  return swappedValue;
}



// Tets
console.log(swapcase("AaBbc")); // "aAbBC"
```

- Write a function to convert a string into camel case.

Example:

```js
/* Requirements
  @name camelize
  @parameter (string) text
  @return String
*/
// your code goes here
function camelize(text) {
  var arrOfWords = text.split(" ");
  var camelizedText = arrOfWords[0].toLowerCase();

  arrOfWords.forEach((word, i) => {
    if(i !== 0) {
      // var capitalizedWord = word.split("").map((char, i) => {
      //   return (i == 0) ? char.toUpperCase() : char.toLowerCase();
      // })
      var capitalizedWord = word.charAt(0).toUpperCase() + word.slice(1).toLowerCase()
      camelizedText += capitalizedWord;
    }
  });

  return camelizedText;
}


// method-2(less preferred)
function camelize(text) {
  return text.split(" ")[0] + text.split(" ").slice(1).map(word => word.split("")[0].toUpperCase() + word.split("").slice(1).join("")).join("")
}
// Test
console.log(camelize("JavaScript Exercises")); // "JavaScriptExercises"
console.log(camelize("JavaScript exercises")); // "JavaScriptExercises"
console.log(camelize("JavaScriptExercises")); // "JavaScriptExercises"
```

- Write a function to uncamelize a string. Example:

```js
/* Requirements
  @name uncamelize
  @parameter (string, string) text, joinStr
  @return String
*/
// your code goes here
function uncamelize(text, joinstr) {
  return text.split('').map((char, i) => {
    if (char.charCodeAt() >= 65 && char.charCodeAt() <= 90) {
      return char.tolowerCase();
    }
	else {
		return char;
    }
  })
}


var final = "";
function uncamelize(text, joinstr) {
  for (i = 0; i < text.length; i++) {
    if (text[i].charCodeAt() >= 65 && text[i].charCodeAt() <= 90) {
      final += joinstr + text[i].toLowerCase();
    }
	else {
		final += text[i];
  }
}
return final;
}
// Tets
console.log(uncamelize("helloWorld", "_")); // "hello_world"
```

- Write a function to concatenates a given string n times (default is 1).

```js
/* Requirements
  @name repeat
  @parameter (string, number) text, times
  @return String
*/
// your code goes here
function repeat(text, times = 1) {
  return text.repeat(times)
}

// Test
console.log(repeat("Ha!", 3)); // "Ha!Ha!Ha!"
```

- Write a function to insert a string within a string at a particular position (default is 1).

```js
/* Requirements
  @name repeat
  @parameter (string, number) text, position
  @return String
*/
// your code goes here
function insert(text1,text2, position) {
  var a = text1.split("");
  a.splice(position, 0, text2);
  return a.join("");
}

//method - 2
function insert(text1,text2, position) {
  var result = text1.slice(0,position) + text2 + text1.slice(position);
  return result;
}
// Test
console.log(insert("We are doing some exercises.", "JavaScript ", 18)); // "We are doing some JavaScript exercises."
```

- Write a JavaScript function to humanized number (Formats a number to a human-readable string.) with the correct suffix such as 1st, 2nd, 3rd or 4th.

```js
/* Requirements
  @name humanize
  @parameter ( number) num
  @return String
*/
// your code goes here
function humanize(num) {
  var a = String(num);
  if (a[a.length-1] == '1') {
      a = a + 'st';
  } else if(a[a.length-1] == '2') {
      a = a + 'nd';
  } else if(a[a.length-1] == '3') {
      a = a + 'rd';
  } else {
      a = a + 'th';
  }
  return a;
}
// Test
console.log(humanize(301)); // "301st"
console.log(humanize(402)); // "402nd"
```

###

Write a function to truncates a string if it is longer than the specified number of characters. Truncated strings will end with a translatable ellipsis sequence ("…") (by default) or specified characters.

```js
/* Requirements
  @name testTruncate
  @parameter (string, number, string) text, len, postfix
  @return String
*/
// your code goes here
function textTruncate(text, len, postfix) {
  if (text.length > len) {
    var a = text.slice(0, (len - postfix.length)) + postfix;
  }
}

// Test
console.log(textTruncate("We are doing JS string exercises.", 15, "!!")); //"We are doing !!"
```

- Write a JavaScript function to chop a string into chunks of a given length.

```js
/* Requirements
  @name chop
  @parameter (string, number) text, size
  @return String
*/
// your code goes here

var final = [];
function stringChop(text, size) {
  for (i = 0; i < text.length; i = i + 2){
    var char = text.substr(i, size);
    final.push(char);
  }
  return final;
}

// Test
console.log(stringChop("hello world", 2)); // ["he", "ll", "o ", "wo", "rl", "d"]
```

- Write a function to count the occurrence of a substring in a string.

```js
/* Requirements
  @name count
  @parameter (string, string) text, char
  @return Number
*/
// your code goes here
var finalCount = 0;
function count(text, char) {
  var splittedWord = text.split(" ");
  splittedWord.forEach(word => {
    if(word == char) {
      finalCount++;
    }
  });
  return finalCount;
}

//method-2 using indexOf



function count(text, char) {
  var pos = 0;
  var finalCount = 0;
  var findPos = text.indexOf(char);
  
  while (findPos !== -1){
      var findPos = text.indexOf(char, findPos + 1);
      finalCount++;
      findPos = findPos + 1;
    }
    return finalCount;
}

// Test
console.log(count("The quick brown fox jumps over the lazy dog", "the")); // 2
```

- Write a function to strip leading and trailing spaces from a string.

```js
/* Requirements
  @name strip
  @parameter (string) text
  @return String
*/

function strip(text) {
  return text.trim();

}

// Test
console.log(strip("   Hello World ")); // "Hello World"
```

- Write a JavaScript function to truncate a string to a certain number of words.

```js
/* Requirements
  @name chopWords
  @parameter (string, number) text, words
  @return String
*/

function chopWords(text, words) {
  return text.split(" ").slice(0, words).join(' ')
}
// Test
console.log(chopWords("The quick brown fox jumps over the lazy dog", 4)); // "The quick brown fox"
```

- Write a function to alphabetize a given string.(A - z)

```js
/* Requirements
  @name alphabetize
  @parameter (string, number) text, times
  @return String
*/
function alphabetize(text) {
  return text.split("").sort().join("");
}

// Test
console.log(alphabetize("United States")); // 'SUadeeinsttt'
```
