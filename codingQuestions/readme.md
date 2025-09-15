---

# 🚀 JavaScript Interview Questions 2025

A collection of frequently asked **JavaScript coding interview questions** with explanations and solutions.

---

## 1. Check if a Number is Prime

```js
function isPrime(num) {
    if (num <= 1) return false;
    for (let i = 2; i < num; i++) {
        if (num % i === 0) return false;
    }
    return true;
}

console.log(isPrime(7)); // true
```

---

## 2. Find Sum of an Array

```js
function sumArray(arr) {
    let sum = 0;
    for (let i = 0; i < arr.length; i++) {
        sum += arr[i];
    }
    return sum;
}

console.log(sumArray([15, 6, 10, 2])); // 33
```

---

## 3. Fibonacci Sequence up to `n` Terms

```js
function fibonacci(n) {
    let num1 = 0, num2 = 1, nextNum;

    console.log("Fibonacci Sequence:");
    for (let i = 1; i <= n; i++) {
        console.log(num1);
        nextNum = num1 + num2;
        num1 = num2;
        num2 = nextNum;
    }
}

fibonacci(7);
```

---

## 4. Factorial of a Number

```js
function factorial(num) {
    let answer = 1;
    for (let i = 2; i <= num; i++) {
        answer *= i;
    }
    return answer;
}

console.log(factorial(7)); // 5040
```

---

## 5. Power of a Number

```js
function power(base, exponent) {
  return base ** exponent;
}
console.log(power(3, 4)); // 81
```

---

## 6. Frequency of Elements in Array

```js
function frequency(arr) {
    const freq = {};
    for (let i = 0; i < arr.length; i++) {
        freq[arr[i]] = (freq[arr[i]] || 0) + 1;
    }
    return freq;
}

console.log(frequency([1, 1, 2, 3, 3, 4]));
// { '1': 2, '2': 1, '3': 2, '4': 1 }
```

---

## 7. Count Occurrences of a Character in String

```js
function countChar(str, char) {
  return str.split(char).length - 1;
}
console.log(countChar('GeeksForGeeks', 'G')); // 2
```

Alternative:

```js
function countChar(str, char) {
    let count = 0;
    for (let i = 0; i < str.length; i++) {
        if (str[i] === char) count++;
    }
    return count;
}

console.log(countChar('GeeksForGeeks', 'G')); // 2
```

---

## 8. Sort Array (Ascending)

```js
function sortArray(arr) {
    for (let i = 0; i < arr.length; i++) {
        for (let j = i + 1; j < arr.length; j++) {
            if (arr[i] > arr[j]) {
                [arr[i], arr[j]] = [arr[j], arr[i]];
            }
        }
    }
    return arr;
}

console.log(sortArray([5, 3, 8, 1])); // [1, 3, 5, 8]
```

---

## 9. Sort Array (Descending)

```js
function sortArrayDesc(arr) {
    let n = arr.length;
    for (let i = 0; i < n - 1; i++) {
        for (let j = 0; j < n - 1 - i; j++) {
            if (arr[j] < arr[j + 1]) {
                [arr[j], arr[j + 1]] = [arr[j + 1], arr[j]];
            }
        }
    }
    return arr;
}

console.log(sortArrayDesc([5, 3, 8, 1])); // [8, 5, 3, 1]
```

---

## 10. Check Even or Odd

```js
function isEven(num) {
    return num % 2 === 0;
}
console.log(isEven(10)); // true
```

---

## 11. Find Minimum in Array

```js
function findMin(arr) {
    let min = arr[0];
    for (let i = 1; i < arr.length; i++) {
        if (arr[i] < min) min = arr[i];
    }
    return min;
}

console.log(findMin([5, 10, -1, 8])); // -1
```

---

## 12. Find Longest Word in a String

```js
function longestWord(str) {
    const words = str.split(' ');
    let longest = '';
    for (let word of words) {
        if (word.length > longest.length) {
            longest = word;
        }
    }
    return longest;
}

console.log(longestWord('GeeksForGeeks is great')); // GeeksForGeeks
```

---

## 13. Map Function Example

```js
let numbers = [5, 6, 7];
let ans = numbers.map(num => num * 2);
console.log(ans); // [10, 12, 14]
```

---

## 14. JSON Parse & Stringify

```js
let jsonData = '{"name": "Geeks"}';
let parsedData = JSON.parse(jsonData);
console.log(parsedData.name); // Geeks
```

---

## 15. Convert String to Array of Words

```js
let sentence = "Geeks For Geeks";
let wordsArray = sentence.split(" ");
console.log(wordsArray); // [ 'Geeks', 'For', 'Geeks' ]
```

---

## 16. Check if Two Strings are Anagrams

```js
function areAnagrams(str1, str2) {
    if (str1.length !== str2.length) return false;

    let count1 = {}, count2 = {};
    for (let char of str1) count1[char] = (count1[char] || 0) + 1;
    for (let char of str2) count2[char] = (count2[char] || 0) + 1;

    for (let char in count1) {
        if (count1[char] !== count2[char]) return false;
    }
    return true;
}

console.log(areAnagrams("listen", "silent")); // true
```

---

## 17. Remove Duplicates from Array

```js
function removeDuplicates(arr) {
  const uniqueArray = [];
  for (let i = 0; i < arr.length; i++) {
      if (!uniqueArray.includes(arr[i])) {
          uniqueArray.push(arr[i]);
      }
  }
  return uniqueArray;
}

console.log(removeDuplicates([5, 2, 5, 6, 6, 7])); // [5, 2, 6, 7]
```

---

## 18. Count Vowels in String

```js
function countVowels(str) {
    let count = 0;
    const vowels = 'aeiouAEIOU';
    for (let i = 0; i < str.length; i++) {
        if (vowels.includes(str[i])) count++;
    }
    return count;
}

console.log(countVowels("hello geek")); // 4
```

---

## 19. Unique Characters from a String

```js
function uniqueCharacters(str) {
    const uniqueChars = [];
    for (let i = 0; i < str.length; i++) {
        if (!uniqueChars.includes(str[i])) {
            uniqueChars.push(str[i]);
        }
    }
    return uniqueChars.join('');
}

console.log(uniqueCharacters("geeksforgeeks")); // geksfor
```

---

## 20. Magic EdTech Question (Merge Objects by ID)

```js
let dummyObject = [
  {id:0,fname:'a'},
  {id:0,mname:'b'},
  {id:0,lname:'c'},
  {id:1,fname:'a1'},
  {id:1,mname:'b1'},
  {id:1,lname:'c1'},
  {id:2,fname:'a2'},
  {id:2,mname:'b2'},
  {id:2,lname:'c2'}
];

let result = [];
dummyObject.forEach(obj => {
  let existing = result.find(item => item.id === obj.id);
  if (existing) {
    Object.assign(existing, obj);
  } else {
    result.push({...obj});
  }
});

console.log(result);
/*
[
  {id:0, fname:'a', mname:'b', lname:'c'},
  {id:1, fname:'a1', mname:'b1', lname:'c1'},
  {id:2, fname:'a2', mname:'b2', lname:'c2'}
]
*/
```

---

## 21. Tricky JS Questions

### Floating Point Precision

```js
let x = 0.1 + 0.2;
let y = 0.3;
console.log(x === y); // false
```

### Comparison Quirk

```js
let x = 1 > 2 > 3;
console.log(x); // false
```

---

## 22. querySelector Examples

```js
// Select element by id
document.querySelector("#myId");

// Select first element with class
document.querySelector(".myClass");

// Select nested element
document.querySelector("div > p");
```

---


