# PART 2. 데이터 분석 기획
# 1장 데이터 분석 기획의 이해
## 1절 분석기획 방향성 도출

### 분석대상과 방법에 따른 분석 유형
분석의 대상 known    / 분석의 방법 known    : Optimization (최적화)
분석의 대상 un-known / 분석의 방법 known    : insight (통찰)
분석의 대상 known    / 분석의 방법 un-known : solution (해결책)
분석의 대상 un-known / 분석의 방법 un-known : discovery (발견)

### 분석기획시 고려사항
정형데이터 : 데이터 자체로 분석가능, RDB 구조의 데이터, 데이터베이스로 관리 (DB로 정제된 데이터)
ex: ERP, CRM, SCM 등 정보시스템, Demand Forecast(수요예측), transportation costs

반정형데이터: 데이터로 분석이 가능하지만 해석이 불가능하며 메타정보를 활용해야 해석이 가능(센서 중심으로 스트리밍되는 머신데이터)
ex: 로그데이터, 모바일데이터, 센싱데이터, competitior pricing 

비정형데이터: 데이터 자체로 분석이 불가능, 특별한 처리 프로세스를 거쳐 분석데이터로 변경 후 분석(보고서, 소셜미디어 데이터)
ex: 영상, 음성, 문자, 이메일, 보고서, 소셜미디어, 블로그와 뉴스 등