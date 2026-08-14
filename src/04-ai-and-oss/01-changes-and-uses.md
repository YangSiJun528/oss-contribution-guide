> 아직 작성 중입니다.

# AI가 바꾼 OSS 기여

공동체의 규칙을 무시하는 기여는 AI 이전에도 있었습니다. AI는 Issue, 코드와 설명을 만드는 비용을 크게 낮추면서, 프로젝트를 이해하지 않아도 그럴듯한 결과물을 제출하기 쉽게 만들었습니다.

## 공동체의 규칙을 쉽게 건너뛸 수 있게 되었다

기여자는 일반적으로 기존 논의와 기여 절차를 확인하고, 문제를 이해하고 재현하며, 변경을 검증하고 리뷰에 응답해야 합니다.

AI는 이 과정을 실제로 수행하지 않고도 수행한 것처럼 보이는 Issue와 PR을 만들 수 있습니다.

대표적인 문제는 다음과 같습니다.

- 프로젝트와 관계없거나 이미 해결된 문제를 보고합니다.
- 필요성을 논의하지 않은 변경을 대량으로 제출합니다.
- 실행하지 않은 테스트와 존재하지 않는 동작을 설명합니다.
- 생성된 내용을 이해하지 못해 리뷰에 제대로 응답하지 못합니다.

AI 사용 자체보다 이해와 검증에 드는 비용을 공동체에 넘기는 것이 문제입니다. 또한 이러한 기여자(TODO: 기여자와 스패머? 구분하기.)의 경우 올바른 지식 형성을 수행할 수 없으므로 공동체에 참여하지 않고 공동체에게 비용만 부담합니다.

일반적인 내용은 [공동체를 무시하는 기여](../03-contributor-attitude/02-ignoring-the-community.md)에서도 다룹니다.

## AI slop과 검토 비용

이해하거나 검증하지 않은 채 생성해 다른 사람에게 처리 비용을 넘기는 결과물을 흔히 **AI slop**이라고 부릅니다. 모든 AI 활용 결과를 뜻하는 말은 아니며, 어디까지를 slop으로 볼지는 사람과 프로젝트마다 다를 수 있습니다.

실제로 다음과 같은 문제가 발생했습니다.

- Spring 메인테이너가 공유한 [프로젝트와 관계없는 Issue 제출 사례][spring-unrelated-ai-issue]에서는 제출자의 계정이 차단되었습니다.
- [Spring의 보안 보고 회고][spring-ai-security]에 따르면 AI 기반 보고가 급증하면서 실제 취약점과 함께 중복되거나 유효하지 않은 보고도 늘었습니다. 보고마다 메인테이너가 직접 범위와 영향을 확인해야 했습니다.
- Rustlings는 요청하지 않은 AI 생성 연습문제와 불필요한 변경으로 판단한 PR을 별도의 리뷰 없이 닫은 사례가 있습니다. 이후 [LLM 사용 정책][rustlings-llm-policy]을 추가해 생성된 코드의 공개를 요구하고, LLM으로 댓글·Issue·PR 설명을 작성하는 것을 금지했습니다. 실제 처리 사례는 [async/await 연습문제 PR][rustlings-async-pr]과 [불필요한 변경으로 판단한 PR][rustlings-slop-pr]에서 볼 수 있습니다.
- curl은 저품질 보안 보고가 급증하자 2026년 2월 버그 바운티를 중단했습니다. 이후 접수 방식을 바꾸어 다시 열었지만, 보고량 증가가 만드는 메인테이너 부담은 계속되고 있습니다. 자세한 경과는 [High-Quality Chaos][curl-high-quality-chaos]에서 볼 수 있습니다.

## 그럼에도 AI는 유용하다

AI는 실제 문제를 탐색하고, 반복적인 변환을 수행하고, 기존 테스트를 기준으로 큰 작업을 검증하는 데 유용하게 쓰일 수 있습니다.

중요한 차이는 사람이 목적과 방향을 정하고 결과를 직접 검증하며 이후의 유지보수를 감당할 수 있는가입니다.

> 여기선 기여자의 입장에서의 사례를 따로 언급하진 않겠는데요. 기여자들의 사용 범위를 명확하게 파악하기가 어렵기 때문입니다.
> AI를 사용해보셨다면 잘 사용한다면 유용하게 사용할 수 있다는데에는 어느정도 동의하실 거라고 생각합니다.
>
> 그 외에 여담으로 zig의 리라이트나 구글의 버그 바운티를 찾는 ai가 잘 수행해내는 작업으로 대규모 작업을 한 경우가 있지만, 이는 기본적으로 기여자가 하기는 어려운 작업의 범위입니다.

## 프로젝트는 함께하기 위한 규칙을 만든다

프로젝트는 AI를 무조건 허용하거나 금지하는 대신, 공동체가 감당할 수 있는 범위를 정하기도 합니다. 사용 사실 공개, 사전 합의, 사람의 직접 검증, 허용·금지 영역과 같은 규칙을 추가하는 방식입니다.

이러한 규칙이 실제로 어떻게 다른지는 다음 글인 [프로젝트의 AI 정책과 기여자의 책임](02-policies-and-responsibility.md)에서 다룹니다.

## 더 보기

- [Nobody's job, everybody's problem: F/OSS in the age of AI][hongminhee-foss-ai-talk]: AI 기여가 만드는 신뢰와 리뷰 용량 문제
- [Spring and Security In The Times Of AI][spring-ai-security]: AI 기반 보안 보고의 증가와 검토 과정
- [High-Quality Chaos][curl-high-quality-chaos]: curl의 AI slop 경험과 이후의 변화

{{#include ../_includes/references.md}}

[curl-high-quality-chaos]: https://daniel.haxx.se/blog/2026/04/22/high-quality-chaos/
[rustlings-async-pr]: https://github.com/rust-lang/rustlings/pull/2413
[rustlings-llm-policy]: https://github.com/rust-lang/rustlings/blob/main/CONTRIBUTING.md#llm-usage-policy
[rustlings-slop-pr]: https://github.com/rust-lang/rustlings/pull/2401
[spring-ai-security]: https://spring.io/blog/2026/06/01/spring_and_security_in_the_times_of_ai/
[spring-unrelated-ai-issue]: https://www.linkedin.com/posts/snicoll_goodbye-albon-idrizi-httpslnkdin-activity-7405253562458378240-Jxu9/
