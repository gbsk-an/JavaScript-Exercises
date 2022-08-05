**1. Вычислить сумму всех элементов массива, которые делятся без остатка на 3** <br>
```javascript
sum = (arr) => {
  if (arr.length === 0) {
    return 0;
  }
  let result = 0;
  for (let i = 0; i < arr.length; i += 1) {
    if (arr[i] % 3 == 0) {
      result += arr[i];
    }
  }
  return result;
};
```
**2. Добавить префикс к каждому элементу массива** <br>
```javascript
const addPrefix = (names, prefix) => {
  for (let i = 0; i < names.length; i += 1) {
    const newNames = names[i];
    const prefixNames = `${prefix} ${newNames}`;
    names[i] = prefixNames;
  }
  console.log(names);
};
```
**3. Высчитать среднее арифметическое элементов переданного массива с помощью цикла for...of** <br>
```javascript
const arithmeticMean = (arr) => {
  if (arr.length === 0) {
    return null;
  }
  let result = 0;
  for (const value of arr) {
    result += value;
  }

  return (result / arr.length);
};
```
**4. Удалить null значения и массива** <br>
```javascript
const deleteNull = (arr) => {
  const result = [];
  for (const value of arr) {
    if (value !== null) {
      result.push(value);
    }
  }

  return result;
};
```
**5. Написать функцию, которая принимает массив из 10 чисел и возвращает строку этих чисел в форме телефонного номера (2 варианта).** <br>
```javascript
function createPhoneNumber(numbers) {
  var format = "(xxx) xxx-xxxx";  
  for(var i = 0; i < numbers.length; i++) {
    format = format.replace('x', numbers[i]);
  }
  
  return format;
}

function createPhoneNumber(numbers) {
  let region = numbers.slice(0, 3).join('');
  let middleNumbers = numbers.slice(3, 6).join('');
  let lastNumbers = numbers.slice(6, 10).join('');
  return `(${region}) ${middleNumbers}-${lastNumbers}`
}
```
**6. Написать функцию, которая принимать на вход строку и возвращает reverse версию ('kebab' => 'babek')** <br>
```javascript
function solution(str) {
  return str.split('').reverse().join('')
}
```
**7. Написать функцию, которая принимать на вход число и заменяют любую цифру < 5 на 0, а цифру > 5 на 1 ('kebab' => 'babek')** <br>
```javascript
function replace(x){
  return x.split('').map((num) => num > 4 ? 1 : 0).join('');
}
```
**8. Найти наименьшее число в массиве ** <br>
```javascript
function min(arr){
  return Math.min(...arr)
}
```
**9. Первый символ к верхнему регистру ** <br>
```javascript
function capitalize(str){
  return str[0].toUpperCase() + str.slice(1)
}
```
**10. Создать функцию, которая возвращает среднее арифметическое всех переданных аргументов ** <br>
```javascript
function sum(...arr) {
  if (arr.lenght === 0) {
    return null
  }
  let result = 0;
  for (const item of arr) {
    result += item;
  }
  return result / arr.lenght
}
```
