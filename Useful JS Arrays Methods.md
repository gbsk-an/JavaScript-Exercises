**Массив, который будет использоваться в примерах**<br>
```javascript
  arr = ['salad', 'ketchup', 'french fries', 'nuggets']
```
1. Get Elements from an Array
```javascript
const element = arr[0]; // salad
```
2. Length of an array
```javascript
const len = arr.length; // 4
```
3. Loop through the array
```javascript
for (let i=0; i < arr.length; i++) {
  console.log(`Element at index ${i} is ${arr[i]}`); // Element at index 0 is salad 
}
//Element at index 0 is salad 
//Element at index 1 is ketchup 
//Element at index 2 is french fries 
//Element at index 3 is nuggets
```
4. Add an element at the end of the array
```javascript
arr.push('hummus');
console.log(arr) // arr = ['salad', 'ketchup', 'french fries', 'nuggets', 'hummus']
```
5. Remove an element from the end of the array
```javascript
arr.pop(); // hummus (it also returns the removed element)
console.log(arr) // arr = ['salad', 'ketchup', 'french fries', 'nuggets']
```
6. Remove an element from the beginning of an array
```javascript
arr.shift(); // salad (it also returns the removed element)
console.log(arr) // arr = ['ketchup', 'french fries', 'nuggets']
```
7. Add element to the beginning of an array
```javascript
arr.unshift('salad');
console.log(arr) // arr = ['salad', 'ketchup', 'french fries', 'nuggets']
```
8. Copy and Clone an Array with slice()
```javascript
const arrCopy = arr.slice();
console.log(arrCopy); // ['salad', 'ketchup', 'french fries', 'nuggets']
arr === arrCopy; // false
```
9. Determine if a Value is an Array
```javascript
Array.isArray(arr) // true
Array.isArray([]) // true
Array.isArray({ key: value }) // false
```
10. Array Destructuring
```javascript
let [food, sauce, potato, meat] = ['salad', 'ketchup', 'french fries', 'nuggets'];
console.log(food, sauce, potato, meat) // salad ketchup french fries 'nuggets
```
11. Rest Parameter
