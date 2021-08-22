# Chapter 00 자바스크립트 기초

> 자료형

```
1. 자바스크립트는 동적 언어로서, 정적 언어와 달리 변수를 정의할 때 자료형을 정의할 필요없음
- 타입스크립트 : 자바스크립트의 자료형을 준수하여 강타입언어로 바꾸는 것  
```

```
2. 원시 자료형 VS 객체
- 원시 자료형은 객체가 아닌 자료형으로 메서드를 가지지 않음
- 객체는 여러 속성의 모음을 저장하는데 사용, 원시 자료형을 제외한 모든 자료형
```

```js
//원시자료형
string tString = 'string';
number tNumber = 1;
boolean tBoolean = true;
null;
undefined;
symbol;
```

> 객체

```js
//빈 객체 생성하기 - 객체리터럴
const car = new Object();
const car = {};

//1. 점 표기법, 대괄호 표기법
const car = {
    wheels:4,
    color:"red",
    "goes fast":true
};
console.log(car.color); //red
console.log(car['goes fast']); //true

//2. 객체의 복사
var car = {color:'red'};
var secondCar = car;    //secondCar는 car에 대한 참조로 주소를 저장
console.log(car === secondCar); //두 객체가 동일
car.color='blue';
console.log(secondCar.color);   //blue : 주소를 저장한 것이기 때문

var thridCar = Object.assign({},car);  //객체를 복사 
car.color='black';
console.log(thirdCar.color);    //red : 객체가 복사된 것이기 때문
```

> 함수

```
- 원시 자료형이 함수에 전달될 때는 참조가 아닌 값의 형태로 전달
- 원시 자료형이 아닌 객체나 배열이 함수에 전달될 때는 참조로 전달
```

```js
function greet(name){ console.log(name) };              //함수 정의
var greet = function greet(name){ console.log(name) };  //함수 표현식
var greet = function(name){ console.log(name) };        //익명 함수
var greet = (name) => { console.log(name) };            //화살표 함수

//4-1.함수스코프
//let,const는 블록스코프를 가진다
var myInt = 0;
if(varInt == 0){
    var varInt = 1;
    let letInt = 2;
    const constInt = 3;
    console.log(varInt);    //1
    console.log(letInt);    //2
    console.log(constInt);  //3
}
console.log(varInt);    //1
console.log(letInt);    //not defined  
console.log(constInt);  //not defined
```
