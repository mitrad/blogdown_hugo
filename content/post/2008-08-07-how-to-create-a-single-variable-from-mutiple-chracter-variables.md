---
title: '[SAS] 복수의 문자변수의 값을 연결해 하나의 변수로 만드는 방법'
date: 2008-08-07
categories:
  - SAS
tags:
  - data step
  - SAS
slug: how-to-create-a-single-variable-from-mutiple-chracter-variables
---
<span style="font-size: 24px;">Q</span>. 복수의 문자변수 값을 컴마(,)로 연결해 하나의 변수로 만드는 방법은?

<span style="font-size: 24px;">A</span>. SAS 9 부터 추가된 CATX 함수를 이용하면 구분문자를 지정하여 문자열로 만들 수 있다.

```
DATA _NULL_;
   dlm=",";
   char1="Hong";
   char2="GilDong";
   char3="15";
   char4="A";
   results=CATX(dlm, OF char1-char4);
 
   PUT results;
RUN;
```

출력결과 : Hong,GilDong,15,A
