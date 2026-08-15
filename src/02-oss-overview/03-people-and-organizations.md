> 아직 작성 중입니다.

# 프로젝트를 구성하는 사람과 조직

## 역할명과 실제 권한

OSS 프로젝트에는 다양한 역할의 사람들이 프로젝트를 구성합니다.

- **사용자**: 프로젝트를 사용하고, 문제를 보고하거나 다른 사용자를 돕습니다.
- **신입 기여자(New Contributor)**: 프로젝트의 절차와 문화를 배우며 첫 기여를 준비하거나 진행합니다.
- **기여자(Contributor)**: 코드, 문서, 테스트, 디자인이나 문제 분석을 제안합니다. 한 번만 참여해도 기여자입니다.
- **커미터(Committer)·메인테이너(Maintainer)**: 변경을 피드백하고 병합하고, 저장소·릴리스·이슈를 지속적으로 관리합니다.
- **오너(Owner)·승인자(Approver)·PMC**: 특정 영역이나 프로젝트 전체의 기술적·운영적 결정을 책임집니다.

<figure>
  <img src="../assets/oss-overview/forge-your-future-community-onion-model.png" width="500" loading="lazy">
  <figcaption>FOSS 커뮤니티의 일반적인 역할을 표현한 양파 모형. VM 브라수어, 『오픈 소스로 미래를 연마하라』, 41쪽에서 인용. 한국어판 © 2019 인사이트.</figcaption>
</figure>

여러 사람이 한 가지의 역할을 맡아 책임을 나눕니다. 경우에 따라 (특히 규모가 작은 경우라면) 한 사람이 여러 역할을 맡을 때도 있습니다.

중심에 가까울수록 활동과 책임이 커지지만 서열이 존재하는 것은 아닙니다. 모든 역할이 있어야만 오픈소스가 존재할 수 있습니다.

구체적인 역할의 이름과 권한은 프로젝트마다 다릅니다. [Kubernetes][kubernetes-roles-and-responsibilities]는 기여자·멤버·리뷰어·승인자를, [Apache Software Foundation][apache-how-it-works]은 커미터와 PMC를 구분합니다.

## 다양한 의사결정 방식

대표적인 방식은 다음과 같습니다. 실제 프로젝트는 여러 방식을 함께 사용할 수 있습니다.

- **개인·창시자 중심**: 한 사람이나 소수의 메인테이너가 최종 결정을 내립니다.
- **메인테이너 합의**: 여러 메인테이너가 리뷰와 공개 토론을 거쳐 방향을 정합니다.
- **위원회 중심**: PMC, Technical Steering Committee 같은 조직이 정해진 투표와 승인 절차를 사용합니다.
- **기업 주도**: 특정 기업의 직원이 핵심 개발과 로드맵을 주도하면서 외부 기여자와 협업합니다.

추가) 개인 리더에게 최종 결정권이 있으면 BDFL(Benevolent Dictator for Life, 자비로운 종신 독재자)이라고 부르기도 합니다.

어느 방식이 항상 더 낫다고 할 수는 없습니다. 기여자에게 중요한 것은 의견을 어디에 제안하고 누가 최종 결정을 내리는지 알 수 있는가입니다.

## 다양한 운영 주체

프로젝트는 개인이나 소규모 팀이 관리할 수도 있고, 기업이 개발 인력과 비용을 지원할 수도 있으며, Apache Software Foundation이나 Linux Foundation/CNCF 같은 비영리 생태계 안에서 운영될 수도 있습니다.

코드 저장소의 소유자, 저작권자, 비용을 대는 조직, 기술적 결정을 내리는 사람이 서로 다를 수도 있습니다.

확실하게 파악하기 위해서는 거버넌스 문서와 `MAINTAINERS`, `OWNERS`, 최근 릴리스와 의사결정 기록을 확인해야 합니다.

## 참고 자료

- [오픈소스 프로젝트의 해부학][open-source-guide-project-anatomy]: 일반적인 역할과 프로젝트 구조
- 『오픈 소스로 미래를 연마하라』(VM 브라수어), 3장: 프로젝트와 커뮤니티의 일반적인 역할을 양파 모형으로 설명

{{#include ../_includes/references.md}}

[kubernetes-roles-and-responsibilities]: https://kubernetes.io/docs/contribute/participate/roles-and-responsibilities/
