
- Kotlin
	- Jetbrain회사에서 만든 언어
	- 제트브레인은 인텔리J를 만듬
	- 인텔리J를 기반으로 만든 프로그램이 안드러이드 스튜디오
		- 안드로이드 스튜디오는 2013년에 나옴
	- 2016 년에 나옴
	- 자바를 보완하기 위해 만든 언어
	- 자바가 동작하는 환경에선 완전한 호환이 됨
	- 2017년도에 코틀린이 공식 언어로 채택됨
	- 결론적으로 편하고 쉽다. 나온지 얼마 안된 언어라서 강하다.

- 기초 문법
	- 세미콜론을 사용하지 않음

- 함수 선언
```
fun sum(a: Int, b: Int): Int{
	return a+b
}
```
- 또는 표현식으로 함수 선언 가능
```
fun sum(a: Int, b: Int) = a+b
fun max(a: Int, b: Int) = if(a>b) a else b
```

- 변수 선언
```
val a: Int = 1
val a = 2 // 타입 추론
```

- 타입
	- 정수형 : Byte, Short, Int, Long
	- 실수형 : Float, Double
	- 그 외: Char, String, Boolean

- 반복문
	- for 반복문
```
for(i in 1..5){} // 1 2 3 4 5 반복
마지막 숫자 포함하기 싫으면 until 로 교체
for(i in 6 downTo 0 step 2) // 6 4 2 0 반복

val numberList = listOf(1,2,3,4)
for(number in numberList)로 객체 반복 가능
```

	- while 반복문
```
while(x>0){}
do while문도 가능
```

- 조건문
```
if(a>b) 어쩌구
코틀린의 if는 표현식으로도 표현 가능
val max = if(a>b){ a } else { b }

when(x) {
	1 -> {}
	2 -> {}
	3 -> {}
	4,5 -> {}
	in 10..20 -> {}
	!in 30..40 -> {}
	is Int -> {}
	else -> {}
	별거 다 가능
}
```

- 자바 VS 코틀린
	- 코틀린은 Null Safe 기능이 있어서 NPE를 방지할 수 있다
	- NPE를 예방하기 위해 널이 되는 타입과 될 수 없는 타입을 나눠놓음
	
- Scope 함수 (범위 함수)
	- apply, with, let, also, run
	- 일시적으로 범위가 생성되며 객체에 자유롭게 접근이 가능해짐
	- apply
		- this로 접근가능 및 this 생략 가능
		- 반환값이 객체 자신이라 보통 초기화에 많이 씀
```
val person = Person().apply{
	firstName = "123"
	lastName = "asd"
}
```

	- also 함수
		- 객체가 파라미터로 전달 됨
		- 파라미터 명 지정 가능 및 지정 안하면 it임

	- let 함수
		- 주로 널이 아닌 객체에서 람다를 실행하기 위해 씀
		- 객체?.let {}
		- 코드 블럭의 수행 결과가 반환됨

	- with 함수
		- 반환값 : 결과값
		- 객체 안에 있는 것들을 this나 생략을 통해 호출 가능
		- 확장 함수로 사용 못함

	- run 함수
		- 객체 초기화와 연산이 필요한 경우에 유용함
		- 반환값 : 결과값

	
- Data Class
	- 데이터 저장을 목적으로 만들어진 클래스
	- 4개의 함수가 자동으로 생성됨

- 람다 표현
	- 코틀린은 간편한 람다 함수를 제공함
	- 버튼 클릭 로직도 자바와 비교했을 때 아주 간소화 됨

- 지연 초기화
	- 나중에 초기화 하고 싶을 때 사용하는 구문
	- 널이 아닌 값이 초기값이 없을 때 나중에 초기화 가능
	- lateinit : var 형식에 사용
	- lazy init : val 형식에 사용
	- 맞나..? 아닌거 같은데


