> 아직 작성 중입니다.

# 라이선스

## 라이선스가 하는 일

코드는 작성되는 순간 저작권의 보호를 받습니다. OSS 라이선스는 다른 사람이 코드를 사용·수정·배포할 수 있는 조건을 정합니다. 공개 저장소에 `LICENSE`가 없다면 코드를 볼 수 있어도 사용할 권리가 생기지는 않습니다.

<figure>
  <img src="../assets/oss-overview/license-landscape.svg" width="960" loading="lazy">
  <figcaption>자주 접하는 소프트웨어 라이선스의 범위입니다.</figcaption>
</figure>

## 자주 접하는 OSS 라이선스

| 범위 | 대표적인 라이선스 | 대략적인 특징 |
| --- | --- | --- |
| 허용적 라이선스 | MIT, BSD-2-Clause, BSD-3-Clause, ISC, Zlib | 고지 유지 등 비교적 적은 조건으로 재사용을 허용합니다. |
| 특허 조항이 있는 허용적 라이선스 | Apache-2.0 | 허용적 조건과 명시적인 특허권 허여를 포함합니다. |
| 제한된 범위의 카피레프트 | LGPL-2.1/3.0, MPL-2.0, EPL-2.0, CDDL-1.0 | 라이브러리·파일 등 정해진 범위에 소스 공개 조건을 적용합니다. |
| 강한 카피레프트 | GPL-2.0/3.0 | 파생 저작물 배포 시 같은 라이선스와 소스 제공을 요구할 수 있습니다. |
| 네트워크 카피레프트 | AGPL-3.0 | 수정본을 네트워크 서비스로 제공할 때도 소스 제공을 요구할 수 있습니다. |

구체적인 의무는 버전, 예외, 코드 결합 방식과 배포 여부에 따라 달라지므로 원문을 확인해야 합니다.

## 한 프로젝트에 라이선스가 여러 개 있을 때

한 저장소에도 여러 라이선스가 적용될 수 있습니다.

SPDX(Software Package Data Exchange)는 라이선스 정보를 표준 형식으로 표시하는 규격입니다. `OR`는 선택, `AND`는 동시 적용, `WITH`는 예외 조항을 뜻합니다.

- **선택**: [Rust][rust-license]의 `MIT OR Apache-2.0`처럼 하나를 선택합니다.
- **동시 적용**: 결합된 코드의 여러 조건을 함께 지킵니다.
- **파일·모듈별 적용**: 코드, 문서, 이미지와 외부 구성요소가 서로 다른 라이선스를 따릅니다.
- **상용·OSS 이중 제공**: [Qt][qt-licensing]처럼 상용 라이선스와 LGPL/GPL 선택지를 함께 제공합니다.

`LICENSE`, `COPYRIGHT`, `NOTICE`, 파일의 SPDX 표시, 하위 디렉터리, 의존성과 SBOM을 함께 확인합니다. [Qt의 외부 구성요소 목록][qt-third-party-licenses]처럼 별도 목록이 있을 수도 있습니다.

## 자체 라이선스와 소스 공개형 라이선스

소스가 공개되었다는 넓은 의미에서 이런 소프트웨어를 오픈소스나 제한된 오픈소스라고 부르기도 합니다.

다만 용도나 서비스 제공을 제한하면 OSI의 오픈소스 정의를 충족하지 않습니다. 이 가이드에서는 이를 OSS가 아닌 `source-available`로 구분합니다.

- [Business Source License 1.1][mariadb-bsl-11]: 사용 제한과 변경 날짜를 두고 이후 OSS 라이선스로 전환합니다.
- [MongoDB의 SSPL][mongodb-sspl]: 서비스 제공에 추가 조건을 둡니다. [OSI는 OSS 라이선스로 인정하지 않습니다][osi-sspl-not-open-source].
- [Elastic License 2.0][elastic-license-2]: 관리형 서비스 제공 등을 제한합니다.

## 기여 코드의 라이선스

- `CONTRIBUTING`과 라이선스 정책을 확인합니다. 기여한 코드는 일반적으로 프로젝트의 라이선스로 배포됩니다.
- 제출할 권리가 없는 회사 코드나 다른 프로젝트의 코드를 포함하지 않습니다.

별도 약정이 없다면 기여자는 자신이 작성한 코드의 저작권을 유지합니다.

## CLA와 DCO

기여를 위해서 특정 동의가 필요한 경우가 있습니다. 대표적으로 다음이 있습니다.

- CLA(Contributor License Agreement)는 추가 권한이나 저작권 양도를 요구할 수 있습니다.
- DCO(Developer Certificate of Origin)는 코드를 제출할 권리가 있음을 확인하며 저작권을 양도하지는 않습니다.

저작권 양도와 관련해서 회사에서 일하는 경우 문제가 될 수 있으므로 [기여를 시작하기 전에](../01-introduction/02-before-you-contribute.md#회사에-다니고-있다면)를 참고해주세요.

## 더 보기

- [라이선스가 없는 코드][choosealicense-no-permission]: 공개 저장소에 라이선스가 없을 때의 기본적인 취급
- [OSI 승인 라이선스 목록][osi-approved-licenses]: 특정 라이선스가 OSI 승인을 받은 오픈소스 라이선스인지 확인하는 목록
- [SPDX 라이선스 표현식][spdx-license-expressions]: 여러 라이선스의 선택·동시 적용·예외를 표현하는 표준
- [MPL 2.0 FAQ][mozilla-mpl-faq]: 파일 단위 카피레프트와 배포 조건을 설명하는 공식 자료
- [Developer Certificate of Origin][dco]: 프로젝트에서 DCO 서명을 요구할 때 확인할 원문

{{#include ../_includes/references.md}}

[choosealicense-no-permission]: https://choosealicense.com/ko/no-permission/
[elastic-license-2]: https://www.elastic.co/licensing/elastic-license/faq/
[mariadb-bsl-11]: https://mariadb.com/bsl11/
[mongodb-sspl]: https://www.mongodb.com/legal/licensing/server-side-public-license
[mozilla-mpl-faq]: https://www.mozilla.org/en-US/MPL/2.0/FAQ/
[osi-sspl-not-open-source]: https://opensource.org/blog/the-sspl-is-not-an-open-source-license
[qt-licensing]: https://doc.qt.io/qt-6/licensing.html
[qt-third-party-licenses]: https://doc.qt.io/qt-6/licenses-used-in-qt.html
[rust-license]: https://github.com/rust-lang/rust#license
[spdx-license-expressions]: https://spdx.github.io/spdx-spec/v2.3/SPDX-license-expressions/
