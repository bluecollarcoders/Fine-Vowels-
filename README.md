# Find-Vowels-

## Problem

We want to know the index of the vowels in a given word, for example, there are two vowels in the word super (the second and fourth letters).

So given a string "super", we should return a list of [2, 4].

Some examples:
Mmmm  => []
Super => [2,4]
Apple => [1,5]
YoMama -> [1,2,4,6]
NOTES
Vowels in this context refers to: a e i o u y (including upper case)
This is indexed from [1..n] (not zero indexed!)

## Solution 1
```javascript
const vowelIndices = (word) => {
 var newArray = [];
 var index = word.split('');
  for(let i = 0; i < word.length; i++) {
    if (/[aeuoiy]/gi.test(index[i])) {
      newArray.push(i + 1)
    }
  }
  return newArray;
};
```

## Solution 2
```javascript
const vowelIndices = (word) => {
 var newArray = [];
 var vowels = ['a', 'e', 'i', 'o', 'u', 'y', 'A', 'E', 'I', 'O', 'U', 'Y'];
  for(let i = 0; i < word.length; i++) {
    if (vowels.indexOf(word[i]) != -1) {
      newArray.push(i + 1)
    }
  }
  return newArray;
};
```
