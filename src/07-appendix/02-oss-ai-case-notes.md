> 아직 작성 중입니다.

# OSS와 AI 사례 노트

- AI가 바꾼 개발 비용
  - 정확히는 Bun의 Zig → Rust 재작성 사례
  - [실제 PR][bun-zig-to-rust-pr]과 [Anthropic 설명][anthropic-ai-code-migration]을 같이 연결
- 프로젝트의 AI 규칙
  - [Rust의 LLM 정책][rust-llm-policy]
  - Zig·Servo 등 금지 또는 제한 사례
- AI slop과 메인테이너 비용
  - Issue·PR·취약점 보고 생성 비용과 검토 비용의 비대칭
  - curl, Node.js, OpenSSF 사례
- 오픈소스 AI의 경계
  - 표현은 “오픈웨이트만으로는 오픈소스 AI가 아니다”가 정확함
  - [OSI의 Open Source AI Definition][osi-open-source-ai-definition] 연결
  - 기억한 Node 메인테이너 글은 확인되지 않았고, 유력한 글은 NixOS 관계자가 쓴 [Open weights are not open source][open-weights-not-open-source]임
- 출처·계보·재구현 문제
  - 말한 용어가 아마 `클린룸 재구현(clean-room reimplementation)`일 가능성이 있음
  - 출처 세탁, 라이선스 세탁, 원본을 모르는 AI 생성물 문제
  - 블루리본 사례는 정확한 링크 확인 후 추가
- AI 보안 연구의 양면성
  - 무효 취약점 보고와 실제 유효한 발견을 함께 제시
  - “AI 사용 여부”보다 재현·검증·전달 품질을 중심으로 정리
- 스타와 관심 지표의 왜곡
  - 설치 과정에서 스타를 요청하는 방식
  - 스타 구매·봇·가짜 계정
  - 둘은 구분해야 함. OMC에서 확인되는 것은 [명시적 동의 후 스타 API를 실행하는 제안][omc-star-api-issue]이지, 스타 구매 증거는 아님

{{#include ../_includes/references.md}}
