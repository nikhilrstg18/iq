# Top 7 time complexity

> Time complexities that every programmer should know


## Big O

**O(n) - time complexity**
> estimates how an algorithm performs regardless of the kind of machine it runs on. 
> 
> You can get the time complexity by “counting” the number of operations performed by your code (operations performed for given input of size n).

- This time complexity is defined as a function of the input size `n` using Big-O notation. 
- `n` indicates the input size, while `O` is the worst-case scenario growth rate function 


![Lexical Environment](./assets/img/dsa-1.png)

---

## Big O CheetSheet


| Big O Notation   | Time Complexity | Example(s)                                                                     | Pririoty of Usage |
| ---------------- | --------------- | ------------------------------------------------------------------------------ | ----------------- |
| O(1)             | Linear          | [OddEven or dictionary lookup](#o1-contant-time-complexity)                    | 1                 |
| O(log n)         | Logarithmic     | [Binary Search on sorted array](#olog-n--logarithmic-time-complexity)          | 2                 |
| O(n)             | Constant        | [Find max element in sorted array](#on--linear-time-complexity)                | 3                 |
| O(n log n)       | Linearithmic    | [Merge Sort an array](#on-log-n--linearithmic-time-complexity)                 | 4                 |
| O(n<sup>2</sup>) | Quadratic       | [Bubble Sort](#onsup2sup--quadratic-time-complexity)                           | 5                 |
| O(2<sup>n</sup>) | Exponential     | [Find all subsets](#o2supnsup--exponential-time-complexity)                    | 6                 |
| O(n!)            | Factorial       | [Find all permutation of a given set / string](#on--factorial-time-complexity) | 7                 |


❓ *What is a good code?*
> Readable and Scalable
   1. Speed (Operations) - measured by **O(n)** aka **Time Complexity**
   2. Memory (Ram) - measured by **O(s)** aka **Space Complexity**
      1. There is a tradeoff between Space and Time
         1. You want to go faster than you might need to sacrifice more memory
         2. You want to save on 
> Space Complexity
   1. When a program executes it has 2 things to remember things
      1. Heap 
      2. Stack - keep track of functional calls
   2. What causes space complexity?
      1. Variables
      2. Data structures
      3. Function call
      4. Allocations
> What are 3 pillars of good code?
   1. Readability
   2. Space Complexity
   3. Time Complexity

---
## Simplifying Big O

- Always consider worst case
- Remove constants
- Different term for inputs
- Drop non-dominents

## Calculating Big O

## O(1): Contant Time Complexity

eg 1 
```javascript
function isEvenOrOdd(n) {
  return n % 2 ? 'Odd' : 'Even'; // <-- only 1 operation
}
```

eg 1.1
```javascript
const dictionary = {the: 22038615, be: 12545825, and: 10741073, of: 10343885, a: 10144200, in: 6996437, to: 6332195 /* ... */};

function getWordFrequency(dictionary, word) {
  return dictionary[word]; // <-- only 1 operation
}
```

> Big O calculation

Analysis of input size at each iteration of Binary Search:

| Number of operation ( No Iteration ) | length of input array |
| ------------------------------------ | --------------------- |
| 1                                    | n                     |

Also, for any length of the array , number of operations performed is 1.

=> 1 = k

Applying Big O function, dropping and constants on LHS will give number of operations performed by algorithm with input size of n:

=> O(1) = k 

- Time Complexity of eg 1 and eg 1.1 -> **O(1)** : Constant ( **as 'n' grows time complexity remains constant**)
- In other words, Run time is independent of the input size of the problem.


## O(log n) : Logarithmic Time Complexity

eg 2
```javascript
function indexOf(array, element, offset = 0) {
  // split array in half
  const half = parseInt(array.length / 2);
  const current = array[half];

  if(current === element) {
    return offset + half;
  } else if(element > current) {
    const right = array.slice(half);
    return indexOf(right, element, offset + half);
  } else {
    const left = array.slice(0, half)
    return indexOf(left, element, offset);
  }
}

// Usage example with a list of names in ascending order:
const directory = ["Adrian", "Bella", "Charlotte", "Daniel", "Emma", "Hanna", "Isabella", "Jayden", "Kaylee", "Luke", "Mia", "Nora", "Olivia", "Paisley", "Riley", "Thomas", "Wyatt", "Xander", "Zoe"];
console.log(indexOf(directory, 'Hanna'));   // => 5
console.log(indexOf(directory, 'Adrian'));  // => 0
console.log(indexOf(directory, 'Zoe'));     // => 18

}
```

> Big O calculation

Analysis of input size at each iteration of Binary Search:

| Number of operation ( Iteration ) | length of input array |
| --------------------------------- | --------------------- |
| 1st                               | n                     |
| 2nd                               | n / 2                 |
| 3rd                               | n / 2<sup>2</sup>     |
| :                                 | :                     |
| kth                               | n / 2<sup>k</sup>     |

Also, we know that after After k iterations, the length of the array becomes 1 (base case) Therefore, the Length of the array

=> n / 2<sup>k</sup> = 1

=>  n = 2<sup>k<sup>

Applying log<sub>2</sub> function on both sides: 

=>  log<sub>2</sub> n = log<sub>2</sub> 2<sup>k<sup>

=>  log<sub>2</sub> n = k log<sub>2</sub> 2

=>  log<sub>2</sub> n = k  [ cuz log<sub>a</sub> a = 1]

Applying Big O function, dropping and constants on LHS will give number of operations performed by algorithm with input size of n:

=> O(log n) = k 

- Time Complexity in eg 2 -> **O(log n)** : Linear (**as soon as 'n' grows time complexity grows  too but in logarithmic trends**)
- In other words, When a big problem is solved by transforming it into a smaller size by some constant fraction.

## O(n) : Linear Time Complexity

eg 3
```javascript
function findMax(n) {
  let max;
  let counter = 0;

  for (let i = 0; i < n.length; i++) {
    counter++;
    if(max === undefined || max < n[i]) {
      max = n[i];
    }
  }

  console.log(`n: ${n.length}, counter: ${counter}`);
  return max;
}
```
eg 3.1

```javascript
function printUpAndDown(n: number) {
    console.log("Going up");
    for (let i = 0; i < n; i++) {
        console.log(i);
    }
    console.log("Going down");
    for (let j = n - 1; j > 0; j--) {
        console.log(j);
    }
}
```

> Big O calculation

Analysis of input size at each iteration of Binary Search:

| Number of operation ( Iteration ) | length of input array |
| --------------------------------- | --------------------- |
| 1st                               | n                     |
| 2nd                               | n-1                   |
| 3rd                               | n-2                   |
| :                                 | :                     |
| kth                               | n-(k-1)               |

Also, we know that after After k iterations, the length of the array becomes 0 (base case) Therefore, the Length of the array

=> n -k + 1 = 0

=> n + 1 = k

Applying Big O function, dropping and constants on LHS will give number of operations performed by algorithm with input size of n:

=> O(n) = k

- Time Complexity in eg 3 and eg 3.1 -> **O(n)** : Linear (**as soon as 'n' grows time complexity grows too but in linear trends**)
- In other words, the problem requires a small amount of processing time for each element in the input
- In eg 3.1 May be thinking O(2n) but we see the big picture! BigONotation doesn't care about precision only about general trends and remove constants


## O(n log n) : Linearithmic Time Complexity

eg 4
```javascript
/**
 * Sort array in asc order using merge-sort
 * @example
 *    sort([3, 2, 1]) => [1, 2, 3]
 *    sort([3]) => [3]
 *    sort([3, 2]) => [2, 3]
 * @param {array} array
 */
function sort(array = []) {
  const size = array.length;
  // base case
  if (size < 2) {
    return array;
  }
  if (size === 2) {
    return array[0] > array[1] ? [array[1], array[0]] : array;
  }
  // slit and merge
  const mid = parseInt(size / 2, 10);
  return merge(sort(array.slice(0, mid)), sort(array.slice(mid))); // <-- O(log n)
}

/**
 * Merge two arrays in asc order
 * @example
 *    merge([2,5,9], [1,6,7]) => [1, 2, 5, 6, 7, 9]
 * @param {array} array1
 * @param {array} array2
 * @returns {array} merged arrays in asc order
 */
function merge(array1 = [], array2 = []) {
  const merged = [];
  let array1Index = 0;
  let array2Index = 0;
  // merge elements on a and b in asc order. Run-time O(a + b)
  while (array1Index < array1.length || array2Index < array2.length) {  // <-- O(n)
    if (array1Index >= array1.length || array1[array1Index] > array2[array2Index]) {
      merged.push(array2[array2Index]);
      array2Index += 1;
    } else {
      merged.push(array1[array1Index]);
      array1Index += 1;
    }
  }
  return merged;
}
```
> Big O calculation 

As we already know that when a algorithm is breaking the input into half in `sort()` 
(Worst case) : O(log n)
As iterating over a list is linear (Worst case): O(n)

So overall operation would be

=> O(log n) + O(n) = k

=> O(n log n) = k

- Time Complexity in eg 4 -> **O(n log n)** : Linearithmic ( **as soon as n grows time complexity grows too but in linearithmic trends**)
- In other words, when a problem is broken into smaller subproblems, solving them independently, and combining the solutions 

## O(n<sup>2</sup>) : Quadratic Time Complexity

eg 5
```javascript
function sort(n) {
  for (let outer = 0; outer < n.length; outer++) {
    let outerElement = n[outer];

    for (let inner = outer + 1; inner < n.length; inner++) {
      let innerElement = n[inner];

      if(outerElement > innerElement) {
        // swap
        n[outer] = innerElement;
        n[inner] = outerElement;
        // update references
        outerElement = n[outer];
        innerElement = n[inner];
      }
    }
  }
  return n;
}
```

> Big O calculation 

This will have a quadratic time look-up since the function is looking at a every index in the array twice:

=> n<sup>2</sup> = k

Applying Big O function, dropping and constants on LHS will give number of operations performed by algorithm with input size of n:

O(n<sup>2</sup>) = k 

- Time Complexity in eg 5 -> **O(n<sup>2</sup>)** : Quadratic ( **as soon as n grows time complexity grows too but in quadratic trends**)


## O(2<sup>n</sup>) : Exponential Time Complexity

eg 6
```javascript
function powerset(n = '') {
  const array = Array.from(n);
  const base = [''];

  const results = array.reduce((previous, element) => {
    const previousPlusElement = previous.map(el => {
      return `${el}${element}`;
    });
    return previous.concat(previousPlusElement);
  }, base);

  return results;
}

powerset('') // ...
// n = 0, f(n) = 1;
powerset('a') // , a...
// n = 1, f(n) = 2;
powerset('ab') // , a, b, ab...
// n = 2, f(n) = 4;
powerset('abc') // , a, b, ab, c, ac, bc, abc...
// n = 3, f(n) = 8;
powerset('abcd') // , a, b, ab, c, ac, bc, abc, d, ad, bd, abd, cd, acd, bcd...
// n = 4, f(n) = 16;
powerset('abcde') // , a, b, ab, c, ac, bc, abc, d, ad, bd, abd, cd, acd, bcd...
// n = 5, f(n) = 32;
```
- Time Complexity in eg 6 -> **O(2<sup>n</sup>)** : Exponenetial ( **as soon as n grows time complexity grows too but in exponential trends**)

## O(n!) : Factorial Time Complexity

eg 7
```javascript
function getPermutations(string, prefix = '') {
  if(string.length <= 1) {
    return [prefix + string];
  }

  return Array.from(string).reduce((result, char, index) => {
    const reminder = string.slice(0, index) + string.slice(index+1);
    result = result.concat(getPermutations(reminder, prefix + char));
    return result;
  }, []);
}
getPermutations('ab') // ab, ba...
// n = 2, f(n) = 2;
getPermutations('abc') // abc, acb, bac, bca, cab, cba...
// n = 3, f(n) = 6;
getPermutations('abcd') // abcd, abdc, acbd, acdb, adbc, adcb, bacd...
// n = 4, f(n) = 24;
getPermutations('abcde') // abcde, abced, abdce, abdec, abecd, abedc, acbde...
// n = 5, f(n) = 120;
```
- Time Complexity in eg 7 -> **O(n!)** : Factorial ( **as soon as n grows time complexity grows too but in quadratic trends**)

---