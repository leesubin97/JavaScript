7. 함수(Function)

1) 함수

- 코드의 집합을 나타내는 자료형

- 선언방법: function 함수명() {코드};

- 사용: 함수명();

*코드위치에 상관없이 먼저 선언됨



2) 익명함수

- 이름이 없는 함수

- 변수에 저장하거나 따로 함수 선언없이 임시사용할 때 사용

- 활용: var 변수 = function() {코드};

-> 변수가 선언되기 전에는 사용할 수 없음



3) 매개변수

- 함수에 전달하는 값

- 같은 이름의 함수라도 매개변수에 따라 실행되는 코드가 다를 수 있음(오버로딩)

- 함수 선언시 지정되지 않은 매개변수는 무시됨

- 형태 function(매개변수) {코드}; -> 매개변수를 코드 내에서 사용 가능



4) 리턴값

- 함수가 반환하는 값

- 형태: return 반환값;

- return 키워드 실행 시 함수 종료

*return; <- 반환값 없이 return만 실행되더라도 함수가 종료됨

- 활용 예시

function sumNum(a, b) {return a+b;};

var num = sumNum(1, 2);

-> num변수에 3이 저장됨



5) 가변인자 함수

- 매개변수의 개수가 변할 수 있는 함수

- 매개변수를 지정하지 않아도 사용 가능

- arguments 객체를 통해 활용(모든 함수는 기본적으로 arguments 객체를 내장하고 있음)

- 활용 예시

function sumAll() {

  var output = 0;

 for(var i=0;i<arguments.length; i++)

	output+=arguments[i];

 return output;

}

-> sumAll(10,20,30) 실행시 60 반환



- 전개연산자: 마침표 3개(...)를 통해 가변인자를 표기, 함수나 배열에서 사용 가능

function sumAll(...numbers) // 매개변수에 전개연산자를 이용해 선언시

output+=numbers[i]; // arguments 대신 numbers 사용 가능



(a, b, ...numbers) // 일반 매개변수와 함께 사용 가능



var array = [1, 2, 3, 4];

sumAll(...array); // 배열을 매개변수로 함수 호출 가능

var array2 = [...array]; 의 형태로 배열 복사 가능

var array3 = [...array, ...array2]; 의 형태로 배열 병합 가능

*같은 방식으로 객체 복제도 가능



6) 내부 함수

- 함수 내부에 다른 함수 선언 가능

- 프로그램 내 함수간의 충돌을 막을 수 있음

- JQuery에서는 함수 대부분을 내부 함수로 작성



7) 자기호출 함수

- 함수의 생성과 동시에 호출하는 함수

- 형태

(function () {코드})();



8) 콜백 함수

- 매개변수로 전달되는 함수

*자바스크립트에서는 함수도 하나의 자료형이기 때문에 매개변수로 전달 가능

- 활용 예시

// 함수 선언 영역

function printTen(callback){

for (var i = 1 ; i <= 10 ; i++) 

 callback(i);

};

var consoleOut= function(values) {console.log(values);};

// 함수 사용 역

printTen(consoleOut);

-> 1부터 10까지 콘솔창에 출력



9) 함수를 리턴하는 함수

- 리턴값을 함수로 지정 가능

- 활용 예시

function funEx() {

return function () { alert('익명함수리턴');};

};

funEx();

-> 익명함수리턴 알림창이 발생



10) 클로저(closure)

- 단어상의 의미는 폐쇄, 클로저의 의미는 다양함

- 함수 실행시 함수를 생성할 때와 동일한 스코프 체인 사용(닫힌 외부함수의 변수 사용 가능)

- 함수로 생성된 공간과 리턴되는 함수 자체, 남은 지역변수까지 모두 클로저로 불리기도 함

- 클로저는 최종 갱신된 변수(변화하는 값의 마지막 값)에 대해서만 접근 가능

-> 원치 않는 값을 얻기도 함 -> 부작용 해소를 위해 IIFE(즉시 호출된 함수 표현식)사용

- IIFE: 클로저 함수의 마지막에 ()를 추가해서 생성과 동시에 호출해서 각각의 공간을 생성

- 예시

function a(){  // a함수 선언

var i=3; // a함수의 변수 i

function b(){return i;};  // b함수 선언(리턴값 a함수의 변수 i)

return b // b함수를 리턴 

};

var var1 = a(); // var1에는 a의 내부 함수 b가 담겨있음, 즉 var1은 b함수임

var var2 = i(); // var2에는 b함수의 리턴값인 a함수의 지역변수 i가 담김

-> 현재 a함수는 닫힌 상태이기 때문에 i라는 변수를 사용할 수 없음

-> 하지만 var2에는 3이라는 값이 담겨있음

- 자세한 내용은 해당 포스팅 참조

http://chanlee.github.io/2013/12/10/understand-javascript-closure/



11) 기본 매개변수

- 매개변수에 기본값 설정 가능(매개변수가 undefined 자료형이면 값을 초기화)

- 형태: if(!매개변수명) { 매개변수=기본값; } // 조건문으로 undefined를 체크 후 기본값 설정

- 예시

function f(a, b, c) {

if(!a) {a=1;} 

if(!b) {b=2;}

if(!c) {c=3;}

console.log(a+":"+b+":"+c);

};

f(10, 20); // 실행시 콘솔창에 10:20:3 출력



- if문 대신 짧은 조건문 사용 가능: a = a || 1; 은 if(!a) {a=1;} 와 같다.

- ECMAScript 6부터는 함수 선언시 매개변수에 설정 가능

function f(a, b=2, c=3){} <- 기본 매개변수 설정

