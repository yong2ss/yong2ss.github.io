---
layout: post
title: Template Engine
tags: [Tech, Tech]
excerpt_separator: <!--more-->
---

About Template Engine
<!--more-->
## Template Engine
동적 컨텐츠를 생성하는 방법이다.<br>
템플릿 양식(웹 템플릿) + 데이터 모델(웹 컨텐츠 정보)로 결과 문서를 출력한다.<br>
웹 템플릿 엔진은 VIEW / DATA를 분리해준다<br>

## Java Template Engine
### Spring/Java에서 주로 사용하는 자바 템플릿 엔진 리스트
* FreeMarker
* Groovy
* Thymeleaf
* Mustache
* Velocity
* JSP

임베디드 서블릿 컨테이너를 사용하는 Spring Boot환경에서는 JSP를 권장하지 않습니다.1) JAR 패키징도 할 수 없으며 의존성 문제도 발생합니다.<br>
Velocity는 Spring에서도 4.3부터 사용이 중단되었습니다.
<br>

Spring Boot에서는 (FreeMarker/Groovy/Thymeleaf/Mustache)이 4가지를 자동 지원합니다.<br>
Spring Boot에서 자동 지원하는 위의 4가지를 비교해봅시다.
<br>

### 빌드 크기
또한 각 템플릿 엔진의 빌드 크기 (Size)가 작은 순서로 비교해보면<br>
Mustache > Thymeleaf > FreeMarker > Groovy 순입니다.
<br>

### 부팅 시간
각 템플릿 엔진의 애플리케이션 부팅 시간입니다<br>
부팅하는게 걸리는 시간이 적은 순서로 비교해봅시다.<br>
Mustache > FreeMarker >= Thymeleaf > Groovy
<br>

### 벤치마크
다음은 각 템플릿 엔진의 벤치마크 결과입니다.<br>
(Mustache = FreeMarker = Thymeleaf) > Groovy<br>
<br>

### 확장성
사용자 측면의 확장성이다.<br>
Thymeleaf > Mustache > (FreeMarker = Groovy)<br>
Thymeleaf는 확장성이 뛰어나며 Mustache는 복잡한 방법을 통하여 약간의 확장이 가능은 합니다.
<br>

### 러닝커브(학습 곡선) 
FreeMarker > Thymeleaf > Mustache > Groovy<br>
FreeMarker는 가독성이 좋고 HTML을 알고있다면 이해하기 쉬운 형태로 되어있습니다.<br>
Thymeleaf는 다양한 IDE에서 지원하므로 다음으로 쉽습니다.<br>
Groovy와 같은 경우는 아예 다른 표기법을 사용하기 때문에 가장 난이도가 높습니다.
<br>

### IDE지원
(FreeMarker = Thymeleaf) > Mustache > Groovy<br>
FreeMarker와 Thymeleaf는 상당한 IDE의 지원을 받고 있습니다.<br>
Mustache는 플러그인을 통하여 IDE의 지원을 받습니다.
<br>

### 유용성(사용에 편리함)
Thymeleaf >= FreeMarker > Groovy > Mustache 
FreeMarker는 HTML의 대부분의 기능을 가지고 있습니다. 여기에 사용자 지정 기능까지 추가된 것이 Thymeleaf라 보시면 됩니다.<br>
Mustache는 두 개를 숫자를 추가하고 템플릿 결과 내에서 인쇄하는 경우 불가능합니다. 실제 사용방법이 어렵고 굉장히 복잡합니다.<br>
<br>

### 결론
Thymeleaf와 FreeMaker가 현실적으로 가장 사용하기 좋은 템플릿 엔진입니다.<br>
다만 Freemarker는 몇 년동안 업데이트가 멈춰있어, Spring Boot에서 권장하지 않습니다.<br>
그리고 종합 점수로 비교해보면 Thymeleaf가 가장 사용하기 좋습니다.

<br><br>

## 참고 자료
1)https://docs.spring.io/spring-boot/docs/2.1.5.RELEASE/reference/htmlsingle/#boot-features-jsp-limitations
2)https://springhow.com/spring-boot-template-engines-comparison/
