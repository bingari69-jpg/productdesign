# 조사 출처와 적용 범위

확인일: 2026-10-29 (한국 시간). 공개 1차 자료를 중심으로 읽고 아래 설계 절차로 종합했다. 자료 전문을 복제하거나 외부 스킬을 설치한 묶음은 아니다. 이 목록이 모든 디자인 지식을 포괄하거나 결과의 우수성을 보증하지 않는다.

## 설계 방법과 연구

1. [Design Council · Double Diamond](https://www.designcouncil.org.uk/resources/the-double-diamond/)
   - 확인: 공식 설명. 문제 탐색과 해결안 탐색을 구분하는 참고 틀.
   - 적용: 성급한 외형 확정 전에 사용자 문제와 여러 해결 방향을 검토. 작은 수정에 전체 절차를 강제하지 않음.
2. [NN/g · Aesthetic–Usability Effect](https://www.nngroup.com/articles/aesthetic-usability-effect/)
   - 확인: 공개 본문. 시각적 호감과 실제 과업 성공을 별도로 검토할 이유.
   - 적용: 예쁘다는 평가만으로 사용성 검증을 대체하지 않음.
3. [NN/g · Recognition and Recall](https://www.nngroup.com/articles/recognition-and-recall/)
   - 확인: 공개 본문. 기억 부담과 맥락 제공의 관계.
   - 적용: 필요한 선택·상태·도움을 사용 위치에 제시.
4. [Wadinambiarachchi et al. · The Effects of Generative AI on Design Fixation and Divergent Thinking, CHI 2024](https://arxiv.org/abs/2403.11164)
   - 확인: 원논문 등록 페이지와 초록. N=60의 시각 아이디어 과제에서 AI 이미지 지원 집단의 고착 증가와 대안 감소 보고.
   - 적용: 초기에 구조가 다른 대안을 비교. 모든 과제나 도구에서 AI가 창의성을 낮춘다는 주장으로 확대하지 않음. 전문·실험 데이터 재분석은 하지 않음.
5. [Li et al. · Beyond Input-Output: Rethinking Creativity through Design-by-Analogy, CHI 2026](https://arxiv.org/abs/2602.09423)
   - 확인: 등록 페이지와 초록. 85개 연구를 검토한 유추 설계 논의.
   - 적용: 다른 분야에서 기능 원리를 찾아 현재 문제에 맞게 변환. 특정 스킬의 성능 입증 자료는 아님.
6. [Baymard · 2024 Checkout Research](https://baymard.com/research-articles/checkout-2024-launch)
   - 확인: 공개 연구 소개와 사례 설명. 유료 전체 지침·연구 세션 영상은 미확인.
   - 적용: 실행 결과가 분명한 버튼 문구와 오류 복구. 전환율 개선 수치를 개별 프로젝트에 약속하지 않음.

## 웹·앱 기준과 실제 제품 자료

7. [W3C · WCAG 2.2](https://www.w3.org/TR/WCAG22/)
   - 확인: 공식 권고안. 디지털 가이드의 대비·키보드·확대·상태·입력 기준 출처. 전체 준수 판정은 별도 검증 필요.
8. [W3C · Target Size Minimum](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html)
   - 확인: 24 CSS px 기준과 간격·인라인 등 예외. 모바일의 편의상 권장 크기와 AA 규격을 구분.
9. [W3C · ARIA Authoring Practices Patterns](https://www.w3.org/WAI/ARIA/apg/patterns/)
   - 확인: 공식 패턴 목록과 역할 설명. 실제 작업에서 해당 위젯의 세부 키보드 규칙을 추가 확인.
10. [GOV.UK · Error Summary](https://design-system.service.gov.uk/components/error-summary/)
    - 확인: 본문·코드 예제. 오류 요약과 해당 입력으로 이동하는 복구 구조의 사례. 영국 정부 서비스의 문구를 모든 제품에 강제하지 않음.
11. [USWDS · Design Tokens](https://designsystem.digital.gov/design-tokens/)
    - 확인: 공식 개념 설명. 색·간격·타이포그래피의 이름 있는 값으로 구현과 설계를 연결.
12. [Android Developers · Canonical Layouts](https://developer.android.com/develop/ui/views/layout/canonical-layouts)
    - 확인: 목록/상세·피드·보조 패널 설명. 공간에 따라 구조를 바꾸고 선택 상태를 보존하는 사례. 실제 앱 실행·영상 재생은 하지 않음.
13. [Linear · Select Issues](https://linear.app/docs/select-issues)
    - 확인: 공개 사용 문서. 선택과 강조, 복수 선택, 명령 실행의 분리 사례. 로그인 뒤 앱을 조작한 것은 아님.
14. [Stripe · Payment Intents](https://docs.stripe.com/payments/payment-intents)
    - 확인: 공개 API 개념·상태 설명. 결제 UI에 실제 처리 상태와 실패 복구가 필요한 사례. 특정 통합 방식은 구현 시 최신 권장 경로를 다시 확인.
15. [Google · Web Vitals](https://web.dev/articles/vitals)
    - 확인: 공식 지표 개요. 사용자 성능 측정의 참고 자료. 이번 스킬 제작에서 웹 성능을 측정한 것은 아님.

## GitHub 구현·스킬 조사

16. [Radix · Dialog Source](https://github.com/radix-ui/primitives/blob/main/packages/react/dialog/src/dialog.tsx)
    - 확인: 230~410행의 오버레이·모달/비모달·포커스 복귀 처리. blob `bd8ac8ddf5465e1cb32e0c4bde6930d3c151b745`.
    - 적용: 보이는 모양 외에 포커스·스크롤·닫힘 상태를 검증. 코드를 복제하거나 라이브러리를 실행하지 않음.
17. [Adobe · React Spectrum / React Aria](https://github.com/adobe/react-spectrum/blob/main/README.md)
    - 확인: README. blob `3e165434ad64dd3444f69ad8690151eb2ba0f151`.
    - 적용: 시각 스타일과 상호작용·접근성을 분리하는 구현 후보. 사용 프로젝트에서 동작 검증은 별도.
18. [shadcn/ui](https://github.com/shadcn-ui/ui/blob/main/README.md)
    - 확인: README와 라이선스 안내. blob `35657b37e0ef00aa7b477896d51a8fd0d5af8f49`.
    - 적용: 편집 가능한 컴포넌트 원본의 활용 후보. 기본 외형을 모든 사용자에게 고정하지 않음.
19. [Anthropic · Frontend Design Skill](https://github.com/anthropics/skills/blob/main/skills/frontend-design/SKILL.md)
    - 확인: 공개 파일. blob `a5333457c414d20d625f307df945842c0952ecc3`.
    - 적용: 브리프와 연결된 미적 판단, 실제 결과를 보며 수정하는 관점 참고. 특정 서체·색·유행 금지 목록을 이식하지 않음. 원문 설치·복제 없음.
20. [Vercel Labs · Web Interface Guidelines](https://github.com/vercel-labs/web-interface-guidelines/blob/main/AGENTS.md)
    - 확인: 공개 파일. blob `2785de041ab86453abcdbedd999084e6c207d6df`.
    - 적용: 상호작용·콘텐츠·구현 검토의 참고. 해당 문서의 강한 표현을 보편 규정으로 복사하지 않음. 대비 판정은 WCAG 규범을 우선하고 APCA와 구분.
21. [OpenSCAD](https://github.com/openscad/openscad/blob/master/README.md)
    - 확인: README 도입부. blob `a16f83066366e7e800699abf117cb12358a59c6f`.
    - 적용: 매개변수 기반 CAD 원본의 후보. 설치·실행·CAD 파일 시험은 하지 않음.

## 실물 제품과 제조

22. [Protolabs · Injection Molding Wall Thickness](https://www.protolabs.com/resources/design-tips/improving-part-design-with-uniform-wall-thickness/)
    - 확인: 공정 지침과 재료별 범위. 벽·리브·보스·구배를 공정 조건에 맞춰 검토. 숫자를 모든 재료에 공통 규격으로 고정하지 않음.
23. [Protolabs · CNC DFM Toolkit](https://www.protolabs.com/resources/design-for-machining-toolkit/)
    - 확인: 공개 설계 안내. 공구 접근·내부 형상·가공 제약을 확인하는 출발점.
24. [Protolabs · Sheet Metal Design Guidelines](https://www.protolabs.com/services/sheet-metal-fabrication/design-guidelines/)
    - 확인: 공개 제작 지침. 굽힘과 주변 형상의 관계 검토. 해당 업체의 수치를 범용 공차로 사용하지 않음.
25. [Formlabs · Form 4 Design Guide](https://formlabs.com/white-papers/form-4-design-guide/)
    - 확인: 웹 본문. Form 4·Grey Resin·50μm 조건이 명시된 기능 치수 지침. PDF 다운로드·출력 시험은 하지 않음.
    - 적용: 장비·소재·적층 조건을 함께 기록하고 다른 공정으로 수치를 전이하지 않음.
26. [NIST · Additive Manufacturability and Assemblability](https://www.nist.gov/publications/part-decomposition-and-evaluation-based-standard-design-guidelines-additive)
    - 확인: 연구기관의 논문 설명·초록. 적층 가능성과 부품 분할·조립을 함께 검토하는 근거. ISO/ASTM 유료 규격 전문은 미확인.
27. [iFixit · Repairability](https://www.ifixit.com/repairability)
    - 확인: 수리성의 공식 설명. 분해·재조립·부품·도구·정비 자료의 관점. 특정 기기를 분해하거나 수리성 점수를 산정하지 않음.

## 접근 실패·확인 한계

- Apple HIG의 기본 페이지는 JavaScript 안내만 반환했고 Markdown 링크도 도구에서 열리지 않았다. 세부 HIG를 읽었다고 주장하지 않는다. iOS/macOS 설계에서는 [공식 HIG](https://developer.apple.com/design/human-interface-guidelines/)를 접근 가능한 방식으로 다시 확인한다.
- Linear의 추측한 keyboard-shortcuts URL은 404였다. 검색으로 찾은 실제 Select Issues 문서를 대신 확인했다.
- 이번 조사는 스킬 설계용 공개 자료 조사다. 앱 로그인 조작·유료 연구 열람·새 디자인 생성·사용자 실험·공장 견적·시제품 제작을 수행한 기록이 아니다.

## 추가 GitHub 조사 · 2026-10-31

아래 자료의 SKILL.md 또는 README를 읽고 우리 작업에 필요한 판단 절차를 새 문장으로 정리했다. 외부 파일·코드·설치 스크립트를 복사하거나 실행하지 않았다. 원문에 있는 승인 반복·도구 의존성·보편 수치와 성능 주장을 그대로 채택하지 않는다.

28. [shawnlix · Product Designer Skill](https://github.com/shawnlix/claude-product-designer-skill)
    - 확인: SKILL.md·README. 형태 탐색, 내부 공간, 기구, 재료와 렌더를 구분한 절차.
    - 반영: 형태·공간·동작 검토를 실제 제작 제약과 연결. 20~50장 스케치·매 단계 승인·특정 이미지 생성 도구 의존은 채택하지 않음. 글로 작성한 기구 설명을 기능 입증으로 취급하지 않음.
29. [wonsukchoi · Commercial / Industrial Designer](https://github.com/wonsukchoi/domain-experts/blob/main/roles/commercial-industrial-designer/SKILL.md)
    - 확인: SKILL.md, draft 표기. blob `6b88b84e233f49fceb689a1e3652078cd6700bc6`.
    - 반영: 생산량·공정·금형비/개당비·재료 비교와 질문별 작은 시제품. 원문의 힘·구배·인체 범위 숫자는 제품·재료·사용자별 근거 확인 없이 공통 규격으로 쓰지 않음.
30. [Gayaya999 · Product Design Three Views](https://github.com/Gayaya999/product-design-three-views)
    - 확인: SKILL.md. blob `7a08331d9a478f6c554d8ecf114e47e275628b4f`.
    - 반영: 형태·구조·상호작용·재료를 분리해 참고 스타일을 해석하고 기준 형상과 부품 목록을 유지하며 뷰를 비교. 고정 3장 산출·브랜드 선택·생성 전 승인 반복은 도입하지 않음. 선화를 정밀 도면으로 취급하지 않음.
31. [CadQuery](https://github.com/CadQuery/cadquery)
    - 확인: README. blob `090c35145118878ee62af919ca7854214171e697`.
    - 반영: 매개변수 CAD·조립·STEP 등 출력의 도구 후보. 이번 업데이트에서 설치·모델링·내보내기 시험은 하지 않음.
32. [build123d](https://github.com/gumyr/build123d)
    - 확인: README. blob `0f0487ce7c3b9789e0781d2e12bbf6691b8a61c4`.
    - 반영: Python 기반 곡선·스케치·솔리드 모델 도구 후보. CadQuery와 둘 다 설치하는 것을 요구하지 않음. 실행·제품 검증은 별도.
33. [UI UX Pro Max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)
    - 확인: README. blob `074a2706ee60450eecabf2a1e8b777c345f5baf7`.
    - 반영: 스타일·색·서체·레이아웃의 구조화된 비교. 카탈로그 추천이나 제작자 설명을 검증된 접근성·전환 성능으로 간주하지 않음. 데이터·CLI를 가져오지 않음.
34. [Impeccable](https://github.com/pbakaus/impeccable)
    - 확인: README. blob `8f27aa965cb56ab578d637e53f0392ae4e2d06db`.
    - 반영: UI 비평·미적 정돈·기술 검사를 구분하고 지정 부분부터 반복 수정. 도구의 명령·규칙 탐지·후크는 설치하거나 성능을 시험하지 않음.
35. [JoaoMonteiro100 · UX Design Skills](https://github.com/JoaoMonteiro100/ux-design-skills)
    - 확인: README. blob `8759d3ec311a64d7237ba5afa2b58910905eb595`.
    - 반영: 경쟁 분석·페르소나·사용성·접근성의 목적별 구분과 근거 범위. 제작자가 보고한 평가를 우리 환경의 독립 검증으로 표현하지 않음.
