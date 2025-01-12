# 개념(concept)

콘셉트(concept)는 제네릭 프로그래밍에서 필수불가결한 것으로 ISO Technical Specification ISO/IEC 19217:2015로 제출된 C++ 템플릿(template)의 확장 기능이다.
콘셉트는 이름이 붙은 boolean 술어이며 컴파일 시간에 평가된다. 콘셉트는 프로그래머에게 주어진 템플릿 인자에 어떤 요구조건이 있는지 알려주는 역할을 한다. 
콘셉트는 템플릿(클래스 템플릿, 함수 템플릿, 클래스의 멤버함수 템플릿)과 함께 사용되어 사용자에게 제한을 두는 것으로 템플릿 파러미터로 전달 될 수 있는 인자에 대해 조건을 부여한다. 

예를 들어 함수를 호출할 때 숫자 유형만 사용하여야 하는 것으로 제한을 두고자 한다면 다음과 같이 코드를 쓸 수 있다. 

```c++
template <Number N>
````
즉 이 코드는 ``ìnt```, ```double```, ``ùint64_t```같은 자료형에 대해서는 사용할 수 있으나 문자열 같은 자료형에 대해서는 사용할 수 없다는 뜻이다. 
여기서 "수(Number)" 같은 제한조건이 콘셉트이다.

다음 코드는 콘셉트를 사용 가능한 C++ 표준 라이브러리를 이용하여 "Equality Comparable"라는 이름의 콘셉트를 정의한다. 
```a==b```와 ```a!=b```가 컴파일이 되고 "Boolean" 콘셉트를 만족하는 자료형의 반환값을 출력한다면 모든 자료형 T는 이 콘셉트를 만족시킨다. 

```c++
template <class T>
concept bool EqualityComparable() {
    return requires(T a, T b) {
        {a == b} -> Boolean; // Boolean은 불린 컨텍스트에서 사용될 수 있는 타입을 정의하는 콘셉트임
        {a != b} -> Boolean;
    };
}
```
이 콘셉트로 인해 제약에 걸린 함수 템플릿을 다음과 같이 선언될 수 있다.

```c++
void f(const EqualityComparable&); // 제약이 걸린 함수 템플릿 선언
```

콘셉트의 주요 용도는 다음과 같다.

* 템플릿 프로그래밍에 타입 검사를 적용


