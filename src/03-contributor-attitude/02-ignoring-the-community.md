> 아직 작성 중입니다.

# 공동체를 고려하지 않은 기여

오픈소스 기여는 결과물을 제출하는 것으로 끝나지 않습니다. Issue와 PR을 검토하고 병합한 뒤 유지하는 데에는 다른 참여자의 시간과 노력이 필요합니다.   
따라서 프로젝트의 규칙과 상황을 고려하지 않은 기여는, 악의가 없더라도 그 비용을 공동체에 떠넘길 수 있습니다.

대표적으로 다음과 같은 경우입니다.

* 기여 안내와 기존 논의를 확인하지 않고 Issue나 PR을 제출합니다.
* 직접 재현하거나 이해하지 않은 문제를 보고합니다.
* 먼저 논의해야 할 큰 변경을 완성한 뒤 병합을 요구합니다.
* 실행하지 않은 테스트나 확인하지 않은 내용을 사실처럼 설명합니다.
* 리뷰 의견에 답하지 않거나 공격적으로 반응합니다.
* 배지, 현상금이나 기여 횟수를 목적으로 비슷한 제출을 반복합니다.

> 물론 저런 상황이 항상 나쁜 결과가 되는건 아닙니다. 결과적으로 좋을수도 있는데, 바람직한 행동은 아님.
> ~~[씨맥의 죽빵론](https://youtube.com/shorts/y7Jh9Lg-tF8?si=UdzsFvO2OPi6UVWt)~~

## 기여의 검토·유지 비용

Issue나 PR을 제출했다고 해서 검토되거나 병합될 권리가 생기는 것은 아닙니다. 메인테이너는 변경 자체뿐 아니라 필요성, 프로젝트 방향, 호환성, 보안, 이후의 유지보수 비용까지 함께 판단해야 합니다.

따라서 프로젝트는 자신이 감당할 수 있는 범위와 방식으로 기여를 받을 수 있으며, 외부 PR을 받지 않을 수도 있습니다. 대표적으로 SQLite는 일반적인 외부 기여를 받지 않습니다.

즉, 기여자가 만드는 비용은 코드를 작성하는 데서 끝나지 않습니다. 제출한 내용을 이해하고 검증하지 않았다면 그 확인 작업까지 메인테이너가 대신 떠안게 됩니다.

> SQLite의 제작자인 Richard Hipp는 외부 기여자의 제안을 **공짜 강아지**에 비유해 기여를 받지 않는 이유를 설명했습니다. 변경을 받아들이는 순간 이후의 관리 책임도 함께 생기기 때문입니다.

## AI를 통한 비용 전가

공동체를 고려하지 않은 기여는 AI 이전에도 있었습니다. 달라진 점은 제출물을 만드는 비용입니다.   
AI를 사용하면 결과물을 빠르고 그럴듣하게 만들 수 있지만, 생성된 결과가 필요한지 이해하고 정확한지 검증하는 비용까지 사라지는 것은 아닙니다.

그 결과 AI는 기존의 문제를 크게 두 방향으로 악화시킬 수 있습니다.

### 검토 비용의 비대칭적 증가

기여자가 PR이나 보고서를 만드는 비용은 크게 낮아졌지만, 메인테이너가 그 필요성과 정확성을 확인하는 비용은 그만큼 줄지 않았습니다.

따라서 이해하거나 검증하지 않은 제출이 많아질수록 메인테이너의 한정된 리뷰 시간이 소모되고, 실제로 필요한 기여의 검토까지 늦어질 수 있습니다.   
생성한 결과를 검증하지 않은 채 다른 사람에게 처리 비용을 넘기는 이러한 결과물을 흔히 **AI slop**이라고 부릅니다.

### 지식·신뢰 축적의 부재

리뷰는 결과물을 통과시키는 절차만이 아닙니다. 기여자는 문제를 이해하고 피드백을 반영하면서 프로젝트에 대한 지식을 쌓고, 반복해서 참여하며 다른 참여자와 신뢰를 형성합니다. 이 과정에서 문서만으로 전달하기 어려운 지식도 공동체 안에 축적됩니다.

하지만 제출자가 생성된 코드를 이해하지 않았다면 리뷰를 받아도 이러한 학습이 이어지기 어렵습니다. 

메인테이너 역시 제출자가 변경을 이해하고 이후의 수정이나 유지에 책임질 수 있는지 판단하기 어렵습니다. 결과물 하나는 남더라도, 장기적으로 프로젝트를 함께 유지할 사람과 지식은 남지 않을 수 있습니다.

따라서 문제는 AI 사용 자체가 아니라 **이해와 검증을 생략한 채 결과만 제출하는 것**입니다. AI를 코드 탐색과 검증에 활용해 자신의 이해를 깊게 하는 경우와, 읽거나 확인하지 않은 결과를 그대로 제출하는 경우는 구분해야 합니다.

## 실제 프로젝트의 문제 사례

이러한 문제는 여러 프로젝트에서 실제 대응으로 이어졌습니다.

### 주요 사례

이러한 문제는 여러 오픈소스 프로젝트에서 실제로 나타났습니다.

* **Spring**에서는 AI로 생성된 것으로 보이는 무관한 Issue와 중복·유효하지 않은 보안 보고가 늘어나면서 검토 부담이 문제가 되었습니다. [관련 Issue 사례][spring-unrelated-ai-issue]와 [보안 보고 회고][spring-ai-security]에서 자세한 내용을 볼 수 있습니다.
* **Rustlings**는 가이드를 따르지 않는 기여가 많고, 이를 닫는데 비용이 듦?. [async/await 연습문제 PR][rustlings-async-pr]과 [불필요한 변경 PR][rustlings-slop-pr]이 대표적인 사례입니다.
* **curl**은 저품질 보안 보고가 급증하면서 2026년 2월 버그 바운티를 중단했고, 이후 접수 방식을 변경해 다시 운영했습니다. 자세한 경과는 [High-Quality Chaos][curl-high-quality-chaos]에서 설명합니다.

프로젝트마다 문제의 형태와 대응 방식은 다릅니다.   
그러나 공통적으로 필요한 것은 제출자가 자신의 기여에 필요한 검토 비용을 줄이고, 제출한 내용에 책임질 수 있어야 한다는 점입니다.

## 참고 자료

* [Richard Hipp의 공짜 강아지 비유][richard-hipp-free-puppy]: PR을 받아들인 뒤 생기는 장기 유지보수 부담
* [SQLite의 기여 방식][sqlite-open-not-open-contribution]: 일반적인 외부 PR을 받지 않는 프로젝트의 공식 설명
* [Nobody's job, everybody's problem: F/OSS in the age of AI][hongminhee-foss-ai-talk]: AI 기여가 만드는 신뢰와 리뷰 용량 문제
* [Spring and Security In The Times Of AI][spring-ai-security]: AI 기반 보안 보고의 증가와 검토 과정
* [High-Quality Chaos][curl-high-quality-chaos]: curl의 AI slop 경험과 이후의 변화

{{#include ../_includes/references.md}}

[curl-high-quality-chaos]: https://daniel.haxx.se/blog/2026/04/22/high-quality-chaos/
[richard-hipp-free-puppy]: https://youtu.be/lSVgeMoXJTs?t=923
[rustlings-async-pr]: https://github.com/rust-lang/rustlings/pull/2413
[rustlings-slop-pr]: https://github.com/rust-lang/rustlings/pull/2401
[spring-ai-security]: https://spring.io/blog/2026/06/01/spring_and_security_in_the_times_of_ai/
[spring-unrelated-ai-issue]: https://www.linkedin.com/posts/snicoll_goodbye-albon-idrizi-httpslnkdin-activity-7405253562458378240-Jxu9/
[sqlite-open-not-open-contribution]: https://github.com/sqlite/sqlite#public-domain
