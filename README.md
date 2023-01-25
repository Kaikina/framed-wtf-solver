# Framed Wtf
[Framed Wtf](https://framed.wtf/) is a daily movie guessing game.

## How to use ? 
Copy the code inside solver.js and paste it to your browser console while being on the framed wtf page.
The answer of the daily movie will be output to the console.
```js
const scripts = document.head.getElementsByTagName('script');
fetch(scripts.item(scripts.length - 1).src)
    .then(response => response.text()).then(content => console.log(content.match(/(?<=answer:")([a-zA-Z0-9 :'\.\-,&\!\\]*)(?=")/g)[Math.ceil(Math.abs(new Date - new Date("5/15/2022")) / 864e5) - 1]));
```

Example of usage : 
![image](https://i.imgur.com/3gihjfh.png)
