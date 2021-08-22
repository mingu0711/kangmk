# Chapter 02 화살표 함수

```js
//화살표 함수 예시
const greeting = function(name){ return "hello"+name };
const greeting = (name) => { return "hello ${name}" };
const greeting = name => { return `hello ${name}` };    //매개변수가 한 개면 괄호 생략 가능
const greeting = () => { return "hello" };  //매개변수가 없으면 빈 괄호

const greeting = name => 'hello ${name}';   //암시적 반환

//화살표 함수에서의 this는 상위 스코프에서 상속
button.addEventListener("click",()=>{
    //!!! 여기서 this는 window객체를 가리킴
    this.classList.toggle("on");
});

//화살표 함수의 argument는 배열 객체로서 접근할 수 있다.
const showWinner = (...args) => {
    const winner = args[0];
    console.log(winner);
};
showWinner('mk','dj','bj'); //mk
```
