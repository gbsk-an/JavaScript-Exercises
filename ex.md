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
**8. Найти наименьшее число в массиве** <br>
```javascript
function min(arr){
  return Math.min(...arr)
}
```
**9. Первый символ к верхнему регистру** <br>
```javascript
function capitalize(str){
  return str[0].toUpperCase() + str.slice(1)
}
```
**10. Создать функцию, которая возвращает среднее арифметическое всех переданных аргументов** <br>
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
**11. Реализуйте функцию, которая генерирует HTML список определений (теги \<dl>, \<dt> и \<dd>) и возвращает получившуюся строку.** <br>
```javascript
function buildDefinitionList(arr) {
  if (arr.length === 0) return '';
  const parts = [];

  for (const item of arr) {
    parts.push(`<dt>${item[0]}</dt><dd>${item[1]}</dd>`);
  }

  const innerValue = parts.join('');
  const result = `<dl>${innerValue}</dl>`;
  return result;
}
```
**12. Сравнение двух массивов и вывод уникальных значений** <br>
```javascript
function count(arr, arr2) {
const result = [];
for (const item of arr) {
  for (const item2 of arr2) {
    if (item === item2) {
      result.push(item);
    }
  }
}

  const res = _.uniq(result);
  return res.length;
}
```
**13. Привести строку к верхнему регистру через map** <br>
```javascript
function makeUpperCase(str) {
return str.split('').map(el => el.toUpperCase()).join('')
}
```
**14. Вычислить сумму положительных чисел массива** <br>
```javascript
function positiveSum(arr) {
   return arr.reduce((a,b)=> a + (b > 0 ? b : 0),0);
}
```
```javascript
function positiveSum(arr) {
  let result = 0;
  for (const item of arr) {
    if (item > 0) {
      result += item;
    }
  }
  return result
}
```
**15. Заменить строку на символ ('text', '%' => '%%%%')** <br>
```javascript
function contamination(text, char){
  if (text.length === 0 || char.length === 0) return "";
  const arr = text.split('');
  const newchar = char.split('');
  const newArr = arr.map(el => newchar);
  return newArr.join('')
}
```
**16. Создать функцию, которая возвращает массив целых чисел от n до 1, где n > 0** <br>
```javascript
const reverseSeq = n => {
  const arr = [];
  for (let i = n; i > 0; i--) {
    arr.push(i);
  }
  
  return arr
};
```
