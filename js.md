### javascript this

1. this 그냥 쓰거나 일반 함수 안에서 쓰면 {widow} obj로 나옴

2. strict mode(최상단에 쓰면 js strict mode로 쓸 수 있음 엄격한 모드) + 일반함수 내에서 쓰면 undefined
### strict mode
- IE 10버전 이상에선 'use strict'라는 키워드를 페이지 최상단에 추가하면 

- strict mode로 자바스크립트를 작성가능합니다. 

- strict mode에선 var 키워드 없이 변수를 선언하거나, 

- 변수를 arguments라는 이상한 키워드로 선언하거나 그런 실수를 방지해줍니다. 

- strict mode에선 this 키워드를 일반함수 안에서 불렀을 때 undefined라는 값으로 강제로 지정해줍니다. 

3. 오브젝트 내 함수안에서 쓰면 그 함수를 가지고 있는 오브젝트를 뜻함

함수 기존 문법: function(){}
es6문법: () => {} arrow function

- Arrow Function 특징: this 값을 함수밖에 있던거 그대로 씀

오브젝트안에 있는 함수를 메소드라 함(method)