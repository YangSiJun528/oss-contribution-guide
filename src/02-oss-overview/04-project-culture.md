> 아직 작성 중입니다.

# 프로젝트의 방식과 문화

## 프로젝트마다 사용하는 방식과 서비스가 다르다

프로젝트는 코드, 작업, 기여와 소통을 서로 다른 방식으로 관리합니다. 한 서비스만 사용하기도 하고 여러 서비스를 조합하기도 합니다.

| 구분 | 자주 쓰는 방식과 서비스 |
| --- | --- |
| 코드 관리 | GitHub, GitLab, Codeberg, 자체 Git 서버 |
| 기여 제출·검토 | GitHub Pull Request, GitLab Merge Request, Gerrit Change, 메일링 리스트 패치 |
| 작업 관리 | GitHub·GitLab Issue, Jira, Bugzilla, 자체 이슈 추적기 |
| 실시간 소통 | Discord, Slack, Matrix, IRC |
| 논의·결정 기록 | 메일링 리스트, 포럼, GitHub Discussions, Issue, RFC |

예를 들어 코드는 GitHub에서 관리하고, 작업은 Jira에서 추적하며, 질문은 Discord에서 받고, 최종 결정은 Issue나 메일링 리스트에 기록할 수 있습니다.

대표적인 차이는 다음 사례에서 볼 수 있습니다.

- [Fastify][fastify-project]는 코드, Issue, Pull Request와 리뷰를 GitHub에서 관리하고 Discord를 실시간 대화에 사용합니다. 많은 GitHub 기반 프로젝트에서 볼 수 있는 형태입니다.
- [Apache Polaris][apache-polaris-community]는 개발은 GitHub, 실시간 대화는 Slack, 개발 논의는 `dev@` 메일링 리스트에서 진행합니다. [ASF의 원칙][apache-mailing-list-culture]에 따라 채팅에서 시작한 중요한 기술 논의와 결정도 메일링 리스트에 남깁니다.
- [Linux 커널][linux-kernel-submitting-patches]은 `git`으로 패치를 만들지만, 관련 메인테이너와 메일링 리스트에 패치를 본문으로 보내고 이메일에서 리뷰합니다.

이 가이드의 실습 과정은 처음 접하기 쉽고 많은 프로젝트가 사용하는 GitHub의 Issue와 Pull Request만을 다룹니다.

## 문서와 실제 운영 확인하기

기여 절차나 운영 방식은 일반적으로 `README`, `CONTRIBUTING`, `LICENSE`, `SECURITY` 등의 문서에서 관리합니다.

깃헙 레포의 루트에 보면 있는 경우가 많습니다. 혹은 오가니제이션 등에서 공유하는 문서가 있을 수도 있습니다.

주요 파일의 역할은 부록의 [저장소에서 확인할 파일](../07-appendix/06-repository-files.md)에 정리했습니다.


## 더 보기

- [오픈소스에 기여하는 방법][open-source-guide]: 일반적인 프로젝트 구조와 의사소통 방식
- [Producing Open Source Software][producing-open-source-software]: 프로젝트 운영과 커뮤니케이션을 깊게 다루는 무료 영문 도서

{{#include ../_includes/references.md}}

[apache-mailing-list-culture]: https://community.apache.org/contributors/mailing-lists.html
[apache-polaris-community]: https://polaris.apache.org/community/
[fastify-project]: https://github.com/fastify/fastify
[linux-kernel-submitting-patches]: https://www.kernel.org/doc/html/latest/process/submitting-patches.html
