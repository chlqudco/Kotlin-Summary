- 컬렉션
	- element들로 이뤄진 그룹을 저장하기 위해 설계된 객체
	- 코틀린은 풍부한 기능을 제공한다
	- 여러가지 데이터 구조와 종합적인 API가 포함된다
	- 컬렉션을 조작하는 연산은 인라인 함수이다.
	- 컬렉션 타입
		- 배열, iterable, sequence, map 타입이 있다.
	- iterable
		- Iterable<T> 로 표현하며 즉시 계산되는 상태가 있는 컬렉션을 표현한다.?
		- 그냥 내가 알고있는 iterator인가
	- Collection 클래스를 상속한 애들
		- List는 인덱스를 통한 접근이 가능함
		- HashSet은 해시 테이블 기반 컬렉션
		- 이진 검색 트리 기반의 TreeSet도 있음
	- 맵
		- key와 value쌍으로 이뤄진 집합

- 컬렉션 생성하기
	- emptyList()나 listOf()는 모두 불변이다.
	- 가변 컬렉션은 mutable이 붙어야 함
