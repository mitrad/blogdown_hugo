---
title: '[SAS] 숫자가 포함된 문자열의 정렬'
date: 2008-08-08
categories:
  - SAS
tags:
  - data step
  - SAS
slug: sorting-strings-containing-numbers
---
<span style="font-size: 24px;">Q.</span> 다음과 같은 데이터셋이 존재한다고 했을 때, 문자열변수 안의 숫자의 크기순으로 정렬하고 싶지만, 이대로 PROC SORT를 이용하면 A-1, A-10, A-12, A-2의 순으로 정렬됩니다. 문자열 안의 숫자의 크기 순으로 정렬하는 방법은 없나요?

![](/images/2008-08-08-fig1.jpg)

<span style="font-size: 24px;">A.</span> 정렬을 하기 전에 id 변수의 숫자의 앞에 0을 추가할 필요가 있습니다. 0을 추가하려면 다음과 같은 과정이 필요합니다.

1.  scan 함수를 이용하여 변수를 &#8220;-&#8221; 문자를 기준으로 분리
2.  Zw.d 포맷을 이용하여 수치 문자열의 앞에 0을 추가
3.  CATX함수를 이용하여 전후의 공백을 없애고 분할할 문자열을 연결

예)

```
DATA test;
  INPUT id $ age $ @@;
  DATALINES;
A-1 10 A-2 15 A-3 9 A-5 5
A-8 6 A-9 3 A-10 12 A-12 7
B-3 9 B-5 3 B-8 4 B-9 6
B-11 7 B-15 10
;
DATA test2;
  FORMAT id3 age;
  SET test;
 
ID1 = SCAN(id,1,'-');
ID2 = PUT(INPUT(SCAN(id, 2, '-'),best.),Z2.);
ID3 = CATX('-', id1, id2); RUN;
 
PROC SORT DATA=test2(KEEP = id3 age);
  BY id3;
RUN;
```

