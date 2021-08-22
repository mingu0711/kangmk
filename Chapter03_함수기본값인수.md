# Chapter 03 함수 기본값 인수

```js
//함수의 인수를 객체로 전달
//매개변수가 주어진 키에 맞춰 입력됨(순서 상관 없음)
function calculatePrice({total=0,tax=0.1,tip=0.05,}={}){
    return total+(total*tax)+(total*tip);
}

const bill = calculatePrice({tip:0.15,total:150});  //187.5
```
