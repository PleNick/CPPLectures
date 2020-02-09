# 연산자

## 산술 연산자

산술 연산자는 이항 연산자로 피 연산자가 2개로 수에 적용되는 연산자이다.  


| 연산자 | 설멍 |
|:---------:|:-----------------------------------:|
| x + y  |  덧셈            |
| x - y  |  빨셈           |
| x * y  |  곱셈          |
| x / y  |  나눗셈 (두 수가 정수 이면 결과도 정수)         
| x % y  |  정수 나머지 연산 (예: 5 % 2 => 1            |


## 축약 연산자 

축약 연산자는 산술 연산의 특별한 경우에 해당하는 연산자이다. 즉 이미 할당받은 저장공간(변수)에 산술 연산을
수행하고 그 저장공간에 다시 저장하는 특별한 경우에 사용된다. 

| 연산자 | 설멍 |
|:---------:|:------------------------------------------------:|
| x += y  |   x = x + y 의 축약 연산자            |
| x -= y  |   x = x - y 의 축약 연산자           |
| x \*= y |   x = x * y 의 축약 연산자           |
| x /= y  |   x = x / y 의 축약 연산자            |
| x %= y  |   x = x % y 의 축약 연산자            |


## 비교 연산자

비교 연산자 관계 연산자라고도 하며 2항 연산자로 피 연산자가 2개 이며 연산의 결과는 부울 값(참 또는 거짓)을 반환한다. 

| 연산자 | 설멍 |
|:---------:|:-----------------------------------:|
| x == y  |  x와 y가 같을 때 참 아니면 거짓            |
| x != y  |  x와 y가 다를 때 참 같은면 거짓            |
| x < y  |   x가 y 보다 작으면 참 아니면 거짓          |
| x > y  |   x가 y 보다 크면 참 아니면 거짓            |
| x <= y  |  x가 y 보다 작거나 같은면 참 아니면 거짓     |
| x >= y  |  x가 y 보다 크거나 같으면 참 이나면 거짓     |


## 논리 연산자 

논리 연산자도 2항 연산자로 두 입력에 대한 논리곱, 논리합, 부정 연산을 치하는 것으로 입력 데이터도 부울 값이고 연산 결과도 부울 값을 반환한다.  

| 연산자 | 설멍 |
|:---------:|:------------------------------------------------:|
| x && y  |  x와 y의 논리 곱, 입력 모두 참일 때만 연산 결과가 참       |
| x \|\| y  |  x와 y의 논리 합, 입력 모두 거짓을 때만 연산 결과가 참      |
| !x      |  x의 논리 값의 반대 값을 반환                           |

논리 연산자의 경우 피 연산자를 앞에서 부터 조사하기 때문에 논리 곱의 경우 앞의 피연산자가 false 이면 두 번째 피연산자를 확인하지 않고 결과를 false로 내고 
논리 합의 경우는 앞의 피연산자가 true 이면 두 번째 

## 비트 연산자 

비트 단위로 연산을 취하는 것으로 비트 비트 논리 연산자와 시프트(shift) 연산자가 있다.  

* 비드 논리 연산자도 이항 연산자로 각 입력 데이터들을 비트별로 논리 연산을 하는 것으로 비트 별 이준수 

| 연산자 | 설멍 |
|:---------:|:------------------------------------------------:|
| x & y  |   x와 y의 비트별 논리 곱            |
| x \| y  |  x와 y의 비트별 논리 합     |
| x ^ y  |  x와 y의 비트별 배타적 논리 합 (두 비트의 값이 다를 때만 참     |
| ~x  |  x와 y의 비트별 논리 부정     |

* 시프트 연산자는 변주에 저장된 데이터를 비트 단위로 이등시키는 연산자로 왼쪽(<<) 으로 오른쪽(>>) 으로 
지장한 수 만큼 비트 이동을 하는 것이다. 왼쪽으로 이동시긴 후 남는 자리는 2진수 값 0 으로 채워진다.
오른쪽으로 이동시키는 경우는 부호 비트가 0 이면 0을 채우고 부호 비트가 1 이면 1을 채운다. 

| 연산자 | 설멍 |
|:---------:|:------------------------------------------------:|
| x << n  |  변수 x 에 저장된 값을 n 비트 왼 쪽으로 이동             |
| x >> n  |  변수 x 에 저장된 값을 n 비트 오른 쪽으로 이동     |

## 증감 연산자

증감 연산자는 변수의 값에 1을 더하거나 1을 빼는 연산자로 연산자가 변수 앞에 있는 경우를 "전위 증감" 연산자가 
변수 뒤에 있는 경우를 "후위 증감" 이라 한다. 전위, 후위의 의미는 다른 연산자와 함께 사용될 때
다른 연산자 보다 먼저 처리 (전위 증감)되는가 후에 처리 (후위 증감) 되는가를 지정하는 것이다. 


| 연산자 | 설멍 |
|:---------:|:------------------------------------------------:|
| x++   |  x를 1 증가시키는 후위 증가    |
| ++x   |  x를 1 증가시키는 전위 증가     |
| x--  |  x를 1 감소시키는 후위 감소     |
| --x  |  x를 1 감소시키는 전위 감소     |


## 연산자 우선 순위



<table>
<tr>
<th> 우선순위</th>
<th> 연산자</th>
<th> 설명</th>
<th> 결합방향</th>
</tr>
<tr>
<th> 1
</th>
<td> <code>::</code></td>
<td> 범위 지정 (Scope resolution)</td>
<td rowspan="6"> 좌 → 우</td>
</tr>
<tr>
<th rowspan="5"> 2 </th>
<td> <code>++</code>   <code>--</code> </td>
<td> 후위 증가와 감소</td>
</tr>
<tr>
<td> <code>()</code></td>
<td> 함수호출</td>
</tr>
<tr>
<td> <code>[]</code></td>
<td> 배열 첨자</td></tr>
<tr>
<td> <code>.</code></td>
<td> 참조로 요소 선택</td>
</tr>
<tr>
<td> <code>-&gt;</code></td>
<td> 포인터를 통해 요소 선택</td>
</tr>
<tr>
<th rowspan="9"> 3</th>
<td> <code>++</code>   <code>--</code></td>
<td> 전위 증가와 감소</td>
<td rowspan="9"> 우 → 좌</td>
</tr>
<tr>
<td> <code>+</code>   <code>−</code></td>
<td> 단항 부호 연산자</td>
</tr>
<tr>
<td> <code>!</code>   <code>~</code></td>
<td> 논리 부정, 비트단위 부정</td>
</tr>
<tr>
<td> <code>(<i>type</i>)</code></td>
<td> 타입 캐스트</td>
</tr>
<tr>
<td> <code>*</code></td>
<td> 역참조</td>
</tr>
<tr>
<td> <code>&amp;</code></td>
<td> 주소값</td>
</tr>
<tr>
<td> <code>sizeof</code></td>
<td> Size-of 연산자</td>
</tr>
<tr>
<td><code>new</code>, <code>new[]</code></td>
<td> 동적 메모리 할당</td>
</tr>
<tr>
<td><code>delete</code>, <code>delete[]</code></td>
<td> 동적 메모리 해제</td>
</tr>
<tr>
<th> 4</th>
<td> <code>.*</code>   <code>-&gt;*</code></td>
<td> 멤버 포인터 접근</td>
<td rowspan="12"> 좌 → 우</td>
</tr>
<tr>
<th> 5</th>
<td> <code>*</code>   <code>/</code>   <code>%</code></td>
<td> 곱셈, 나눗셈, 나머지</td>
</tr>
<tr>
<th> 6 </th>
<td> <code>+</code>   <code>−</code></td>
<td> 더하기, 빼기</td>
</tr>
<tr>
<th> 7</th>
<td> <code>&lt;&lt;</code>   <code>&gt;&gt;</code></td>
<td> 비트 왼쪽 시프트와 오른쪽 시프트</td>
</tr>
<tr>
<th rowspan="2"> 8</th>
<td style="border-bottom-style: none"> <code>&lt;</code>   <code>&lt;=</code></td>
<td style="border-bottom-style: none"> 비교(관계) 연산자 &lt; 와 ≤</td>
</tr>
<tr>
<td> <code>&gt;</code>   <code>&gt;=</code></td>
<td> 비교(관계) 연산자 &gt; 와 ≥</td>
</tr>
<tr>
<th> 9 </th>
<td> <code>==</code> <code>!=</code> </td>
<td> 비교(관계) = 와 ≠</td>
</tr>
<tr>
<th> 10</th>
<td> <code>&amp;</code></td>
<td> 비트 곱</td>
</tr>
<tr>
<th> 11</th>
<td> <code>^</code></td>
<td> 비트 배타적 곱 (exclusive or)</td>
</tr>
<tr>
<th> 12</th>
<td> <code>|</code></td>
<td> 비트 합 (inclusive or)</td>
</tr>
<tr>
<th> 13</th>
<td> <code>&amp;&amp;</code></td>
<td> 논리 곱</td>
</tr>
<tr>
<th> 14</th>
<td> <code>||</code></td>
<td> 논리 합</td>
</tr>
<tr>
<th rowspan="6"> 15</th>
<td> <code>?:</code></td>
<td> 조건 연산자 (삼항 연산자)</td>
<td rowspan="7"> 우 → 좌</td>
</tr>
<tr>
<td> <code>=</code></td>
<td> 직접 대입 (C++ 클래스를 위해 기본 제공)</td>
</tr>
<tr>
<td> <code>+=</code>   <code>−=</code></td>
<td> 합과 차 대입</td>
</tr>
<tr>
<td> <code>*=</code>   <code>/=</code>   <code>%=</code></td>
<td> 곱, 몫, 나머지 대입</td>
</tr>
<tr>
<td> <code>&lt;&lt;=</code>   <code>&gt;&gt;=</code></td>
<td> 비트 왼쪽 쉬프트와 오른쪽 쉬프트 후 할당</td>
</tr>
<tr>
<td> <code>&amp;=</code>   <code>^=</code>   <code>|=</code></td>
<td > 비트연산 곱, 배타곱, 합 연산 후 대입</td>
</tr>
<tr>
<th> 16</th>
<td> <code>throw</code></td>
<td> (예외를 위한)Throw 연산자</td>
</tr>
<tr>
<th> 17</th>
<td> <code>,</code></td>
<td> 콤마</td>
<td> 좌 → 우</td>
</tr></table>