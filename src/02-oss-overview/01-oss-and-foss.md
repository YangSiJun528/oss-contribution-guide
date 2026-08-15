> 아직 작성 중입니다.

# OSS와 FOSS

## 라이선스와 사용 허가

글, 그림과 코드는 공개되어 있어도 마음대로 복사하거나 수정할 수 없습니다. 권리자가 이용을 허락한 조건인 **라이선스**를 따라야 합니다.

라이선스는 여러 산업에서 사용하며, 대상과 이용 방식에 따라 다양하게 존재합니다. 다음은 몇 가지 예시입니다.

- 소프트웨어: MIT, Apache, GPL
- 사진·문서·교육 콘텐츠: Creative Commons
- 제조·통신·제약: 특허 라이선스와 FRAND
- 글꼴·데이터·하드웨어: 각 분야의 전용 오픈 라이선스

## 소프트웨어와 소프트웨어 라이선스

소프트웨어도 전용 라이선스를 가지고 있습니다. 이는 소프트웨어의 특성 때문인데요.

소스 코드와 바이너리가 따로 유통되고 다른 코드와 결합되거나 수정될 수 있어, 소스 공개 범위, 라이선스 호환성, 보증과 책임 등을 다룰 필요가 있기 때문입니다.

## 소스 공개와 OSS의 차이

OSI(Open Source Initiative)의 [Open Source Definition][osi-open-source-definition]에 따르면 OSS는 소스 열람뿐 아니라 사용·수정·재배포를 허용해야 하며, 특정 개인·집단이나 용도를 차별적으로 제한해서는 안 됩니다.

소스를 공개해도 상업적 사용, 수정 또는 재배포를 제한한다면 보통 `source-available`이라고 부르고 OSS가 아닙니다.

## OSS와 공개적 프로젝트 운영의 구분

OSS라는 분류는 소프트웨어를 사용할 수 있는 권리에 관한 것입니다. 외부인이 개발 과정에 참여할 수 있어야 한다거나 모든 의사결정을 공개해야 한다는 뜻은 아닙니다. 기업이나 소수의 메인테이너가 로드맵을 결정하고 외부 PR을 거의 받지 않더라도, 소프트웨어가 OSS 라이선스로 배포된다면 OSS일 수 있습니다.

ClickHouse의 Alexey Milovidov가 제안한 [오픈소스 개발 개방성 수준 분류][clickhouse-openness-levels]는 개발 과정에 외부인이 얼마나 참여할 수 있는지를 설명합니다. 이것들 모두 넓은 의미에서 오픈소스라고 볼 수 있습니다. (공신력 있는 기준은 아니지만 구분이 잘 되어 있어 가져왔습니다.)


- **0단계:** 코드는 읽을 수 있게 공개하지만 더 이상의 개발을 기대하지 않는 보존·기록 단계. Doom과 MS-DOS가 예입니다.
- **1단계:** 공개 저장소에서 계속 개발하지만 외부 기여를 반드시 받지는 않는 단계. SQLite와 Ladybird가 예입니다.
- **2단계:** 외부 기여는 받지만 개발 과정과 의사결정이 충분히 공개되지는 않은 단계. 다수의 활발한 OSS 프로젝트가 여기에 속합니다.
- **3단계:** 기여 지침, 작업 추적, 코드 리뷰, 로드맵, CI, 릴리스와 지원 과정까지 공개한 단계. ClickHouse나 Kubernetes 같은 프로젝트가 예입니다.

반대로 공개 저장소에서 Issue와 PR을 받더라도 사용·수정·재배포를 제한하는 라이선스를 사용한다면 일반적인 의미의 OSS는 아닙니다.

## OSS와 FOSS

FOSS(Free and Open Source Software)는 자유 소프트웨어와 오픈소스 소프트웨어를 함께 부르는 표현입니다. 여기서 `free`는 무료가 아니라 자유를 뜻합니다.

두 개념이 가리키는 소프트웨어는 대부분 겹치지만 강조점이 다릅니다.

- 자유 소프트웨어: 사용자가 실행·연구·수정·공유할 자유를 윤리적 가치
- 오픈소스 소프트웨어: 공개된 소스와 라이선스를 통한 협업과 실용성

이 가이드에서는 구분이 필요한 경우가 아니면 OSS를 기본 용어로 사용합니다.
다만 기여 시에 프로젝트가 특정 표현을 사용할 수 있습니다. 이 경우 프로젝트에서 강조하려는 가치가 담길 수 있으므로 해당 커뮤니티의 용어를 존중해주세요.

## 참고 자료

- [Open Source Definition][osi-open-source-definition]: 소스 공개를 넘어 OSS 라이선스가 충족해야 할 기준
- [자유 소프트웨어의 정의][fsf-free-software-definition-ko]: FOSS에서 말하는 자유의 의미
- [네이버 오픈소스 가이드][naver-open-source-guide]: OSS, 라이선스, 기여 절차를 폭넓게 다루는 한국어 자료. 오래된 화면과 절차는 최신 공식 문서에서 다시 확인

{{#include ../_includes/references.md}}

[cc-by-4]: https://creativecommons.org/licenses/by/4.0/deed.ko
[cc-software-faq]: https://creativecommons.org/faq/#can-i-apply-a-creative-commons-license-to-software
[clickhouse-openness-levels]: https://clickhouse.com/blog/open-source-10
