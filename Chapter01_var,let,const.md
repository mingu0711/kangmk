# Chapter 01 let, var, const

> var
```
var 키워드로 선언된 변수는 함수 스코프에 종속된다.
```

```js
for(var i=0;i<5;i++){
    var myString='hello world';
}
console.log(myString);  //hello world

function myFunc(){
    var funcString = 'function string';
}

myFunc();
console.log(funcString);    // ReferenceError
//함수 스코프 내에 제한되어 있어 외부에서 접근 불가
```

> let
```
let, const로 선언된 변수는 블록 스코프로 종속된다.
```

```js
//let vs var
let x='global';
if(x=='global'){
    let x='block-scoped';
    console.log(x); //block-scoped
}
console.log(x); //global

var y='global';
if(y=='global'){
    var y='block-scoped';
    console.log(y); //block-scoped
}
console.log(y); //block-scoped
```

> const
```
블록 스코프로 종속된다.
재할당을 통해 값이 변경될 수 없으며, 다시 선언될 수 없다.
```

```js
//const로 선언된 객체의 속성은 재할당이 가능하다.
const person = {
    name:'myName',
    age:13
}
person.age=26;
console.log(person.age);    //26
```

> TDZ(일시적 비활성 구역)
```
var는 정의되기 전에 접근할 수 있지만, 그 값에는 접근할 수 없다.
- 정의되기 전까지 undefined 값을 가지게 됨

let과 const는 정의하기 전에 접근할 수 없다.
- 변수가 선언되기 전까지 TDZ에 존재
```

```js
//호이스팅(hoisting)
console.log(i);     //undefined
var i = 'this is variable';

console.log(j);     //ReferenceError
let j = 'this is let';
```
