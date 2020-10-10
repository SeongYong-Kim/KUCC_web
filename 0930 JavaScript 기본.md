# JavaScript 기본

웹과 사용자가 상호작용할 수 있게 만들어주는 언어



### Web에서의 사용

```shell
<script></script> : JavaScript 작성 테그

document.write : Web에 출력

document.querySelector('tag, class, id').style.backgroundColor = "black" : tag, class, id에서 style을 background-color를 black으로 지정

document.querySelectorAll : 모든 결과를 불러옴

event : <input type = "" value ="" onclick ="alert('hi')"> - 클릭 시 실행
		<input type = "" value ="" onchange ="alert('changed')"> - 내용이 바뀌는 경우 실행
		<input type = "" value ="" onkeydown ="alert('key down')"> - 포인트를 가져다 대면 실행
		
this : 자신이 속해있는 tag를 가리킴
```

​     

### Data type

숫자형 : 사칙연산 가능

문자열 : "" 또는 ''로 표현

Boolean : ===, <, > 등 비교연산자를 통해 비교



### 변수와 대입연산자

var {변수} : 변수 선언, 변수 사용으로 반복을 줄일 수 있음

{변수} = {대입 값} : 변수에 대입 값 대입



### 조건문

```shell
if(){

}else{

}
```



### 반복문

```shell
while(){

}

for(var key in 객체){

}, key값을 다 불러옴
```



### 함수

```shell
function {function name}(self){

return 
}
: script tag안에 정의함

parameter : 매개변수
argument : 입력값
```



### 객체

```shell
var coworkers(객체) = {
	"programmer" : "tjddyd1592"
	"designer" : "leezche"
}

ex. document.write("programmer : "+ coworkers.programmer); #결과 : programmer : tjddyd1592
	coworkers.bookkepper = "duru"; #정보 추가
	coworkers["data scientist"] = "taeho"; #띄어쓰기가 있는 정보추가

. : 객체에 접근하는 operater
```

 ```shell
#객체 반복문
for(var key in coworkers){
	document.write(key + '<br>');
}
 ```

```shell
<script>
var Links = {
	setColor:function(color){
	var alist = document.querySelectorAll('a');
		for( i = 0 ; i < alist.length ; ++i){
		alist[i].style.color = color;
		}
	}
}

var Body = {
    setColor:function (color){
    	document.querySelector('body').style.color = color;
   		},
    setBackgroundColor:function (color){
    	document.querySelector('body').style.backgroundColor = color;
    	}
}
```



### Property & Method

Property와 Property사이에 , 넣어줘야함

```shell
coworkers.showAll = function(){		#함수 정의, function showAll(){}이랑 같은 개념
    for(var key in coworkers){		#coworkers 대신에 this 사용가능
        document.write(key + '<br>');
    }
}
```



### 파일로 만들기

```
<script src = "파일명 또는 주소"></script>
```



### jQuery

```shell
<script src = "jQuery 주소"></script>

setColor:function(color){
	$('a').css('color', color);
} #a테그 css color를 입력받는 color로
```

