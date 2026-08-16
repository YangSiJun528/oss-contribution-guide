# 프로젝트의 구성과 운영 방식

OSS 프로젝트마다 다루는 작업의 범위와 참여자의 구성이 다릅니다.

개인이 관리하는 작은 라이브러리부터 여러 조직과 수많은 참여자가 함께 개발하는 프로젝트까지 규모와 형태도 다양합니다.

이에 따라 역할/의사결정/작업 절차 등도 프로젝트마다 다양합니다. OSS 프로젝트에서 볼 수 있는 주요 구성과 운영 방식을 살펴봅시다.

## 운영 주체와 구조

### 다양한 운영 주체

프로젝트는 개인이나 소규모 팀이 관리할 수도 있고, 기업이 개발 인력과 비용을 지원할 수도 있으며, Apache Software Foundation이나 Linux Foundation/CNCF 같은 비영리 생태계 안에서 운영될 수도 있습니다.

코드 저장소의 소유자, 저작권자, 비용을 대는 조직, 기술적 결정을 내리는 사람이 서로 다를 수도 있습니다.

### 참여자의 역할과 권한

프로젝트의 역할은 정해진 표준이 아닙니다. 프로젝트에서 사용하는 기술, 공동체의 필요와 운영 방식에 따라 필요한 역할과 권한이 달라집니다. 아래 역할이 모두 존재하지 않을 수도 있고, 한 사람이 여러 역할을 함께 맡을 수도 있습니다.

『오픈 소스로 미래를 연마하라』에서 소개한 양파 모형을 기준으로 FOSS 프로젝트에서 흔히 볼 수 있는 역할을 정리하면 다음과 같습니다.

- **사용자**: 프로젝트를 실제로 사용하는 사람입니다. 가장 바깥에 있지만 프로젝트가 존재하는 이유가 되는 중요한 참여자입니다.
- **신입 기여자(New Contributor)**: 첫 기여를 준비하거나 진행하면서 프로젝트의 절차, 도구와 문화를 익히는 참여자입니다.
- **기여자(Contributor)**: 코드, 문서, 테스트, 번역, 디자인이나 문제 분석을 지속적으로 제안하고 토론에 참여합니다.
- **핵심 기여자(Core Contributor)**: 프로젝트 경험과 신뢰가 쌓인 기여자입니다. 프로젝트에 따라 주 저장소에 변경을 병합할 권한인 커밋 비트(commit bit)를 가지며, 커미터(Committer), 메인테이너(Maintainer), 리뷰어(Reviewer), 승인자(Approver) 등으로 불립니다.
- **창시자·BDFL·리더십**: 프로젝트 전체의 방향과 주요 결정을 책임지는 중심 역할입니다.

<figure>
  <img src="../assets/oss-overview/forge-your-future-community-onion-model.png" width="500" loading="lazy">
  <figcaption>FOSS 커뮤니티의 일반적인 역할을 표현한 양파 모형. VM 브라수어, 『오픈 소스로 미래를 연마하라』, 41쪽에서 인용. 한국어판 © 2019 인사이트.</figcaption>
</figure>

양파의 중심에 가까울수록 지속적인 활동, 신뢰, 권한과 책임이 커집니다. 그러나 이 모형이 모든 프로젝트가 따라야 하는 서열이나 승급 순서를 뜻하지는 않습니다. 바깥의 사용자도 프로젝트의 필요와 방향을 확인하게 하는 필수적인 역할입니다.

구체적인 역할의 이름과 권한도 프로젝트마다 다릅니다. 예를 들어 [Kubernetes][kubernetes-roles-and-responsibilities]는 기여자·멤버·리뷰어·승인자를, [Apache Software Foundation][apache-how-it-works]은 커미터와 PMC를 구분합니다.

## 의사결정 방식

프로젝트의 리더십을 반드시 창시자가 계속 맡는 것은 아닙니다. 창시자가 다른 참여자에게 권한을 넘기기도 하고, 한 사람 대신 여러 사람이 책임을 나누기도 합니다.

대표적인 의사결정 방식은 다음과 같습니다. 실제 프로젝트는 여러 방식을 함께 사용할 수 있습니다.

- **개인·BDFL 중심**: 창시자나 소수의 메인테이너가 최종 결정을 내립니다. BDFL(Benevolent Dictator for Life, 자비로운 종신 독재자)은 최종 결정권과 거부권을 가진 개인 리더를 뜻합니다.
- **메인테이너 합의**: 여러 메인테이너가 리뷰와 공개 토론을 거쳐 방향을 정합니다.
- **위원회 중심**: PMC, Technical Steering Committee 같은 조직이 정해진 투표와 승인 절차를 사용합니다.
- **기업 주도**: 특정 기업의 직원이 핵심 개발과 로드맵을 주도하면서 외부 기여자와 협업합니다.

최종 결정권자가 분명한 프로젝트에서도 모든 결정을 일방적으로 내리기보다 토론과 검토를 통해 합의를 만들 수 있습니다. 어느 방식이 항상 더 낫다고 할 수는 없습니다. 기여자에게 중요한 것은 의견을 어디에 제안하고 어떤 절차를 거쳐 누가 최종 결정을 내리는지 알 수 있는가입니다.

## 협업 방식

### 작업과 소통 경로

각 역할은 실제 작업과 소통 과정에서 서로 연결됩니다. 사용자는 피드백, 버그 보고와 기능 아이디어를 전하고, 기여자는 결과물을 제안하거나 다른 사람의 변경을 검토합니다. 경험이 쌓인 기여자는 신입 기여자에게 조언하고, 핵심 기여자는 변경을 병합하고 저장소와 릴리스를 관리합니다.

신입 기여자가 절차와 문화를 익히고 정착할 수 있도록 안내와 피드백을 제공하는지는 프로젝트의 협업 환경을 판단하는 기준이 될 수 있습니다.

이러한 협업에는 코드 관리, 작업 조율, 의사소통과 문서화가 필요합니다. 작은 프로젝트는 이 모든 일을 한 공간에서 처리할 수 있지만, 규모가 커지면 목적에 따라 여러 협업 경로를 나누기도 합니다.

| 구분 | 자주 쓰는 방식과 서비스 |
| --- | --- |
| 코드 관리 | GitHub, GitLab, Codeberg, 자체 Git 서버 |
| 기여 제출·검토 | GitHub Pull Request, GitLab Merge Request, Gerrit Change, 메일링 리스트 패치 |
| 작업 관리 | GitHub·GitLab Issue, Jira, Bugzilla, 자체 이슈 추적기 |
| 실시간 소통 | Discord, Slack, Matrix, IRC |
| 논의·결정 기록 | 메일링 리스트, 포럼, GitHub Discussions, Issue, RFC |

### 프로젝트별 사례

예시:
- [Fastify][fastify-project]는 GitHub에서 코드/이슈/PR/리뷰 등을 Discord를 실시간 대화에 사용합니다.
- [Apache Polaris][apache-polaris-community]는 개발은 GitHub, 실시간 대화는 Slack, 개발 논의는 `dev@` 메일링 리스트에서 진행합니다.
  - 추가적인 정보로, Apache 재단의 프로젝트들은 모두 [ASF의 원칙][apache-mailing-list-culture]에 중요한 기술 논의와 결정을 메일링 리스트에 기록합니다.
  - 이처럼 조직/재단/단체에서 공유되는 규칙이 있기도 합니다.
- [Linux 커널][linux-kernel-submitting-patches]은 `git`으로 패치를 만들지만, 관련 Maintainer와 메일링 리스트에 패치를 본문으로 보내고 이메일에서 리뷰합니다.
  - github을 사용하지 않는 대표적인 서비스입니다! TMI로 리눅스는 깃이나 깃헙보다 더 빨리 만들어졌습니다.

## 참고 자료

- [오픈소스 프로젝트의 해부학][open-source-guide-project-anatomy]: 일반적인 역할, 프로젝트 구조와 참여 방법
- [오픈소스에 기여하는 방법][open-source-guide]: 일반적인 프로젝트 구조와 의사소통 방식
- [Producing Open Source Software][producing-open-source-software]: 프로젝트 운영과 커뮤니케이션을 깊게 다루는 무료 영문 도서
- 『오픈 소스로 미래를 연마하라』(VM 브라수어), 3장과 6장: 프로젝트 공동체의 역할과 코드 이외의 기여

{{#include ../_includes/references.md}}

[apache-mailing-list-culture]: https://community.apache.org/contributors/mailing-lists.html
[apache-polaris-community]: https://polaris.apache.org/community/
[fastify-project]: https://github.com/fastify/fastify
[kubernetes-roles-and-responsibilities]: https://kubernetes.io/docs/contribute/participate/roles-and-responsibilities/
[linux-kernel-submitting-patches]: https://www.kernel.org/doc/html/latest/process/submitting-patches.html
