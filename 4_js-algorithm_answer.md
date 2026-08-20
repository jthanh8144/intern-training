# JS algorithm

## Answer

```js
const exercise1 = (arr) => {
  return [
    arr.sort((a, b) => a - b)[0],
    arr.sort((a, b) => a - b)[arr.length - 1],
  ];
};

const exercise2 = (arr1, arr2) => {
  return arr1.reduce((a, b) => a + b, 0) + arr2.reduce((a, b) => a + b, 0);
};

const exercise3 = (n) => {
  return n === 0 ? 1 : n * exercise3(n - 1);
};

const exercise4 = (str) => {
  return str.split("").reverse().join("");
};

const exercise5 = (num) => {
  return Number(
    num
      .toString()
      .split("")
      .sort((a, b) => b - a)
      .join(""),
  );
};

const exercise6 = (names) => {
  switch (names.length) {
    case 0:
      return "no one likes this";
    case 1:
      return `${names[0]} likes this`;
    case 2:
      return `${names[0]} and ${names[1]} like this`;
    case 3:
      return `${names[0]}, ${names[1]} and ${names[2]} like this`;
    default:
      return `${names[0]}, ${names[1]} and ${names.length - 2} others like this`;
  }
};

const exercise7 = (n) =>
  Array.from({ length: n }, (_, i) => Array.from({ length: i + 1 }).fill(1));

const exercise8 = (n) => n.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
const exercise8_2 = (n) => {
  return n
    .toString()
    .split("")
    .reverse()
    .join("")
    .match(/.{1,3}/g)
    .join(",")
    .split("")
    .reverse()
    .join("");
}

function getNumber(word: string): number {
  for (const char of word) {
    const num = Number(char);

    if (num >= 1 && num <= 9) {
      return num;
    }
  }

  return 0;
}

function exercise9(words: string): string {
  if (!words) return '';

  return words
    .split(' ')
    .sort((a, b) => {
      const numA = getNumber(a);
      const numB = getNumber(b);

      return numA - numB;
    })
    .join(' ');
}


function exercise10(integers: number[]): number {
  const firstThree = integers.slice(0, 3);

  const oddCount = firstThree.filter(num => num % 2 !== 0).length;

  const lookingForOdd = oddCount === 1;

  for (const num of integers) {
    if ((num % 2 !== 0) === lookingForOdd) {
      return num;
    }
  }

  return 0;
}

function exercise11(str: string): string {
  let i = str.length - 1;

  while (i >= 0 && str[i] >= '0' && str[i] <= '9') {
    i--;
  }

  if (i === str.length - 1) {
    return str + '1';
  }

  const prefix = str.slice(0, i + 1);
  const numberPart = str.slice(i + 1);

  const number = Number(numberPart) + 1;

  const result = String(number).padStart(numberPart.length, '0');

  return prefix + result;
}

function exercise12(n: number): number {
  while (n >= 10) {
    let sum = 0;

    while (n > 0) {
      sum += n % 10;
      n = Math.floor(n / 10);
    }

    n = sum;
  }

  return n;
}

function exercise13(parens: string): boolean {
  let count = 0;

  for (const char of parens) {
    if (char === '(') {
      count++;
    } else if (char === ')') {
      count--;
    }

    if (count < 0) {
      return false;
    }
  }

  return count === 0;
}
```
