> 아직 작성 중입니다.

# 프로젝트의 AI 정책과 기여자의 책임

LLM 사용 정책은 프로젝트마다 다릅니다.

다만 AI Slop으로 인한 문제를 보완하는 방향으로 정해져있습니다.

대표적으로 3가지 유형이 있는데 프로젝트와 알아봅시다.

## 유형 1: 허용하되 공개와 검증을 요구하는 경우

[Fedify][fedify-ai-policy]는 코드와 글을 만드는 데 AI를 사용하는 것도 허용합니다.

대신 사용한 도구와 범위를 PR과 커밋에 공개하고, 사람이 직접 이해하고 검증해야 합니다. AI로 만든 PR은 먼저 합의된 Issue를 대상으로 해야 한다는 조건도 있습니다.

## 유형 2: 일부 용도만 허용하는 경우

[Rust][rust-llm-policy]는 개인적인 탐색·요약·검토에는 AI를 사용할 수 있지만, 공개 문서와 댓글, 신규 기능 구현과 같은 창작에는 사용을 제한합니다.

일부 코드 생성은 사전 합의, 공개와 검증을 조건으로 허용합니다.

## 유형 3: 사용을 금지하는 경우

[Zig][zig-no-llm-policy]는 공식 저장소와 대화 공간에서 코드·글 생성뿐 아니라 교정, 번역, 브레인스토밍과 버그 탐색에도 LLM을 사용하지 못하게 합니다.

## 기여자의 책임

이 사례가 모든 정책을 대표하지는 않습니다.

실제 기여 전에는 해당 저장소와 참여 공간의 최신 규칙을 확인해야 합니다.

정책이 자신의 생각과 다르더라도 프로젝트에 참여하려면 그 규칙을 따르는 것이 필요합니다.

{{#include ../_includes/references.md}}

[fedify-ai-policy]: https://github.com/fedify-dev/fedify/blob/main/AI_POLICY.md
[rustlings-llm-policy]: https://github.com/rust-lang/rustlings/blob/main/CONTRIBUTING.md#llm-usage-policy
[zig-no-llm-policy]: https://ziglang.org/code-of-conduct/#strict-no-llm-no-ai-policy
