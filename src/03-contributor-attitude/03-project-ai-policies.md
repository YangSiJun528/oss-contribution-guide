> 아직 작성 중입니다.

# 프로젝트별 AI 사용 규칙

AI를 받아들이는 범위는 프로젝트마다 다릅니다.

이 글에서는 대표적인 정책을 다음 네 가지 유형으로 나눕니다.

> 이 구분은 작성자의 개인적인 기준입니다.

## AI 생성 기여 허용

AI로 만든 코드나 글도 기여로 받지만, 기여자가 내용을 이해하고 검증하며 결과에 책임지도록 요구합니다. 프로젝트에 따라 AI 사용 사실이나 사용한 도구를 밝히도록 하기도 합니다.

예: [CPython][cpython-ai-policy], [Linux 커널][linux-ai-policy], [Fedify][fedify-ai-policy]

## AI 생성 기여의 제한적 허용

결과물의 종류나 생성 방식에 따라 일부 기여만 받습니다.

예: [Rust][rust-llm-policy]

## AI 생성 기여 비허용

개인적인 조사나 코드 이해에는 AI를 사용할 수 있지만, AI 생성물이 포함된 기여는 받지 않습니다.

예: [OpenJDK][openjdk-ai-policy], [QEMU][qemu-ai-policy]

## 공식 기여 과정의 AI 사용 금지

개인적인 사용까지 제한하지는 않지만, AI로 만든 결과나 AI로 찾은 버그를 프로젝트의 공식 공간에 공유할 수 없습니다.

예: [Zig][zig-no-llm-policy]

{{#include ../_includes/references.md}}

[cpython-ai-policy]: https://devguide.python.org/getting-started/generative-ai/
[fedify-ai-policy]: https://github.com/fedify-dev/fedify/blob/main/AI_POLICY.md
[linux-ai-policy]: https://docs.kernel.org/process/coding-assistants.html
[openjdk-ai-policy]: https://openjdk.org/legal/ai
[qemu-ai-policy]: https://www.qemu.org/docs/master/devel/code-provenance.html#use-of-ai-generated-content
[zig-no-llm-policy]: https://ziglang.org/code-of-conduct/#strict-no-llm-no-ai-policy
