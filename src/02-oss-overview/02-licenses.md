> 아직 작성 중입니다.

# 라이선스

## 라이선스의 역할

코드는 작성되는 순간 저작권의 보호를 받습니다. OSS 라이선스는 저작권자가 다른 사람에게 코드를 사용·수정·배포할 권리를 어떤 조건으로 허용하는지 정합니다. 소스가 공개되어 있다는 사실만으로 이러한 권리가 생기지는 않습니다.

<figure>
  <img src="../assets/oss-overview/license-landscape.svg" width="960" loading="lazy">
  <figcaption>자주 접하는 소프트웨어 라이선스의 범위입니다.</figcaption>
</figure>

## 주요 OSS 라이선스

`O`는 일반적으로 허용됨을, `△`는 조건에 따라 달라짐을, `X`는 일반적으로 해당하지 않음을 뜻합니다.

| 범위 | 대표적인 라이선스 | 자유 이용 | 재배포 | 소스 취득 | 수정 | 독점 SW와 결합 | 소스 재공개 필요 |
| --- | --- | :---: | :---: | :---: | :---: | :---: | :---: |
| 허용적 | MIT, BSD, ISC, Zlib, Apache-2.0 | O | O | O | O | O | X |
| 파일·모듈 단위 카피레프트 | MPL-2.0, EPL-2.0, CDDL-1.0 | O | O | O | O | △ | △ |
| 라이브러리 단위 카피레프트 | LGPL-2.1/3.0 | O | O | O | O | △ | △ |
| 강한 카피레프트 | GPL-2.0/3.0 | O | O | O | O | △ | △ |
| 네트워크 카피레프트 | AGPL-3.0 | O | O | O | O | △ | △ |

실제 사용/배포 전에는 라이선스 원문과 프로젝트의 안내를 확인해야 합니다.

참고: https://naver.github.io/OpenSourceGuide/book/UsingOss/the-legal-side-of-opensource.html
참고: https://choosealicense.com/ko/

## 한 프로젝트의 복수 라이선스

한 저장소에서도 여러 라이선스 중 하나를 선택하게 하거나, 여러 조건을 동시에 적용하거나, 파일과 구성요소마다 다른 라이선스를 사용할 수 있습니다. SPDX(Software Package Data Exchange)는 이러한 관계를 표준 형식으로 표시합니다. OR는 선택, AND는 동시 적용, WITH는 예외 조항을 뜻합니다.

- **선택**: [Rust][rust-license]의 주요 코드는 `MIT OR Apache-2.0`으로 배포되어 둘 중 하나를 선택할 수 있습니다.
- **동시 적용**: [Pyro의 `util.py`][pyro-and-license]는 Apache-2.0 코드와 MIT 코드를 함께 포함해 `Apache-2.0 AND MIT`로 표시합니다. 이 파일을 사용할 때는 두 라이선스의 조건을 함께 지켜야 합니다.
- **파일·구성요소별 적용**: [Spring Framework][spring-framework-license]는 전체적으로 Apache-2.0으로 배포되지만, `spring-core`에 재패키징된 [ASM 소스][spring-asm-license]에는 ASM의 BSD 계열 라이선스가 적용됩니다.

따라서 프로젝트의 대표 라이선스만 보고 모든 구성요소에 같은 조건이 적용된다고 단정해서는 안 됩니다.

## 자체 라이선스와 소스 공개형 라이선스

소스가 공개되었다는 넓은 의미에서 이런 소프트웨어를 오픈소스나 제한된 오픈소스라고 부르기도 합니다.

다만 용도나 서비스 제공을 제한하면 OSI의 오픈소스 정의를 충족하지 않습니다. 이 가이드에서는 이를 OSS가 아닌 `source-available`로 구분합니다.

예시 
- [MongoDB의 SSPL][mongodb-sspl]: 서비스 제공에 추가 조건을 둡니다. 
- [Sustainable Use License][n8n-license] — n8n이 사용합니다. 소스 수정·자체 호스팅은 허용하지만, 소프트웨어 자체의 기능을 이용해 상업적 서비스를 제공하는 등의 용도는 제한합니다.
- [Functional Source License (FSL)][fsl] — Sentry 등이 사용합니다. 경쟁 제품을 만드는 용도를 제한하고, 각 버전은 2년 후 Apache-2.0 또는 MIT로 전환됩니다.

## 기여 코드의 라이선스

기여한 코드는 일반적으로 프로젝트가 정한 라이선스와 기여 조건에 따라 배포됩니다.
기여자는 자신이 작성했거나 제출할 권한이 있는 코드만 제공해야 하며, 제출할 권리가 없는 회사 코드나 다른 프로젝트의 코드를 포함해서는 안 됩니다.

별도 약정이 없다면 기여자는 자신이 작성한 코드의 저작권을 유지합니다.

## CLA와 DCO

기여를 위해서 특정 동의가 필요한 경우가 있습니다. 대표적으로 CLA와 DCO가 있습니다.

- CLA(Contributor License Agreement)는 프로젝트가 기여 코드를 이용하는 데 필요한 추가 권한을 받거나 저작권 양도를 요구하는 계약입니다. 구체적인 조건은 프로젝트마다 다릅니다.
- DCO(Developer Certificate of Origin)는 기여자가 코드를 제출할 권리가 있음을 확인하는 인증 방식입니다. 일반적으로 커밋의 sign-off로 확인하며 저작권을 양도하지는 않습니다.

## 재직자의 기여 권리

재직자의 OSS 기여는 사내 정책이나 지식재산권 계약의 적용을 받을 수 있습니다.

일부 프로젝트는 저작권 양도 등 별도 동의를 요구하기도 하므로, 기여 전 관련 규정을 확인합니다.

참고: [Open Source Guides의 법률 안내](https://opensource.guide/ko/legal/)

## 참고 자료

- [라이선스가 없는 코드][choosealicense-no-permission]: 공개 저장소에 라이선스가 없을 때의 기본적인 취급
- [Open Source Definition][osi-open-source-definition]: OSS가 공통으로 허용해야 하는 재배포, 소스 제공과 수정·파생 저작물의 기준
- [OSI 승인 라이선스 목록][osi-approved-licenses]: 특정 라이선스가 OSI 승인을 받은 오픈소스 라이선스인지 확인하는 목록
- [GNU 라이선스 FAQ][gnu-license-faq]: LGPL·GPL·AGPL 코드의 결합과 소스 제공 범위에 관한 설명
- [SPDX 라이선스 표현식][spdx-license-expressions]: 여러 라이선스의 선택·동시 적용·예외를 표현하는 표준
- [MPL 2.0 FAQ][mozilla-mpl-faq]: 파일 단위 카피레프트와 배포 조건을 설명하는 공식 자료
- [Developer Certificate of Origin][dco]: 프로젝트에서 DCO 서명을 요구할 때 확인할 원문

{{#include ../_includes/references.md}}

[choosealicense-no-permission]: https://choosealicense.com/ko/no-permission/
[elastic-license-2]: https://www.elastic.co/licensing/elastic-license/faq/
[gnu-license-faq]: https://www.gnu.org/licenses/gpl-faq.html
[mariadb-bsl-11]: https://mariadb.com/bsl11/
[mongodb-sspl]: https://www.mongodb.com/legal/licensing/server-side-public-license
[mozilla-mpl-faq]: https://www.mozilla.org/en-US/MPL/2.0/FAQ/
[osi-sspl-not-open-source]: https://opensource.org/blog/the-sspl-is-not-an-open-source-license
[pyro-and-license]: https://github.com/pyro-ppl/pyro/blob/dev/pyro/ops/einsum/util.py
[samsung-c406x-notice]: https://opensource.samsung.com/opensource/Samsung_C406x_Series/seq/0
[samsung-release-center]: https://opensource.samsung.com/uploadList?menuItem=mobile
[spdx-license-expressions]: https://spdx.github.io/spdx-spec/v2.3/SPDX-license-expressions/
[spring-asm-license]: https://github.com/spring-projects/spring-framework/blob/main/spring-core/src/main/java/org/springframework/asm/ClassReader.java
[spring-framework-license]: https://github.com/spring-projects/spring-framework#license
[rust-license]: https://github.com/rust-lang/rust#license
