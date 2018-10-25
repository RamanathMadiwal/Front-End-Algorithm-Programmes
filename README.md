# UI Web developer Javascript Interview Questions

   :red_circle:
## 1. Write code to find prime numbers efficiently

```
function isPrime(num) {

    if (num === 2) {
        return true;
    }

    if (!(Number.isInteger(num)) || (num < 2) || !(num % 2)) {
        return false;
    }

    let q = Math.floor(Math.sqrt(num));
    for (let i = 3; i <= q; i++) {
        if (num % i === 0) {
            return false;
        }
    }
    return true;
}


console.log(isPrime(23));
```

//******************************************************************************************************

## 2. write code to reverse string and integer
```
function reverseString(str){
Step 1
   return str.split('').reverse().join('');
step 2
    let subString='';
    let output=str.split('').reduce(function (subString,char) {
        console.log("the car value is"+char +"The subString value is"+subString);
        //the car value iscThe subString value is
        //the car value isaThe subString value isc
        //the car value isrThe subString value isac
        return char+subString;

    },'');

   return console.log(output);
step 3
  let subStringValue='';

  for(let char of str){
      subStringValue=char+subStringValue;
      console.log("The value is "+subStringValue);

  }
console.log(subStringValue);

}


reverseString("car");
console.log(reverseString("car"));
```
!******************************************************************************************************
```
function reverseInteger(Intg){
    let str=Intg.toString();

        let subString='';
        let output=str.split('').reduce(function (subString,char) {
        console.log("the car value is"+char +"The subString value is"+subString);
        //the car value iscThe subString value is
        //the car value isaThe subString value isc
        //the car value isrThe subString value isac
        return char+subString;

    },'');
     console.log("The o"+output);
   return console.log(Math.floor((output)) * Math.sign(Intg));

}
reverseInteger(420);
```
!******************************************************************************************************

3.write code to find palindrome
```
function isPalindrome(str){

    let regEx=[/^[W_]]/gi];
    let convertedValue=str.toLowerCase().replace(regEx,'');
    let input=str.split('').reverse().join('');

    return input===convertedValue;

}

console.log(isPalindrome("racecar"));
```
!******************************************************************************************************
4.write code to find fibnoacci series
```
function printFibnoaciSum(num){

    let a=0;
    let b=1;
    let f=1;
    for(let i=2;i<num;i++){
        f=a+b;
        a=b;
        b=f;
    }
     return f;

}

console.log(printFibnoaciSum(8));
```
//!******************************************************************************************************
```
5. function printFibSeries(num) {

    if(num==2){
        return [0,1];
    }
    else{
        let s=printFibSeries(num-1);
        s.push(s[s.length-1]+s[s.length-2])
        return s;
    }
}

console.log(printFibSeries(8));
```
!******************************************************************************************************

6.write code to find factorial
```
function factorial(x){
    if(x == 0) {
        return 1;
    }
    if(x < 0 ) {
        return undefined;
    }
    for(var i = x; --i; ) {
        x *= i;
    }
    return x;
}

console.log(factorial(4));
```
!******************************************************************************************************

7.write code to find fizzbuzz
```
function FizzBuzz() {

    for(let i=0;i<=100;i++){
        if(i % 3===0 && i % 5===0){
            console.log("FIZZBUZZ");
        }else if(i %5 ===0) {
            console.log("BUZZ");
        }else if(i%3===0 && i%5===0){
            console.log("FIZZ");
        }else{
            console.log(i);
        }
    }

}

FizzBuzz();
```
!******************************************************************************************************
8.write code to find anagram
```
function isAnagram(str1,str2) {
    return console.log(format(str1)===format(str2));
}

function format(str) {

    return str.replace(/[^\w]/g,'').toLowerCase().split('').sort().join('');

}

isAnagram("elbow","below");
isAnagram("dormitory","dirtyroom");
```
!******************************************************************************************************
9.write code to find longest word
```
function longestWordWithReduce(str){
    var finalStr=str.split(' ').reduce(function (accumulatedValue,currentValue) {

        return accumulatedValue.length > currentValue.length?accumulatedValue :currentValue;

    },'');

    return finalStr;

}

//longestword("I am awesome ");

console.log(longestWordWithReduce("I am Awesome"));
```

!******************************************************************************************************
10.write code to find duplicates in array

```
function findDuplicate(arr) {
    const result = arr.filter((value, index, array) => array.indexOf(value) !== index);
    return result;
}
function findDuplicatesinArray(arr){

    let output=arr.filter(function (elem,index) {

       return arr.indexOf(elem)!==index ;

    });

    return output;

}
let a=[1,2,2,2,3,4,5,5,6];
console.log(findDuplicatesinArray(a));
```
!******************************************************************************************************
10.write code to remove duplicates in array
```
function removeDuplicates(arr) {
    let newList = [];

    let output = arr.filter(function (elem, index) {

        if (arr.indexOf(elem) === index) {
            return newList.push(elem);
        }
    });

    return output;
}
let b=[1,2,2,2,3,4,5,5,6];
console.log(removeDuplicates(b));
```
!******************************************************************************************************
12.write code to chunk the array and flatten the array
```
function chunkArrayIntoPieces(array,chunkLength) {
    let chunkedArray=[];
    let i=0;

    while(i<array.length){

        chunkedArray.push((array.slice(i,i+chunkLength)))

        i+=chunkLength;

    }
    return console.log(chunkedArray);
}

chunkArrayIntoPieces([1,2,3,4,5,6,7,8,9,0],3);
```
!******************************************************************************************************
13.write code to flatten the array
```
function flattenArray(arr){
   let output= arr.reduce(function (a,b) {
         return a.concat(b);
    }) ;

    return output;
}


console.log(flattenArray([[1,2],[3,4]]));

```
!******************************************************************************************************


14.Capitalize  first letters of sentence
```
function capitalizeFirstLetters(str){

    return str.toLowerCase().split(' ').map(function (word) {

        return word[0].toUpperCase()+word.substring(1);

    }).join(' ');
}

Using regExp
```
function capitalizeUsingRegularExpression(str) {
    const output=str.replace(/\b[a-z]/gi,function(char){
        return char.toUpperCase();
    });

    return console.log(output)
}

console.log(capitalizeFirstLetters("I am amazing"))
```
!******************************************************************************************************

15.circular letter change a-b or  z to a

```
function circularLetterChange(word) {
    let value=word.toLowerCase().replace(/[a-z]/gi,function (word) {
        if(word==='z' || word ==="Z"){
            return 'a'
        }
        else{
          return  String.fromCharCode((word.charCodeAt()+1))
        }
    });


   return value;
}

console.log(circularLetterChange("abcd"));

```
!******************************************************************************************************


16.create permutatation of strings
```
function allPermutationofArrayElements(inputArray){
    let result = inputArray.reduce(function permute(res, item, key, arr) {
        return res.concat(arr.length > 1 && arr.slice(0, key).
            concat(arr.slice(key + 1)).
            reduce(permute, []).
            map(function(perm) {
                return [item].concat(perm);
            }) || item);
    }, []);
  return result;

}



function  allPermArr(input) {
    let permArr = [],
        usedChars = [];
    let i, ch;
    for (i = 0; i < input.length; i++) {
        ch = input.splice(i, 1)[0];
        usedChars.push(ch);
        if (input.length == 0) {
            permArr.push(usedChars.slice());
        }
        allPermArr(input);
        input.splice(i, 0, ch);
        usedChars.pop();
    }
    return permArr;

}

var inputArray = [1, 2, 3];

console.log(allPermutationofArrayElements(inputArray));
console.log(allPermArr(inputArray));
```
!******************************************************************************************************
17.Ends with word
```
function confirmEnding(str, target) {
    var isTrue=str.substr(-target.length)===target;
    if(isTrue){
        return true;
    }else{
        return false;
    }
}

confirmEnding("Bastian", "n");
```
!******************************************************************************************************

//18.max character in word
```
function maxCharacter(str) {
    const charMap = {};
    let max = 0;
    let maxChar = '';

    for (let char of str) {
        if (charMap[char]) {
            charMap[char]++;
        } else {
            charMap[char] = 1;
        }
    }

    for (let char in charMap) {
        if (charMap[char] > max) {
            max = charMap[char];
            maxChar = char;
        }
    }

    return console.log(maxChar);
}



maxCharacter("Ramanath")
```
!******************************************************************************************************

19.Repeat strings number of times
```
function repeatStringNumTimes(string, times) {
    //Step 1. If times is positive, return the repeated string
    if (times > 0) { // (3 > 0) => true
        return string.repeat(times); // return "abc".repeat(3); => return "abcabcabc";
    }

    //Step 2. Else if times is negative, return an empty string if true
    else {
        return "";
    }
}
```
```
function repeatStringNumberTimes(str, num) {
    return num < 0 ? "": new Array(num + 1).join(str);
}
```
```
function repeatStrings(str, num) {
    let repeatedStrings = '';
    while (num > 0) {
        repeatedStrings += str;
        num--;
    }

    return repeatedStrings;
}

console.log(repeatStrings("hi", 5));
```
//******************************************************************************************************
```20.//First letter of sentence should be capital letter

 function titleCase(str) {
    return str.toLowerCase().split(' ').map(function(word) {
         return word.replace(word[0], word[0].toUpperCase());
    }).join(' ');
 }
 titleCase("I'm a little tea pot");
```
******************************************************************************************************







