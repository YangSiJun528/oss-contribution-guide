> 아직 작성 중입니다.

# 프로젝트를 구성하는 사람과 조직

## 역할명보다 실제 권한을 확인한다

OSS 프로젝트에는 코드를 쓰는 사람만 있는 것이 아닙니다. 흔히 다음과 같은 역할이 함께 프로젝트를 만듭니다.

- **사용자**: 프로젝트를 사용하고, 문제를 보고하거나 다른 사용자를 돕습니다.
- **기여자(Contributor)**: 코드, 문서, 테스트, 디자인이나 문제 분석을 제안합니다. 한 번만 참여해도 기여자입니다.
- **리뷰어(Reviewer)**: 제안된 변경의 정확성, 범위와 품질을 검토하고 피드백합니다.
- **커미터(Committer)·메인테이너(Maintainer)**: 변경을 병합하고, 저장소·릴리스·이슈를 지속적으로 관리합니다.
- **오너(Owner)·승인자(Approver)·PMC**: 특정 영역이나 프로젝트 전체의 기술적·운영적 결정을 책임집니다.

<figure>
  <img src="../assets/oss-overview/project-roles.svg" width="960" loading="lazy">
  <figcaption>책임과 권한이 넓어지는 흔한 흐름입니다. 모든 사람이 이 순서를 거치는 것은 아니며 실제 역할과 이름은 프로젝트마다 다릅니다.</figcaption>
</figure>

`member`, `committer`, `owner`, `approver`, `PMC` 같은 이름은 프로젝트마다 뜻이 다릅니다. 어떤 프로젝트에서는 저장소 쓰기 권한을 뜻하고, 다른 프로젝트에서는 투표권이나 릴리스 승인 권한까지 포함합니다. GitHub 조직에 속해 있다는 사실만으로 프로젝트의 모든 결정을 내릴 수 있는 것도 아닙니다.

예를 들어 [Kubernetes][kubernetes-roles-and-responsibilities]는 기여자, 멤버, 리뷰어, 승인자의 역할과 권한을 나눕니다. [Apache Software Foundation][apache-how-it-works]의 프로젝트에서는 커미터와 PMC가 구분되며, PMC가 릴리스와 프로젝트 운영을 책임집니다. 이런 역할은 일반적인 승진 단계라기보다 해당 공동체가 책임과 권한을 나누는 방식입니다.

## 운영 주체도 다양하다

프로젝트는 개인이나 소규모 팀이 관리할 수도 있고, 기업이 개발 인력과 비용을 지원할 수도 있으며, Apache Software Foundation이나 Linux Foundation/CNCF 같은 비영리 생태계 안에서 운영될 수도 있습니다. 코드 저장소의 소유자, 저작권자, 비용을 대는 조직, 기술적 결정을 내리는 사람이 서로 다를 수도 있습니다.

따라서 프로젝트의 규모나 유명세만 보고 구조를 추측하지 말고, 거버넌스 문서와 `MAINTAINERS`, `OWNERS`, 최근 릴리스와 의사결정 기록을 확인해야 합니다.

## 더 보기

- [오픈소스 프로젝트의 해부학][open-source-guide-project-anatomy]: 일반적인 역할과 프로젝트 구조

{{#include ../_includes/references.md}}
