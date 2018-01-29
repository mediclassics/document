---
layout: post
title:  "한의학고전DB 이용 가이드"
categories: guide
---

[한의학고전DB](http://mediclassics.kr/), 이렇게 이용하시면 편리합니다.


주요메뉴
--------

### 1. 열람

##### 1.1. 서적 네비게이션(목차)


[![](http://i.imgur.com/IW4cNXrm.png)](http://i.imgur.com/IW4cNXr.png)

- 본문 왼쪽의 파랑색 막대기는 현재 선택된 문단을 의미합니다.
- 서적 네비게이션은 현재 문단이 속한 목차를 의미합니다.
- 서적 네비게이션을 클릭하면 해당 부분으로 이동합니다.

##### 1.2. 설정 버튼 (언어 / 주석 / 글자크기)

[![](http://i.imgur.com/ZpPfLaAm.png)](http://i.imgur.com/ZpPfLaA.png)

- 언어별로 각각 볼 수 있습니다.
- 로그인 후에 언어를 설정하면 다음 로그인할 때에도 설정이 유지됩니다.
- 주석은 역자주![](https://mediclassics.kr/img/common/book_exp01.png)와 교감기![](https://mediclassics.kr/img/common/book_exp02.png)로 나뉩니다. 역자주![](https://mediclassics.kr/img/common/book_exp01.png)는 번역자가 작성한 주석이며, 교감기![](https://mediclassics.kr/img/common/book_exp02.png)는 다른 판본과 대조하여 원문(한자)을 교감한 주석입니다.

##### 1.3. 기호

- 별표`*` : 번역에 반영된 교감 결과를 표시합니다. 빠져야할 글자는 `*없음`으로 표시합니다.
- 당구장표`※` : 역자주  혹은 교감기의 근거를 나타냅니다.
- 파자 : 쉴휴(休)는 `【人+木】`의 형태로 표기합니다.
- 신출자, 마멸자 : `◍`로 표기합니다.

##### 1.4. 스타일

- 양각 : 글자를 둘러싼 타원으로 표시합니다.

[![](http://i.imgur.com/tugXDvvm.png)](http://i.imgur.com/tugXDvv.png)


- 음각 : 회색 음영으로 표시합니다.

[![](http://i.imgur.com/UCuX5i2m.png)](http://i.imgur.com/UCuX5i2.png)

- 임의 삽입 구문 : 약한 그림자로 표시하고 역자주![](https://mediclassics.kr/img/common/book_exp01.png)를 답니다.

[![](http://i.imgur.com/kVCRXsMm.png)](http://i.imgur.com/kVCRXsM.png)

### 2. 검색

##### 2.1. 일반검색

- 한 단어를 검색하면 각 서적별로 제목/본문으로 나누어 검색 결과를 출력합니다.
- 2개 이상의 단어를 검색하면 해당 단어가 모두 포함된 검색 결과를 출력합니다.(AND 검색)
- 서적분류, 출간년도, 제목/본문, 언어로 검색결과를 필터링할 수 있습니다.

##### 2.2. 상세검색(Advanced)

- 서지사항(서명, 출간년 등)과 내용(제목/본문)과 역자주 필드에서 검색할 수 있습니다.
- 'add' 버튼과 연산자(AND/OR/NOT)를 사용하면 기존에 사용했던 검색어를 조합할 수 있습니다.
- 내용(제목/본문) 필드에서는 용어확장과 이체자 옵션을 추가할 수 있습니다.
- 이체자 옵션은 `甘草`를 검색할 때 `甘草`, `甘艸`, `甘艹` 등을 함께 검색해줍니다. `甘草/v[내용/본문-원문]`
- 용어확장 옵션은 `감초`를 검색할 때 `甘草`, `國老`, `粉草` 등을 함께 검색해줍니다. `감초/t[내용/본문-원문]`
- 용어확장 기능은 걸음마 단계이며 데이터를 계속 보완해가고 있습니다.
- 용어확장과 이체자 옵션은 동시에 사용할 수 있습니다. `감초/t/v[내용/본문-원문]`


<!--### 3. Open API

회원가입 후 홈페이지 하단의 'OPEN API'를 통해 신청해주세요.-->

* * *


서비스 예정 서적
----------------

[여기]({{ site.baseurl }}{% post_url 2016-01-22-mediclassics-plan %}) 서적들이 만들어지고 있습니다.
