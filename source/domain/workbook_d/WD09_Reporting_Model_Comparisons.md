# 역번역 워크북 · D09. Reporting Model Comparisons
### 모델 비교 결과 보고 (결과: 표 서술과 차이의 해석)

| 항목 | 내용 |
|---|---|
| 원본 | D09_Reporting_Model_Comparisons.md |
| 트랙 | Domain Track (C1–C2) |
| 문장 수 / 단어 수 | 13문장 / 약 256단어 |
| 집중 포인트 | 표 지시와 범위 보고 (ranged from… to…), 차이와 신뢰구간 (Δ, 95% CI), 유의성 서술의 절제, 순위 변화 보고, 작은 표본 상관의 불확실성 |
| 권장 소요 시간 | 1차 풀이 약 25분 (채점·섀도잉 별도) |

## 진행 순서

1. **Part A** 한국어 문장을 보고 영어로 씁니다. 처음에는 힌트를 보며 풀고, 복습 때는 힌트를 가리고 풉니다.
2. **Part D** 정답과 비교해 **Part C**에 점수(0–3)와 오류 유형 코드를 적습니다. 채점 기준은 `00W_Backtranslation_Guide.md`에 있습니다.
3. **Part D**의 끊어 읽기 스크립트로 정답 문장을 섀도잉합니다.
4. **Part B** 리텔링을 원문을 보지 않고 수행합니다.
5. 1일·3일·7일·21일 뒤에 2점 이하 문장만 다시 풉니다.

> 한국어 번역은 직역이 아니라 자연스러운 의역입니다. 정답과 문장 구조가 달라도 의미와 핵심 어휘가 맞으면 높은 점수를 주세요.

---

## Part A. 역번역 문제

### 문단 1 · Monolingual retrieval

**①** 표 2는 네 가지 평가 조건에서 여섯 모델의 성능을 보여 준다.  
<sub>힌트 (12단어): —</sub>  
✍️ 

**②** 한국어–한국어 조건에서 nDCG@10은 0.61(모델 F)부터 0.74(모델 A)까지였다.  
<sub>힌트 (14단어): range 범위에 걸치다</sub>  
✍️ 

**③** 모델 A는 Recall@10(0.89)과 MRR@10(0.70)에서도 가장 높았다.  
<sub>힌트 (11단어): achieve 달성하다</sub>  
✍️ 

**④** 그러나 모델 A와 2위인 모델 C의 차이는 작았고 통계적으로 유의하지 않았다(ΔnDCG@10 = 0.012, 95% 신뢰구간 −0.008~0.031).  
<sub>힌트 (25단어): second-ranked 2위의 · statistically significant 통계적으로 유의한</sub>  
✍️ 

**⑤** 모델 A와 모델 D–F의 차이는 홈 보정 후에도 유의했다.  
<sub>힌트 (12단어): remain 남다 · correction 보정</sub>  
✍️ 

**⑥** 영어–영어 조건의 결과도 비슷한 양상이었고, nDCG@10은 0.65에서 0.76 범위였다.  
<sub>힌트 (16단어): pattern 양상</sub>  
✍️ 

### 문단 2 · Cross-lingual retrieval

**⑦** 모든 모델이 단일 언어 조건보다 교차 언어 조건에서 낮은 성능을 보였다.  
<sub>힌트 (11단어): perform 수행하다, 성능을 보이다</sub>  
✍️ 

**⑧** 한국어–한국어에서 한국어–영어로 바뀔 때 nDCG@10의 하락 폭은 0.06(모델 C)부터 0.21(모델 E)까지였다.  
<sub>힌트 (17단어): decline 하락</sub>  
✍️ 

**⑨** 하락 폭이 모델마다 크게 달라 순위가 바뀌었다. 모델 C가 두 교차 언어 조건 모두에서 가장 높은 nDCG@10(한국어–영어 0.67, 영어–한국어 0.69)을 기록했고, 모델 A는 3위였다.  
<sub>힌트 (32단어): vary 다르다 · substantially 상당히 · ranking 순위 · rank (순위를) 차지하다</sub>  
✍️ 

### 문단 3 · Agreement with the general benchmark

**⑩** 분야 벤치마크의 순위는 일반 벤치마크에서 도출한 순위와 약하게만 대응했다(켄달 τ: 한국어–한국어 조건 0.33, 교차 언어 평균 0.20).  
<sub>힌트 (30단어): correspondence 대응 · average 평균</sub>  
✍️ 

**⑪** 특히 일반 벤치마크에서 2위였던 모델 E는 분야 단일 언어 조건에서 5위, 두 교차 언어 조건에서는 모두 꼴찌였다.  
<sub>힌트 (23단어): notably 특히</sub>  
✍️ 

**⑫** 그러나 모델이 여섯 개뿐이라 이 순위 상관은 부정확하며, 관찰된 값은 실제 일치 정도가 넓은 범위 어디에 있든 나올 수 있는 값이다.  
<sub>힌트 (22단어): rank correlation 순위 상관 · imprecise 부정확한 · compatible with ~와 양립하는 · underlying 기저의</sub>  
✍️ 

### 문단 4 · Inference cost

**⑬** 단일 워크스테이션 GPU에서 전체 말뭉치를 인코딩하는 데 모델당 2–11분이 걸렸고, 대체로 작은 모델이 빨랐다. 교차 언어 성능이 가장 좋았던 모델 C는 6분이 걸렸다.  
<sub>힌트 (31단어): encode 인코딩하다 · workstation 워크스테이션 · performer 성능을 보이는 것</sub>  
✍️ 

---

## Part B. 리텔링 과제

원문을 보지 않고 아래 구조에 맞춰 **영어로 4–5문장** 말하거나 쓰세요. 학술 문체(완곡 표현, 출처를 밝히는 동사, 명사화)를 의식적으로 사용합니다.

| 단계 | 내용 | 문장 수 |
|---|---|---|
| 논제 | 이 글이 주장하거나 설명하는 핵심 | 1 |
| 전개 | 핵심 근거, 개념, 또는 분석 단계 | 2–3 |
| 마무리 | 한계·단서 또는 결론 | 1 |

**필수 사용 어휘** (5개 이상 사용):

range from A to B (A부터 B까지 걸치다) · vary substantially (크게 달라지다) · achieve the highest (가장 높은 값을 기록하다) · rank third (3위를 하다) · not statistically significant (통계적으로 유의하지 않은) · weak correspondence (약한 대응) · remain significant (유의성이 유지되다) · notably (특히) · follow a similar pattern (비슷한 양상을 보이다) · imprecise (부정확한) · perform worse (성능이 더 낮다) · performer ((성능을 보이는) 모델)

✍️ 

✍️ 

✍️ 

---

## Part C. 채점표 및 오류 기록

점수: 3 = 의미·핵심 구조·핵심 어휘 일치 · 2 = 의미 일치, 구조나 어휘 한 곳 차이 · 1 = 의미 일부만 일치 · 0 = 의미 불일치  
오류 코드: **A** 관사·한정사 · **T** 시제·상 · **P** 전치사 · **W** 어순·문장 구조 · **V** 어휘 선택 · **S** 수 일치 · **O** 누락·추가 · **R** 문체·격식

| 문장 | 1차 점수 | 오류 코드 | 메모 (맞게 고친 표현) | 1일 | 3일 | 7일 | 21일 |
|---|---|---|---|---|---|---|---|
| ① | | | | | | | |
| ② | | | | | | | |
| ③ | | | | | | | |
| ④ | | | | | | | |
| ⑤ | | | | | | | |
| ⑥ | | | | | | | |
| ⑦ | | | | | | | |
| ⑧ | | | | | | | |
| ⑨ | | | | | | | |
| ⑩ | | | | | | | |
| ⑪ | | | | | | | |
| ⑫ | | | | | | | |
| ⑬ | | | | | | | |

**1차 합계:** ____ / 39점  ·  **가장 많은 오류 코드:** ____

---

## Part D. 정답과 섀도잉 스크립트 (풀이 후 확인)

> 끊어 읽기 표시( / )는 1회차 청크 경계입니다. 섀도잉은 음성 없이 시작해도 됩니다. 먼저 끊어 읽기 단위로 소리 내어 읽고, 익숙해지면 표시를 무시하고 한 호흡에 읽으세요.

### 문단 1 · Monolingual retrieval

**①** Table 2 reports performance for six models under the four evaluation conditions.  
<sub>↳ Table 2 reports / performance / for six models / under the four / evaluation conditions.</sub>

**②** In the Korean-to-Korean condition, nDCG@10 ranged from 0.61 (Model F) to 0.74 (Model A).  
<sub>↳ In the Korean-to-Korean condition, / nDCG@10 ranged / from 0.61 (Model F) / to 0.74 (Model A).</sub>

**③** Model A also achieved the highest Recall@10 (0.89) and MRR@10 (0.70).  
<sub>↳ Model A / also achieved / the highest Recall@10 (0.89) / and MRR@10 (0.70).</sub>

**④** However, the difference between Model A and the second-ranked Model C was small and not statistically significant (ΔnDCG@10 = 0.012; 95% CI, −0.008 to 0.031).  
<sub>↳ However, / the difference / between Model A / and the second-ranked Model C / was small / and not statistically significant / (ΔnDCG@10 = 0.012; / 95% CI, −0.008 to 0.031).</sub>

**⑤** Differences between Model A and Models D–F remained significant after Holm correction.  
<sub>↳ Differences / between Model A / and Models D–F / remained significant / after Holm correction.</sub>

**⑥** Results in the English-to-English condition followed a similar pattern, with nDCG@10 ranging from 0.65 to 0.76.  
<sub>↳ Results / in the English-to-English condition / followed a similar pattern, / with nDCG@10 / ranging from 0.65 to 0.76.</sub>

### 문단 2 · Cross-lingual retrieval

**⑦** All models performed worse in cross-lingual conditions than in monolingual conditions.  
<sub>↳ All models / performed worse / in cross-lingual conditions / than in monolingual conditions.</sub>

**⑧** The decline in nDCG@10 from Korean-to-Korean to Korean-to-English ranged from 0.06 (Model C) to 0.21 (Model E).  
<sub>↳ The decline in nDCG@10 / from Korean-to-Korean / to Korean-to-English / ranged from 0.06 (Model C) / to 0.21 (Model E).</sub>

**⑨** Because the decline varied substantially between models, the ranking changed: Model C achieved the highest nDCG@10 in both cross-lingual conditions (0.67 for Korean-to-English and 0.69 for English-to-Korean), whereas Model A ranked third.  
<sub>↳ Because the decline / varied substantially / between models, / the ranking changed: / Model C achieved / the highest nDCG@10 / in both cross-lingual conditions / (0.67 for Korean-to-English / and 0.69 for English-to-Korean), / whereas Model A / ranked third.</sub>

### 문단 3 · Agreement with the general benchmark

**⑩** Rankings on the domain benchmark showed only weak correspondence with rankings derived from the general benchmark (Kendall's τ = 0.33 for the Korean-to-Korean condition and 0.20 for the cross-lingual average).  
<sub>↳ Rankings / on the domain benchmark / showed / only weak correspondence / with rankings / derived from / the general benchmark / (Kendall's τ = 0.33 / for the Korean-to-Korean condition / and 0.20 / for the cross-lingual average).</sub>

**⑪** Notably, Model E, which ranked second on the general benchmark, ranked fifth in the domain monolingual condition and last in both cross-lingual conditions.  
<sub>↳ Notably, / Model E, / which ranked second / on the general benchmark, / ranked fifth / in the domain / monolingual condition / and last / in both cross-lingual conditions.</sub>

**⑫** With six models, however, these rank correlations are imprecise, and the observed values are compatible with a wide range of underlying agreement.  
<sub>↳ With six models, / however, / these rank correlations / are imprecise, / and the observed values / are compatible / with a wide range / of underlying agreement.</sub>

### 문단 4 · Inference cost

**⑬** Encoding the full corpus required between 2 and 11 minutes per model on a single workstation GPU, with smaller models generally faster; Model C, the best cross-lingual performer, required 6 minutes.  
<sub>↳ Encoding the full corpus / required / between 2 and 11 minutes / per model / on a single workstation GPU, / with smaller models / generally faster; / Model C, / the best cross-lingual performer, / required 6 minutes.</sub>

---

*원본 에세이: D09_Reporting_Model_Comparisons.md · 이 워크북은 원본의 2회차 번역과 1회차 청크에서 자동 생성되었습니다.*
