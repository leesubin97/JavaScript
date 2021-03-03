# JavaScript

1. 자바스크립트 기본

1) 표현식과 문장

- 표현식: 자바스크립트에서 값을 만들어내는 간단한 코드

ex) 1, 1+1, 10*5, 'Hi' 등등

- 문장: 표현식의 모음, 문장 끝에는 세미콜론으로 종결을 표현

ex) x=y+1; / var hi = 'h'+'i'; / alert('Hi'); 등등



2) 키워드

- 키워드: 특별한 의미가 있는 단어

- 예시

break, else, instanceof, true, case, false, new, try, catch, finally, null, typeof, continue, for, return, var, default, function, switch, void, delete, if, this, while, do, in, throw, with



3) 식별자

- 식별자: 변수와 함수의 이름을 지을 때 사용하는 단어

- 명명규칙: 키워드 사용 불가, 숫자로 시작 불가, 특수문자 '_', '$' 외 사용불가, 공백 사용 불가

- 변수: 객체의 속성

- 함수(메소드): 특별한 목적의 작업을 수행하기 위해 설계된 블록

*단어 뒤에 소괄호()가 있는 경우는 함수, 없으면 변수 혹은 키워드

- 관례: 생성자의 이름 첫 글자는 대문자, 그 외에 변수나 함수의 이름은 소문자로 시작하고 여러 단어를 조합해서 사용할 경우 첫 글자를 대문자로 작성

ex) var maxNumber / getNumber()



4) 주석

- 주석: 프로그램 코드 설명에 사용

- 프로그램 실행에 전혀 영향을 주지 않음

- HTML태그 주석과 자바스크립트 주석으로 구분되며 각각 다르게 적용시켜주어야 함

- HTML태그 주석: <!-- 주석 내용-->

- 자바스크립트 주석: // 주석내용 혹은 /* 주석내용 */



5) 출력

- alert() 함수: 브라우저에 경고창 생성

ex) alert('내용');

- console.log() 함수: 콘솔창에 내용 출력

ex) console.log('내용');



6) 입력

- prompt() 함수: 사용자 입력창 생성

ex) var input = prompt('메세지', '기본값');

- confirm() 함수: 확인창 생성(Yes or No)

ex) var input = confirm('메세지');

