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
**17. Преобразовать числа в символы** <br>
```javascript
const ArrowFunc = function(arr) {
  return arr.map(el =>String.fromCharCode(el)).join(''); 
}
```
**18. Убрать все повторяющиеся значения  вмассиве и sort по частоте повторений** <br>
```javascript
const fn = (array) => {
const result = [];
  const unique = array.reduce((acc, cur) => {
    acc[cur] = (acc[cur] || 0) + 1;
    return acc;
  ,{})
  const keys = Object.keys(unique)
  return unique.sort((a, b) => {
    return unique[b] - tem[a]
  })
}
```
**19. Каждый элемент массива умножить на 2** <br>
```javascript
function multiplyByTwo (...restArgs) {
   return restArgs.map(el => el*2)
}
```
**20. КАРРИРОВАНИЕ для суммы** <br>
```javascript
function sum(a) {
  return function(b) {
    return a+b
  }
}
```
**21.SPREAD Остаточные параметры SPREAD** <br>
```javscript
function sumAll(...args) {
  let sum = 0;

  for (let arg of args) sum += arg;

  return sum;
}
sumAll(1, 2) // 3
```
**22.REST Остаточные параметры REST** <br>
```javscript
const pizza = ['Pepperoni', 2222, 5, 6, 10, 30, 1];
const [name, id, ...rest] = pizza;
```
**23. РЕКУРСИЯ ** <br>
```javscript
function fur(n) {
if (n<=1) {
	return n;	//сумма вхождений
	} else {
	return fn(n-1) + fn(n-2)	
	}
}
```
**24. ДЕСТРУКТУРИЗАЦИЯ REST** <br>
```javscript
const [firstName, ...otherInfo] = ["Anna", "Smith", "github"];

console.log(firstName); // "Anna"
console.log(otherInfo); // ["Smith", "github"]
```
**25. Таймер setInterval  ** <br>
```javscript
let timerId = setInterval(() => alert('tick'), 2000);
```
**26. Напишите функцию printNumbers(from, to), которая выводит число каждую секунду, начиная от from и заканчивая to. ** <br>
```javscript
function printNumbers(from, to) {
  let current = from;

  setTimeout(function go() {
    alert(current);
    if (current < to) {
      setTimeout(go, 1000);
    }
    current++;
  }, 1000);
}

function printNumbers(from, to) {
  let current = from;

  let timerId = setInterval(function() {
    alert(current);
    if (current == to) {
      clearInterval(timerId);
    }
    current++;
  }, 1000);
}

// printNumbers(5, 10);
```
## Что в будет в консоли
**1. Что выведется** <br>
```javascript
var a = 5; //a = 5;
funnction fn() { // a = undefined
  if(a) {
  concole.log(a);
  var a = 10;
  }
}
f(); // undefined
```
**1. Функция, которая выведет каждый раз значение++ (замыкание)** <br>
```javascript 
let inc = (function () {
  let counter = 0;
  return function () => {
    counter + 1;
  }
 })()
 inc() // 1
 inc() // 2
 
// ИЛИ
 function counter() {
	let i = 1;
	return function() {return i++};
}
```
