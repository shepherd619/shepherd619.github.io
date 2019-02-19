---
layout: default
title:  "flex box에 대하여"
date:   2018-08-27 00:00:00
categories: main
---

# flex box에 대하여

## flexbox
- display: flex 속성을 준 요소
- flexbox의 직계자식은 자동으로 flex-item이 된다.
- 기본적으로 화면을 그릴 때 한줄만 그리게 되어있다. = flex line 
- box기준으로 축이 생긴다.
    - main-axis = 기본적으로 flex-item이 배치되는 축, 기본은 row
    - cross-axis = main-axis와 교차되는 축
- flexbox 에는 다음과 같은 속성이 올 수 있다.
    - flex-direction : 위의 축을 바꾸는 속성. main-axis와 cross-axis를 변경할수있다.
    - justify-content : 메인축에 대한 속성을 지정한다 (그래서 flex-direction에 따라 바뀌어 적용되는것)
    - align-items : 크로스축에 대한 속성을 지정한다
    - flex-wrap : flex-box가 꽉차면 줄바꿈을 시켜줌 (윗줄에서 가장 아래쪽에 위치한 애가 시작점이 됨)
    - align-content : flex-box가 flex-wrap일 때, 여러줄의 flex요소들을 배치하는 법을 정의
    
## flexitem
- display: flex된 요소의 자식 요소들은 flexitem이 된다.
- flexitem에는 절대적(absolute) 및 상대적(relative) 플렉스 아이템 이 있다.
    - 이 둘의 주요 차이점은 간격(spacing)과 계산(computed) 방법에 있다.
    - 상대적 플렉스 아이템(relative flex item)의 간격은 컨텐츠 크기에 따라 계산된다.
    - 절대적 플렉스 아이템(absolute flex item)에서는 컨텐츠와 상관없이 "플렉스(flex)"에만 기반한다.
- flexitem 에는 다음과 같은 속성이 올 수 있다.
    - order : flex-item간의 배치순서를 바꿀수 있음 (html 마크업과는 무관하다)
    - align-self : 크로스축에 대해 자신이 어떻게 정렬될것인가를 정의. 부모가 정렬한 속성을 무효화하고 자신의 정렬방식대로 움직인다.
    - flex-grow : flex영역 안에서 공간이 남을 때 어디까지 늘어날것인가
    - flex-shrink : flex영역 안에서 공간이 없을 때 어디까지 수축될것인가 
    - flex-basis :
        - auto : 자신 안에 있는 컨텐츠만큼 차지 (기본값)
        - 값의 단위(width에 줄 수 있는 모든 단위) : 지정하면 값대로 차지
        - max- : max- 값이 flex속성보다 우선순위를 갖는다.
    - flex: none | [ <‘flex-grow’> <‘flex-shrink’>? || <‘flex-basis’>
        - none = flex: 0 0 auto와 같다.
        - auto = flex: 1 1 auto와 같다.
        - initial = flex: 0 1 auto와 같다.
        - 정수 = flex: 정수 1 0과 같다.

## flexitem과 margin
- 플렉스 아이템에서 margin: auto를 사용하면 auto 값을 갖는 방향 (왼쪽, 오른쪽 또는 양쪽 모두)으로 빈 공간을 채운다.
- 예를들어 ....

## 참고글
- [Flexbox 이해: 당신이 알아야 할 모든 것 (Understanding Flexbox: Everything you need to know)](https://www.vobour.com/3-flexbox-%EC%9D%B4%ED%95%B4-%EB%8B%B9%EC%8B%A0%EC%9D%B4-%EC%95%8C%EC%95%84%EC%95%BC-%ED%95%A0-%EB%AA%A8%EB%93%A0-%EA%B2%83-understa)
- [flexbox-grow, flex-shrink, flex-basis について](http://memowomome.hatenablog.com/entry/2016/09/06/080000)