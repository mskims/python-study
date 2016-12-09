# 파이썬

<span class="confluence-embedded-file-wrapper">![](https://wikidocs.net/images/page/5/pahkey_KRRKrp.png)</span>

> 1991년 귀도 반 로섬이 발표한 C기반의 객체 지향적 대화형 프로그래밍 언어 이다.

## 특징

*   간결하고 쉬운 (직관적인) 문법
*   빠른 개발 속도
*   오픈소스

### 간결하고 쉬운 문법

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">print 'hello world!'</pre>

</div>

</div>

파이썬에서 hello world 를 출력하기 위한 코드는 단 한줄!

### 사라진 세미콜론

파이썬의 가장 큰 특징 중 하나가 생소한 문법이다.

파이썬은 다른 보편적인 언어와 달리 명령어 끝에 세미콜론을 쓰지 않는다.

아 물론 세미콜론을  붙여도 문제없이 동작 하지만 파이썬이 공식으로 제공하는 코드 컨벤션인 PEP가 경고한다. 

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">print 'Where is semicolon?'</pre>

</div>

</div>

### 들여쓰기 scope

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs"># Python
if Condition:
	do_something()
// JS
if(condition){
	do_something()
}</pre>

</div>

</div>

파이썬의 코드블럭이다.

이 해괴 망측한 문법은 코드블럭을 { }  로 구분하는 대신 가독성이 뛰어나다는 이유로 들여쓰기로 구분한다. 쓰다보니 편하네요.

### PEP8

파이썬이 제공하는 PEP라는 코드 스타일 가이드이다.

다른 언어로 짜여진 프로젝트들을 보면 코드 스타일이 다르지만 파이썬은 엄격하게 가이드라인을 만들어 제시하고 있다.

1.  들여쓰기는 공백 4칸을 권장합니다.
2.  한줄은 최대 79자까지 (????)
3.  최상위(top-level) 함수와 클래스 정의는 2줄씩 띄어 씁니다.
4.  클래스 내의 메소드 정의는 1줄씩 띄어 씁니다.

파이참은 칼같이 이 가이드라인을 지킨다.

<span class="confluence-embedded-file-wrapper">![](attachments/92864570/95551554.png)</span>

우리 모두 지켜 씁시다. 

## 자료형

### 숫자형

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">a = 1</pre>

</div>

</div>

평범하다.

### 문자열

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">a = 'this is string'</pre>

</div>

</div>

#### 문자열 내장함수

문자열은 많은 함수를 가지고 있다.

''capitalize', 'center', 'count', 'decode', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'index', 'isalnum', 'isalpha', 'isdigit', 'islower', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'partition', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill'......

그중 몇개를 자세히 알아보자.

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">a = 'Hello String'
a.upper(), a.lower()	# 'HELLO STRING', 'hello string'
'i am min seok kim'.title	# 'I Am Min Seok Kim'</pre>

</div>

</div>

파이썬에서 자주 쓰이는 String.format 함수를 알아보자.

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">'I am {}'.format('Babo')	# 'I am Babo'
'I love {0} and {1}'.format('you', 'me')	# I love you and me
'{s} {v} {o}'.format(s='Modernize', v='Your', o='DBMS')	# Modernize Your DBMS

'{s} {v} {o}'.format({ 's': 'Mordernize', 'v': 'Your', 'o': 'DBMS' })	# KeyError: 's'</pre>

</div>

</div>

### 튜플

파이썬은 튜플이란 이상한 데이터 형태를 가지고있다.

#### 기본형태

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">a = 1
b = 2
tuple = a, b
print tuple		# (1, 2)</pre>

</div>

</div>

이런것도 가능하다

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">a, b = 1, 2
a # 1
b # 2</pre>

</div>

</div>

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">def func(a, b):
	return a + b
tuple = 1, 2
print func(*tuple)	# 3</pre>

</div>

</div>

ㅎㄷㄷ

### 딕셔너리

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">a = {
	'key': 'value',
	'key2': 'value2'
}
# 이렇게 선언할 수도 있다.
b = dict(
	key='value',
	key2='value2'
)</pre>

</div>

</div>

보기엔 JSON 과 유사해보인다.

딕셔너리는 키와 값 한쌍을 갖는 데이터 집합이다.

키는 중복될 수 없으며 키값이 중복되있으면 한 값만 남는데, 보통 뒤에 선언된 값이 남는다.

항상 그렇다는건 아니다. 중복되게 쓰지 마세요.

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">a = {
	'key': 'value',
	'key': 'value?'
}
a	# { 'key': 'value?' }</pre>

</div>

</div>

#### 주소 참조

딕셔너리의 복사에 대해 이야기 해보자.

딕셔너리의 복사는 2종류가 있는데 코드로 봅시다.

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">a = {
	'key': 'value',
	'key2': 'value2'
}
b = a
del b['key2']
print a</pre>

</div>

</div>

print a 의 결과값은 { 'key': 'value' } 이다.

일반 대입식처럼 딕셔너리를 새로운 변수에 대입했을 경우엔 값을 복사하는게 아니고 딕셔너리의 주소를 복사하게 된다. 

포인터랑 비슷하다고 보면 된다.

값 자체를 복사해서 새로운 딕셔너리 객체를 만들고 싶으면 copy() 내장 함수를 사용하면 된다.

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">a = {
	'key': 'value',
	'key2': 'value2'
}
b = a.copy()
del b['key2']
print a # { 'key': 'value', 'key2': 'value2' }
print b # { 'key': 'value' }</pre>

</div>

</div>

#### 딕셔너리 제어

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">a = {
	'key': 'value',
	'key2': 'value2'
}
# 삭제
del a['key']
a	# { 'key2': 'value2' }</pre>

</div>

</div>

#### 반복문 적용하기

딕셔너리 객체 (파이썬에선 모든것이 객체이다) 는 keys, values, items... 함수를 프로토타입으로 가지고있다.

*   (Dict).keys() 함수는 딕셔너리의 키들을 리스트 형태로 반환한다.
*   (Dict).values() 함수는 딕셔너리의 값들을 리스트 형태로 반환한다.
*   (Dict).items() 함수는 딕셔너리의 키,밸류 쌍을 튜플로 묶어 리스트 형태로 반환한다.

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">a = {
	'key': 'value',
	'key2': 'value2'
}
a.keys()	# ['key', 'key2']
a.values()	# ['value', 'value1']
a.items()	# [('key', 'value'), ('key2', 'value2')]</pre>

</div>

</div>

여기서 주의해야 할 점이 있다. 이 책에선 파이썬 2버전으로 예제를 쓰고있지만 3버전 같은 경우엔 다르기 때문에 주의해야 한다.

파이썬 2.7 버전 까지는 keys, values, items 함수는 리스트 형태로 반환을 했지만 3.0 버전부터는 메모리 낭비의 이유로 리스트 객체가 아닌 이터러블(반복가능)한 객체를 반환해준다.

리스트는 아니기때문에 직접 접근할 수는 없지만 이터러블한 객체기때문에 반복문에 넣어도 아무 문제가 없고 메모리문제도 개선되어 성능을 향상시킬 수 있다.

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs"># in python 3
a = {
	'key': 'value',
	'key2': 'value2'
}
a.keys()	// dict_keys(['key2', 'key'])
a.values()
a.items()
for key in a.keys():
	print(key)</pre>

</div>

</div>

#### 딕셔너리 리터럴/함수 선언 방식 퍼포먼스 비교

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: bash; gutter: false; theme: Emacs" data-theme="Emacs">$ python -m timeit "d=dict(prop='val')"
10000000 loops, best of 3: 0.219 usec per loop
$ python -m timeit "d={'prop': 'val'}"
10000000 loops, best of 3: 0.075 usec per loop

$ python3 -m timeit "d = dict(prop='val')"
1000000 loops, best of 3: 0.475 usec per loop
$ python3 -m timeit "d = {'prop': 'val'}"
10000000 loops, best of 3: 0.143 usec per loop</pre>

</div>

</div>

리터럴 선언 방식이 더 빠르다.

### 집합

## 제어문

### if

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">if condition:
	print 'Oh its true'

tFlag, fFlag = True, False
if not fFlag:	# if fFlag != True
	print '!'
elif tFlag:		# else if tFlag == true
	print '!!'
else:
	print '..'</pre>

</div>

</div>

### while

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">while condition:
	do_something()
	if condition:
		break	# 반복문 종료
	elif condition:
		continue	# 현재 반복 종료 (다음 반복으로 넘어감)</pre>

</div>

</div>

### for

<div class="code panel pdl" style="border-width: 1px;">

<div class="codeContent panelContent pdl">

<pre class="syntaxhighlighter-pre" data-syntaxhighlighter-params="brush: py; gutter: false; theme: Emacs" data-theme="Emacs">for value in ITERABLE_VARIABLE:
	print value

for i in [1, 2, 3, 4, 5]:
	print value 
# 1
# 2
# ...
d = {
	'key': '11',
	'key2': '22'
}
for key in d:
	print key
# key
# key2
for key, value in d:
	print key, value</pre>

</div>

</div>

## 핵심 기능

### 클래스, 모듈

### 패키지

### 예외

### 익명함수 (람다)

### dunder variables

## 카드놀이
