> 아직 작성 중입니다.

# 공동체를 고려하지 않은 기여

프로젝트를 단순히 결과물을 제출하는 장소로만 보면, 기여가 필요한지와 누가 이를 검토하고 유지할지는 놓치기 쉽습니다. 악의가 없더라도 공동체의 규칙과 상황을 고려하지 않은 기여는 다른 참여자의 부담이 됩니다.

대표적인 경우는 다음과 같습니다.

- 기여 안내와 기존 논의를 확인하지 않고 Issue나 PR을 제출합니다.
- 직접 재현하거나 이해하지 않은 문제를 보고합니다.
- 필요성을 먼저 논의해야 하는 큰 변경을 완성한 뒤 받아 달라고 요구합니다.
- 실행하지 않은 테스트나 확인하지 않은 내용을 사실처럼 설명합니다.
- 리뷰 의견에 답하지 않거나 공격적으로 반응합니다.
- 배지, 현상금이나 기여 횟수를 위해 비슷한 제출을 반복합니다.

## 기여도 유지보수 비용을 만든다

기여자가 Issue나 PR을 제출해도 검토와 병합을 요구할 권리가 생기지는 않습니다. 메인테이너는 변경의 필요성, 프로젝트 방향, 호환성, 보안과 앞으로의 관리 비용까지 검토해야 합니다.

프로젝트는 감당할 수 있는 범위와 방식으로 기여를 받을 수 있으며, 외부 PR을 받지 않을 수도 있습니다. 대표적으로 SQLite는 일반적인 외부 기여를 받지 않습니다.

> 제작자인 Richard Hipp는 외부 기여자의 제안을 **공짜 강아지**에 비유해 기여를 받지 않는 이유를 설명했습니다. 변경을 받아들이면 메인테이너가 이후에도 계속 관리해야 하기 때문입니다.

## AI로 인해 심해진 문제

공동체를 고려하지 않은 기여는 AI 이전에도 있었습니다. AI는 Issue, 코드와 설명을 만드는 비용을 낮추면서 이해하거나 검증하지 않은 결과도 쉽게 제출할 수 있게 했습니다. 이로 인해 두 가지 문제가 더 두드러졌습니다.

### 메인테이너의 검토 부담

PR을 만드는 비용은 크게 줄었지만, 메인테이너가 변경의 필요성과 정확성을 확인하는 비용은 그대로입니다. 이해하거나 검증하지 않은 제출이 늘어날수록 한정된 리뷰 시간이 소모되고 필요한 기여까지 늦어집니다.

이처럼 생성한 결과를 검증하지 않고 다른 사람에게 처리 비용을 넘기는 결과물을 흔히 **AI slop**이라고 부릅니다.

### 기여자의 지식 형성 단절

리뷰는 결과물을 통과시키는 절차만이 아닙니다. 기여자는 문제를 이해하고 피드백을 반영하는 과정에서 프로젝트에 대한 지식을 쌓고, 반복해서 참여하며 공동체와 신뢰를 형성합니다. 이 과정은 문서에 모두 담기 어려운 지식을 여러 참여자에게 나누는 공동체의 지식 형성이기도 합니다.

[홍민희님의 발표 자료][hongminhee-foss-ai-talk]는 이를 기여자가 프로그램에 대한 자기 나름의 이해를 만들어 가는 과정으로 설명합니다. 제출자가 생성된 코드를 이해하지 않았다면 리뷰가 반복되어도 이러한 지식이 쌓이기 어렵고, 메인테이너도 제출자가 변경을 이해하고 책임질 수 있는지 판단하기 어렵습니다. 결과물 하나는 남을 수 있지만 장기적으로 함께 프로젝트를 유지할 사람과 지식은 남지 않을 수 있습니다.

문제는 AI 사용 자체가 아니라 이해와 검증을 건너뛰는 사용입니다. AI를 코드 탐색과 검증에 활용해 이해를 깊게 하는 경우와, 읽지 않은 결과를 그대로 제출하는 경우는 구분해야 합니다.

### AI Slop 사례

실제로 다음과 같은 문제가 발생했습니다.

- Spring 메인테이너가 공유한 [프로젝트와 관계없는 Issue 제출 사례][spring-unrelated-ai-issue]에서는 제출자의 계정이 차단되었습니다.
- [Spring의 보안 보고 회고][spring-ai-security]에 따르면 AI 기반 보고가 급증하면서 중복되거나 유효하지 않은 보고도 늘었습니다.
- Rustlings는 요청하지 않은 AI 생성 연습문제와 저품질 AI 기여로 판단한 PR을 짧은 설명과 함께 닫았습니다. [async/await 연습문제 PR][rustlings-async-pr]과 [불필요한 변경으로 판단한 PR][rustlings-slop-pr]에서 볼 수 있습니다.
- curl은 저품질 보안 보고가 급증하자 2026년 2월 버그 바운티를 중단했습니다. 이후 접수 방식을 바꾸어 다시 열었지만 보고량 증가에 따른 부담은 계속되고 있습니다. 자세한 경과는 [High-Quality Chaos][curl-high-quality-chaos]에서 볼 수 있습니다.

메인테이너의 검토 부담과 기여자에 대한 신뢰는 서로 다른 문제이므로 프로젝트마다 대응 방식도 다릅니다. AI를 사용했다면 제출한 내용을 직접 이해하고 검증해야 하며, 별도의 사용 규칙이 있다면 [프로젝트마다 다른 AI 사용 규칙](03-project-ai-policies.md)도 확인합니다.

## 더 보기

- [Richard Hipp의 공짜 강아지 비유][richard-hipp-free-puppy]: PR을 받아들인 뒤 생기는 장기 유지보수 부담
- [SQLite의 기여 방식][sqlite-open-not-open-contribution]: 일반적인 외부 PR을 받지 않는 프로젝트의 공식 설명
- [Nobody's job, everybody's problem: F/OSS in the age of AI][hongminhee-foss-ai-talk]: AI 기여가 만드는 신뢰와 리뷰 용량 문제
- [Spring and Security In The Times Of AI][spring-ai-security]: AI 기반 보안 보고의 증가와 검토 과정
- [High-Quality Chaos][curl-high-quality-chaos]: curl의 AI slop 경험과 이후의 변화

{{#include ../_includes/references.md}}

[curl-high-quality-chaos]: https://daniel.haxx.se/blog/2026/04/22/high-quality-chaos/
[richard-hipp-free-puppy]: https://youtu.be/lSVgeMoXJTs?t=923
[rustlings-async-pr]: https://github.com/rust-lang/rustlings/pull/2413
[rustlings-slop-pr]: https://github.com/rust-lang/rustlings/pull/2401
[spring-ai-security]: https://spring.io/blog/2026/06/01/spring_and_security_in_the_times_of_ai/
[spring-unrelated-ai-issue]: https://www.linkedin.com/posts/snicoll_goodbye-albon-idrizi-httpslnkdin-activity-7405253562458378240-Jxu9/
[sqlite-open-not-open-contribution]: https://github.com/sqlite/sqlite#public-domain
