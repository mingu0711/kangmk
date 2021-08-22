# Chapter 04 템플릿 리터럴

> 문자열 삽입
```js
//백틱(`)
var name='kangmk';
var greeting1='hello my name is '+name;
var greeting2=`hello my name is ${name}`;
```

> 표현식 삽입
```js
var a=1;
var b=2;

console.log('1 * 10 is ' + (a * b));
console.log(`1 * 10 is ${a * b}`);
```

> 여러 줄 문자열 생성
```js
var text = 'hello, \
my name is kangmk \
how are you?';

var text2 = `hello,
my name is kangmk
how are you?`;
```

> 중첩 템플릿
```js
const people=[
    {name:'a',age:27},
    {name:'b',age:13},
    {name:'c',age:25}
]
const markup=`
<ul>
    ${people.map(person=>'<li> $person.name}</li>')}
</ul>
`;
```

> 삼항 연산자
```js
const isDiscounted=false;
console.log(isDiscounted?"$10":"$20");
```

> 템플릿 리터럴에 함수 전달하기

```js
function groceries(others){
    return `
        <p>
            ${others.map(other=>`<span>${other}</span>`).join('\n')}
        </p>
    `;
}
```