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
