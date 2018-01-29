---
layout: post
title:  "텍스트 구축에 사용된 마크업(markup) 문법"
categories: document
---

한의학고전DB 구축에는 고문헌 콘텐츠에 특화된 마크업 문법이 사용되었다. 이 문법은 KIOM 고문헌 연구팀 내부 실무 경험을 바탕으로 사용자에게 부담을 최소화 하면서 실용성을 강조하였다. 그 대략을 소개해 본다. 

***

문장기호(single line tag)
---------------

한 문장 안에 사용하는 테그이다. 크게 모양에 대한 정보를 담은 `형태기호(style tag)`와 교열 및 번역 연구 과정에서 생성된 `주석기호(annotation tag)`로 나뉜다.

### 형태기호(style tag)

고문헌을 살펴보면 글자의 크기, 음영 등으로 내용을 구분하는 경우가 많다. 이 때 `[ ]`를 사용하여 이러한 정보를 추가한다. 

형태	|	기호   | html example
----|---|---
작은글자 <small>(small)</small> | <kbd>[當歸]</kbd> | `<span class="size-sm">當歸</span>`
큰글자 <small>(large)</small> | <kbd>[lg/當歸]</kbd> | `<span class="size-lg">當歸</span>`
양각 <small>(positive / relief)</small>	|	<kbd>[ps/當歸]</kbd> | `<span class="print-ps">當歸</span>`
음각 <small>(negative / intaglio)</small>	|	<kbd>[ng/當歸]</kbd> | `<span class="print-ng">當歸</span>`

예를 들어 아래 첫번째 이미지와 같은 것은 `[ps/內疳][[ps/瘡]]生於口上腭...`와 같이, 두번째 이미지와 같은 것은 `單製[[ng/調經散]]當歸一錢半...`라고 입력한다. 

![](http://imgur.com/XLx8h6v.png%20/%22%EC%96%91%EA%B0%81%EC%98%88%EC%8B%9C%22)

![](http://imgur.com/1IPaUtn.png%20/%22%EC%9D%8C%EA%B0%81%EC%98%88%EC%8B%9C%22)


### 주석기호(annotation tag)

주석기호는 연구자가 원문 혹은 번역문의 이해를 돕기 위해 추가하는 정보로 `{  }`를 사용한다. 

유형	| 설명 |	기호 
----|----|---|---
교감기 | 원문 글자 교감 | <kbd>{A=B@출전}</kbd>, 여러개일 경우 <kbd>{A=B@출전1;C@출전2...}</kbd> 
역자주 | 원문 설명 | <kbd>{○○:독음!설명@출전}</kbd>
역자주 | 번역문 설명 | <kbd>{○○:설명@출전}</kbd>, 여러개일 경우 <kbd>{○○:설명@출전;설명@출전}</kbd>
기타 | 줄바꿈  | <kbd>{n}</kbd>

<br>
<br>

문단기호(multi line tag)
----------------

문단기호는 문단 전체의 속성에 대한 정보를 담고 있으며, 문단전체의 개요번호 혹은 메타데이터로 생각하면 된다.

### 표제

표제를 나타내는 문단기호는 2자로 표현되는데, 앞의 첫째 자리는 문단의 수준을, 둘째 자리는 문단의 의미를 나타낸다. 

예를 들어 표제의 경우 일반적으로는 `CC`와 같이 나타내며, 이는 2번째 큰 하위 제목이 된다. 

만약 `CP`와 같이 된다면 2번째 큰 하위 제목으로 처방명을 의미한다. 

기호|의미| html example
---|---|---
<kbd>AA</kbd>	 |	표제(주로 편명) | `<h1> ... </h1>`
<kbd>BB</kbd>	 |	표제(하위 제목들) | `<h2> ... </h2>`
<kbd>CC</kbd>	 |	표제(하위 제목들) | `<h3> ... </h3>`
<kbd>DD</kbd>	 |	표제(하위 제목들) | `<h4> ... </h4>`
<kbd>EE</kbd>	 |	표제(하위 제목들) | `<h5> ... </h5>`
<kbd>FF</kbd>	 |	표제(하위 제목들) | `<h6> ... </h6>`

기호|의미
---|---
<kbd>xP</kbd> 	|	처방 표제  
<kbd>xK</kbd> 	|	침구 표제  
<kbd>xH</kbd> 	|	본초 표제  

### 본문 

`ZZ`와 `SS`는 일반적으로 본문을 나타내며, 두번째 자리는 들여쓰기 정도를 의미한다. 

기호|의미| html example
---|---|---
<kbd>ZZ</kbd>	 |	본문 | `<p class="zz"> ... </p>`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<kbd>Z0</kbd>	|	본문(위로 1칸 내어쓰기)    | `<p class="zz up"> ... </p>`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<kbd>Z1</kbd>	|	본문(아래로 1칸 들여쓰기)    | `<p class="zz dn1"> ... </p>`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<kbd>Z2</kbd>	|	본문(아래로 2칸 들여쓰기)    | `<p class="zz dn2"> ... </p>`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<kbd>Z3</kbd>	|	본문(아래로 3칸 들여쓰기)    | `<p class="zz dn3"> ... </p>`
<kbd>SS</kbd> 	|	중간에 삽입된 본문(특히 방제)    | `<p class="ss"> ... </p>`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<kbd>S0</kbd>	|	본문(위로 1칸 내어쓰기)    | `<p class="ss up"> ... </p>`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<kbd>S1</kbd>	|	본문(아래로 1칸 들여쓰기)    | `<p class="ss dn1"> ... </p>`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<kbd>S2</kbd>	|	본문(아래로 2칸 들여쓰기)    | `<p class="ss dn2"> ... </p>`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<kbd>S3</kbd>	|	본문(아래로 3칸 들여쓰기)    | `<p class="ss dn2"> ... </p>`
<kbd>XX</kbd> 	|	표제어에 딸린 설명  |   `<span class="xx"> ... </span>`

### 기타

기타 도상과 표는 다음과 같이 나타낸다. 

기호|의미| html example
---|---|---
<kbd>PP</kbd> <small>(picture)</small>	|	도상(그림) |  `<img>`
<kbd>TT</kbd> <small>(table)</small>	|	표  | `<table> ... </table>`

텍스트를 한 줄에 표현해야 하기 때문에 표의 경우에는 `#`로 열과 열을 구분하였고 행은 본문과 마찬가지로 줄바꿈 기호인 `{n}`으로 구분하였다.


