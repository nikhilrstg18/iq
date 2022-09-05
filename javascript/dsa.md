# JS DSA


## Big O

**O(n) - time complexity**
> estimates how an algorithm performs regardless of the kind of machine it runs on. 
> 
> You can get the time complexity by “counting” the number of operations performed by your code (operations performed for given input of size n).

- This time complexity is defined as a function of the input size `n` using Big-O notation. 
- `n` indicates the input size, while `O` is the worst-case scenario growth rate function 


![Lexical Environment](./assets/img/dsa-1.png)

---

### Big O CheetSheet
<style>.heatMap {
        text-align: left;
        
    }
    .heatMap tr:nth-child(1) td:nth-child(1),
    .heatMap tr:nth-child(1) td:nth-child(2) { background: #E8F5E9; color :black; }
    .heatMap tr:nth-child(2) td:nth-child(1) ,
    .heatMap tr:nth-child(2) td:nth-child(2) { background: #E8F5E9; color :black; }
    .heatMap tr:nth-child(3) td:nth-child(1) ,
    .heatMap tr:nth-child(3) td:nth-child(2) { background: #E8F5E9; color :black; }
    .heatMap tr:nth-child(4) td:nth-child(1) ,
    .heatMap tr:nth-child(4) td:nth-child(2) { background: #E8F5E9; color :black; }
    .heatMap tr:nth-child(5) td:nth-child(1) ,
    .heatMap tr:nth-child(5) td:nth-child(2) { background: #FFF3E0; color :black; }
    .heatMap tr:nth-child(6) td:nth-child(1) ,
    .heatMap tr:nth-child(6) td:nth-child(2) { background: #FFEBEE; color :black; }
    .heatMap tr:nth-child(7) td:nth-child(1) ,
    .heatMap tr:nth-child(7) td:nth-child(2) { background: #FFEBEE; color :black; }
</style>
<div class="heatMap">

| Big O Notation   | Time Complexity | Example(s)                                   | Pririoty of Usage |
| ---------------- | --------------- | -------------------------------------------- | ----------------- |
| O(1)             | Linear          | Odd or Even<br/> dictionary lookup           | 1                 |
| O(log n)         | Logarithmic     | Binary Search on sorted array                | 2                 |
| O(n)             | Constant        | Find max element in sorted array             | 3                 |
| O(n log n)       | Linearithmic    | Merge Sort an array                          | 4                 |
| O(n<sup>2</sup>) | Quadratic       | Bubble Sort                                  | 5                 |
| O(2<sup>n</sup>) | Exponential     | Find all subsets                             | 6                 |
| O(n!)            | Factorial       | Find all permutation of a given set / string | 7                 |

</div>

❓ *What is a Good code?*
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

### Calculating Big O

#### O(1): Contant Time Complexity

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

- Time Complexity of eg 1 and eg 1.1 -> **O(1)** : Constants ( **as 'n' grows time complexity remains constant**)
- In other words, Run time is independent of the input size of the problem.


#### O(log n)

eg 2
```javascript
function indexOf(array, element, offset = 0) {
  // split array in half
  const half = parseInt(array.length / 2);          // <-- 1
  const current = array[half];                      // <--

  if(current === element) {
    return offset + half;
  } else if(element > current) {                    // <-- 2.1
    const right = array.slice(half);
    return indexOf(right, element, offset + half);  // <-- 3.1
  } else {                                          // <-- 2.2
    const left = array.slice(0, half)
    return indexOf(left, element, offset);          // <-- 3.2
  }
}

// Usage example with a list of names in ascending order:
const directory = ["Adrian", "Bella", "Charlotte", "Daniel", "Emma", "Hanna", "Isabella", "Jayden", "Kaylee", "Luke", "Mia", "Nora", "Olivia", "Paisley", "Riley", "Thomas", "Wyatt", "Xander", "Zoe"];
console.log(indexOf(directory, 'Hanna'));   // => 5
console.log(indexOf(directory, 'Adrian'));  // => 0
console.log(indexOf(directory, 'Zoe'));     // => 18

}
```

See calculation 👉 [view](https://www.geeksforgeeks.org/complexity-analysis-of-binary-search/)

- Time Complexity in eg 2 -> **O(log n)** : Linear (**as soon as 'n' grows time complexity grows  too but in logarithmic trends**)
- In other words, When a big problem is solved by transforming it into a smaller size by some constant fraction.

#### O(n)

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

- Time Complexity in eg 3 and eg 3.1 -> **O(n)** : Linear (**as soon as 'n' grows time complexity grows too but in linear trends**)
- In other words, the problem requires a small amount of processing time for each element in the input
- In eg 3.1 May be thinking O(2n) but we see the big picture! BigONotation doesn't care about precision only about general trends and remove constants

#### O(n<sup>2</sup>) : Quadratic Time Complexity

eg 4
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
- Time Complexity in eg 4 -> **O(n<sup>2</sup>)** : Quadratic ( **as soon as n grows time complexity grows too but in quadratic trends**)
- 
#### O(n log n) : Linearithmic Time Complexity

eg 5
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
  return merge(sort(array.slice(0, mid)), sort(array.slice(mid)));
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
  while (array1Index < array1.length || array2Index < array2.length) {
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
- Time Complexity in eg 4 -> **O(n log n)** : Linearithmic ( **as soon as n grows time complexity grows too but in linearithmic trends**)
- In other words, when a problem is broken into smaller subproblems, solving them independently, and combining the solutions 


#### O(2<sup>n</sup>) : Exponential Time Complexity

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

#### O(n!) : Factorial Time Complexity

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

### Simplifying Big O

### CheetSheet

---

## How to solve coding problems

How to Tackle Coding Interview with 15 steps

1. When the interviewer says the question; **Write down key points on the top (sorted, array, etc.)**
   1. Make sure you have all the details.
   2. Show how organized you are.
2. **Double check**: 
   1. What are the inputs? 
   2. What are the outputs?
3. **What is most important value of the problem?** 
   1. What you want to focus on time or  space. 
   2. What is the mail goal?
4. Don't be annoying asking too many questions.
5. **Start with naive/brute force approach.**
   2. First thing that comes into your mind
   3. It that you are able to thinks well and critically 
   4. You don't even need to write the code, just speak about it.
6. **Tell them why your first approach is not the best** (i.e. O(n2) or higher, readability, etc.)
7.  **Walk-through your approach, comment things and see where you may be able to break things**
    1.  Any Repeatetion, bottleneck(s) or any unnecessary work done?
8.  **Before you start coding walk through your code, write down the steps that you're going to do** 
    1.  Tip: create a recipe before actually dive into cooking
9.  **Modularize your code from the very beginning.**
    1.  Break down your code into very small bits and pieces
    2.  Just add comments if you need to 
10. Start actually writing your code now.
    1.  Keep in mind that the more you prepare and what you need to code, the better the whiteboard.
    2.  So never start a white board interview not being sure how things are going to workout  
11. **Think about the error checks and how you can break this code**
    1.  Never make assumptions about inputs.
    2.  Assume people are trying to break your code
    3.  How will you safeguard it?
    4.  Tip: Always check false input that you don't want. 
12. **Don't use Bad/Confusing names like i, j, map, etc**.
    1.  Write code that reads well.
13. **Test your code**: 
    1.  Check for no params, 0, undefined, null, massive arrays, async code, etc.
14. Finally talk to the interviewer, where you would improve the code.
    1.  Does it work ?
    2.  Is it readable ?
    3.  Are there different approaches ?
15. If you interviewer is happy with your code, interview usually ends here. It's common that interviewer usually asks extension questions, like 
    a. How will you handle the problem if the whole input is too large to fit into memory? Start talking about the Space Complexity

❓ *Do I Need to go through this kind of analysis to solve problem in everyday life ?*

- **No**, above points demonstrate the thought process the good developers have, and what companies are looking for.

- If You are able to think clearly thru aforesaid steps and you are able to solve problems this way, You'll see how impressive is this instead of just writing the solution

- Even if by end of time, you are not able to solve the problem. You have demonstrated the ability to think like an engineer to you interviewer and these are the skills which are rare and companies like to hire for

---

# Data Structures

---

## Array

### Static 
### Dynamic - LinkedList
---

## Hashtable
---

## Stack
---

## Queue
---

## Trees
---

## Graphs

---

# Algorithms
---

## Recursion

---

## Sorting

### Sort
### QuickSort
### Heap Sort
### Bubble Sort
### Selection Sort
### Insertion Sort
### Merge Sort
### Counting Sort
### Bucket Sort
### ShellSort
### Comb Sort
### Pigeonhole Sort
### Cycle Sort

---

## Searching

### Linear Search
### Binary Search
### Jump Search
### Interpolation Search
### Exponential Search
### Ternary Search
---

## Divide and Conquer

---

## Dynamic Programming

---

## Backtracking 