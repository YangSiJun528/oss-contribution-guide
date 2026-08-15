> 아직 작성 중입니다.

# PR 작성과 리뷰 대응

> **공개 가이드 요약**
>
> 좋은 PR을 작성하는 자세한 방법은 [Google Engineering Practices][google-engineering-practices]와 [GitHub의 리뷰하기 쉬운 변경 작성법][github-helping-others-review]을 참고합니다.
> 핵심은 변경을 한 가지 목적에 집중해 작게 유지하고, 변경 이유와 검증 결과를 명확히 적은 뒤, 제출 전에 전체 diff를 직접 검토하는 것입니다. 프로젝트의 자체 규칙과 템플릿이 있다면 이를 우선합니다.

PR을 생성했다는 것과 Maintainer가 검토할 수 있는 PR을 제출했다는 것은 다릅니다. 검토자는 변경된 코드뿐 아니라 변경 이유와 검증 근거를 함께 확인할 수 있어야 합니다.

## 검토 가능한 PR 작성

별도 형식이 없다면 다음 내용을 간결하게 적습니다.

- 어떤 문제가 있고 왜 변경이 필요한가?
- 어떤 방법으로 해결했으며, 다른 변경까지 포함하지는 않았는가?
- 어떤 테스트와 검증을 실행했고 결과는 어땠는가?
- 알려진 한계나 확인하지 못한 내용이 있는가?
- 어떤 Issue와 관련되어 있는가?

Commit 메시지와 단위도 변경 의도를 드러내도록 정리하고, 공개할 의도가 없는 이메일이나 개인정보가 Commit에 포함되지 않았는지 확인합니다.

아직 방향이나 구현에 대한 피드백이 필요하다면 Draft PR을 사용할 수 있습니다.

## 리뷰 대응

- 리뷰 요청을 정확히 이해합니다.
- 요청이 모호하면 자신이 이해한 내용을 되물어 확인합니다.
- 동의하지 않는다면 기술적 근거와 가능한 대안을 제시합니다.
- 수정한 뒤 무엇을 바꾸고 어떻게 검증했는지 설명합니다.
- AI가 생성한 답변을 검토 없이 게시하지 않습니다.

리뷰는 제출한 변경을 함께 판단하는 과정입니다. 모든 요청에 무조건 동의할 필요는 없지만, 자신의 판단을 코드와 테스트, 프로젝트의 목표에 근거해 설명해야 합니다.

PR의 병합·거절·무응답과 제출 이후의 소통은 [PR 제출 이후](../05-after-first-contribution/01-after-submission.md)에서 다룹니다.

[google-engineering-practices]: https://google.github.io/eng-practices/
[github-helping-others-review]: https://docs.github.com/en/pull-requests/concepts/helping-others-review-your-changes
