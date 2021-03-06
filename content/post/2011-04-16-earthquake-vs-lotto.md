---
title: 3월 11일 일본 대지진이 일어날 확률과 로또에 당첨될 확률 어느쪽이 더 높을까?
date: 2011-04-16
categories:
  - 통계 이야기
tags:
  - 로또
  - 일본 지진
  - 확률
slug: earthquake-vs-lotto
---
일본 대지진이 일어난 지 벌써 한 달이 지났습니다. 아직 후쿠시마 원전 사고는 수습될 기미가 보이지 않고, 피해지역의 고충도 여전히 진행 중입니다.  
오늘 인터넷 서핑을 하다가 흥미로운 사이트를 알게 되었습니다. 전 세계의 지진 관측데이터를 수집하고 공표하는 사이트 [Earthquake Hazard Program][1] 입니다. 이곳에서는 1973년 이후 세계 전역에서 발생한 모든 지진 데이터를 데이터베이스에 보관하고 있습니다. 이 데이터를 이용해 3월 11일 대지진이 일어날 확률과 로또에 당첨될 확률을 비교해 보겠습니다.  

  
먼저, 1973년 이후 2011년 3월 10일까지 데이터베이스에는 총 34,506건의 지진이 등록되어 있습니다. 이를 지진의 규모(Magnitude) 0.1단위로 그래프를 그려 보면 다음과 같습니다. 그래프의 세로축은 각 진도가 전체 데이터에서 차지하는 비율을 의미합니다.

![](/images/2011-04-16-fig1.jpg)

저의 예상으로는 규모 0~3 사이의 소규모 지진이 가장 잦을 것 같았는데, 실제 그래프를 그려보니 그렇지 않더군요. 데이터 전체의 평균 규모는 4.43입니다. 즉, 몸으로 느낄 수 있는 정도의 지진이 가장 자주 발생함을 알 수 있습니다. 그리고 그래프의 모양을 보면 평균근처에 가장 많은 관측값이 모여 있고, 관측값이 작거나 커질수록 그 비율은 점점 낮아집니다. 우리 주변의 데이터는 대부분 이런 모양을 하고 있는데, 통계학에서는 이러한 모양의 데이터 분포에 대해 정규분포(Normal distribution)를 따른다고 합니다. 그래프의 파란 실선이 바로 이론적인 정규분포의 모습입니다. 일견 실제 관측값과 이론적인 값이 다르게 보이지만, 이 데이터는 정규분포를 따른다고 해도 큰 무리는 없습니다. 또한, 지진 규모의 표준편차(평균으로부터 각 관측값이 어느 정도 떨어져 있나를 판단하는 기준)는 0.953입니다. 통계에서는 평균으로 부터 표준편차의 3배보다 작거나 큰 값은 이상치(outlier)라고 해서 이러한 값이 관측될 확률은 아주 낮다고 생각합니다. 그래프에서는 이 값을 붉은색 점선으로 나타냈습니다.

이번 일본 대지진의 규모 9.0은 어디에 위치할까요? 그래프에도 표시했습니다만 이상치의 상한값(7.29)보다도 훨씬 높은 값임을 알 수 있습니다.

이상의 사실을 이용하면 규모 9.0 이상의 지진이 발생할 확률을 구할 수 있습니다. 계산 결과에 의하면 0.000000827입니다. 퍼센트로 나타내면 0.0000827%입니다. 한편, 로또에 당첨될 확률은 얼마일까요? 45개의 숫자 중 6개를 골라 1등에 당첨될 확률은 0.0000123%입니다.

이번 지진이 얼마나 일어나기 어려운 일인지 감이 잡히시나요?  
확률상으로는 백이십만 번의 지진에 한번 일어날까 말까 하는 정도의 지진입니다.

 [1]: http://earthquake.usgs.gov/
