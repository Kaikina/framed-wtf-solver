# Framed Wtf
[Framed Wtf](https://framed.wtf/) is a daily movie guessing game.

## How to use ? 
Copy the following code and paste it to your browser console while being on the framed wtf page.
The answer of the daily movie will be output to the console.
```js
const date = new Date("2022-03-12");
date.setDate(date.getDate() - 1);
const now = new Date();
const day = Math.floor((now - date) / 86400000);
fetch('https://framed.wtf/_next/static/chunks/834-c92d63ae6352084e.js').then(response => response.text()).then(content => console.log(content.match(/(?<=title:")([a-zA-Z0-9 :,?\\\-\!&'\./]*)(?=")/g)[day - 1]));
```

Example of usage : 
![image](https://i.imgur.com/3gihjfh.png)
