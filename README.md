# Merge Sort Generator 🧩

A simple JavaScript module that sorts arrays using the Merge Sort algorithm through recursive methods.

## What is Merge Sort?

- **Merge Sort** is a divide-and-conquer algorithm that divides the input array into two halves, recursively sorts each half, and then merges the sorted halves to produce the sorted array.
- It is known for its efficiency and stability, making it a popular choice for sorting large datasets.

## The Takeaway

Creating the Merge Sort Generator helped me understand different ways to solve the same problem. By implementing the merge sort algorithm, I learned about the strengths of recursive approaches and how to efficiently handle array operations in JavaScript.

**Key points:**

- **Divide and Conquer:** Split the array into smaller subarrays, sort them individually, and then merge them back together in order.
  
- **Recursive Method:** Utilized recursion to break down the problem into smaller, more manageable parts, enhancing my grasp of recursive thinking in JavaScript.
  
- **Code Clarity:** Balanced clear and readable code with performance considerations, ensuring the implementation is both understandable and efficient.
  
- **Problem-Solving:** Enhanced my ability to approach sorting problems methodically and implement effective solutions using algorithmic strategies.

Overall, this project improved my skills in algorithm design, recursive programming, and writing clean and efficient JavaScript code.

## Usage

```javascript
// Merge Function
function merge(left, right) {
  const sorted = [];

  while (left.length > 0 && right.length > 0) {
    sorted.push(left[0] <= right[0] ? left.shift() : right.shift());
  }

  return sorted.concat(left, right);
}

// Merge Sort Function
function mergeSort(arr) {
  if (arr.length <= 1) return arr;

  const mid = Math.ceil(arr.length / 2);
  const left = arr.slice(0, mid);
  const right = arr.slice(mid, arr.length);

  return merge(mergeSort(left), mergeSort(right));
}

// Example Usage
const unsortedArray = [38, 27, 43, 3, 9, 82, 10];
const sortedArray = mergeSort(unsortedArray);
console.log(sortedArray); // [3, 9, 10, 27, 38, 43, 82]
