// Anonymous function and IIFE

//odd numbers in array
const array=[1, 2, 3, 4, 5, 6, 7, 8, 9];
array.forEach(function(num) {
    if (num%2!==0) {
        console.log(num);
    }
});

//convert all string to title caps
function Title(str){
    return str.replace(/\w\S*/g, function(txt){
        return txt.charAt(0).toUpperCase() + txt.substr(1).toLowerCase();
    });
}
let Arr= ["hello", "welcome", "to","guvi"];
let title=Arr.map(Title);
console.log(title);

//sum of elements in array
function sumOf(numbers) {
    let sum = 0;
    for (let i = 0; i < numbers.length; i++) {
        sum += numbers[i];
    }
    return sum;
}
let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let sums = sumOf(numbers);
console.log(sums);

//prime numbers in a array
function Prime(number){
    if (number <= 1) {
        return false;
    }
    for (let i = 2; i <= Math.sqrt(number); i++) {
        if (number % i === 0) {
            return false;
        }
    }
    return true;
}
function Primes(numbers) {
    return numbers.filter(function (number) {
        return Prime(number);
    });
}
let number= [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let primeNumbers = Primes(number);
console.log(primeNumbers);

//palindrome in array
let stringsArray = ["guvi", "mom", "wow", "world","malayalam", "radar"];
function isPalindrome(str) {
    const reversedStr=str.split('').reverse().join('');
    return str === reversedStr;
}
let palindrome=stringsArray.filter(function (str) {
    return isPalindrome(str);
});
console.log(palindrome);

//remove duplicates from array
let array= [1,1,2,3,4,4,5,6,7,7,8,9,0,0];
let Duplicate= (arr => [...new Set(arr)])(array);
console.log(Duplicate);

//Rotate array by k times
function rotateArray(arr, k) {
    let Part=arr.slice(-k);
    let remaining=arr.slice(0,arr.length-k);
    let rotated=Part.concat(remaining);
    return rotated;
}
let originalArray = [1, 2, 3, 4, 5];
let k = 2;
let rotated= rotateArray(originalArray, k);
console.log(rotated);


//arrow functions
//print odd numbers in array

let numbersArray = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
numbersArray.forEach(num => {
    if (num % 2 !== 0) {
        console.log(num);
    }
});

//convert all string to title caps
let Arr= ["hello","welcome","to","guvi"];
let upper=Arr.map(str => str.replace(/\b\w/g,char => char.toUpperCase()));
console.log(upper);

//sum of all numbers in a array
let Arr=[1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
let sum=Arr.reduce((acc,num)=>acc+num,0);
console.log(sum);

//return prime numbers in a array
const isPrime=num => {
    if (num < 2){
        return false;
    }
    for (let i=2;i<=Math.sqrt(num);i++){
        if (num%i===0) {
            return false;
        }
    }
    return true;
};
const Arr= [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
const prime=Arr.filter(num => isPrime(num));
console.log(prime);

//palindrome in given array
const isPalindrome = str =>{
    const reversedStr=str.split('').reverse().join('');
    return str === reversedStr;
};
const Arr= ["malayalam","mom","hello","guvi"];
const palindrome=Arr.filter(str=> isPalindrome(str));
console.log(palindrome);