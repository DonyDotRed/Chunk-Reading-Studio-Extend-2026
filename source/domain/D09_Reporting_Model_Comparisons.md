# D09. Reporting Model Comparisons
### 모델 비교 결과 보고 (결과: 표 서술과 차이의 해석)

| 항목 | 내용 |
|---|---|
| 시리즈 | Domain Track · Unit C 결과 (9/18) · 분야: ML·LLM 평가 |
| 수준 | 대학원·연구자 · CEFR C1–C2 |
| 분량 | 약 256단어 · 4문단 · 13문장 |
| 문체 | 연구 논문 결과 절 (가상 연구, D03·D06의 후속) |
| 핵심 문법 | 표 지시와 범위 보고 (ranged from… to…), 차이와 신뢰구간 (Δ, 95% CI), 유의성 서술의 절제, 순위 변화 보고, 작은 표본 상관의 불확실성 |
| 미리보기 | 한계와 후속 연구 (D12) |

---

## 학습 방법

| 단계 | 할 일 | 권장 횟수 |
|---|---|---|
| 1회차 | 청크 단위 직독직해. 청크마다 끊어 소리 내어 읽고 바로 한국어 뜻을 떠올린다 | 3회 |
| 2회차 | 문장 단위 직독직해. 한 문장을 한 호흡으로 읽고 의미를 확인한다 | 3회 |
| 3회차 | 원문만 보고 처음부터 끝까지 낭독한다. 시간을 재서 기록한다 | 3회 이상 |

낭독 속도는 분당 단어 수(WPM)로 기록합니다. 256단어를 3분에 읽으면 약 85 WPM입니다. 회독이 거듭될수록 속도가 오르고 끊기는 지점이 줄어드는지 확인하세요.

---

## 0. 원문 (Full Text)

> **Monolingual retrieval**
>
> Table 2 reports performance for six models under the four evaluation conditions. In the Korean-to-Korean condition, nDCG@10 ranged from 0.61 (Model F) to 0.74 (Model A). Model A also achieved the highest Recall@10 (0.89) and MRR@10 (0.70). However, the difference between Model A and the second-ranked Model C was small and not statistically significant (ΔnDCG@10 = 0.012; 95% CI, −0.008 to 0.031). Differences between Model A and Models D–F remained significant after Holm correction. Results in the English-to-English condition followed a similar pattern, with nDCG@10 ranging from 0.65 to 0.76.
>
> **Cross-lingual retrieval**
>
> All models performed worse in cross-lingual conditions than in monolingual conditions. The decline in nDCG@10 from Korean-to-Korean to Korean-to-English ranged from 0.06 (Model C) to 0.21 (Model E). Because the decline varied substantially between models, the ranking changed: Model C achieved the highest nDCG@10 in both cross-lingual conditions (0.67 for Korean-to-English and 0.69 for English-to-Korean), whereas Model A ranked third.
>
> **Agreement with the general benchmark**
>
> Rankings on the domain benchmark showed only weak correspondence with rankings derived from the general benchmark (Kendall's τ = 0.33 for the Korean-to-Korean condition and 0.20 for the cross-lingual average). Notably, Model E, which ranked second on the general benchmark, ranked fifth in the domain monolingual condition and last in both cross-lingual conditions. With six models, however, these rank correlations are imprecise, and the observed values are compatible with a wide range of underlying agreement.
>
> **Inference cost**
>
> Encoding the full corpus required between 2 and 11 minutes per model on a single workstation GPU, with smaller models generally faster; Model C, the best cross-lingual performer, required 6 minutes.

---

## 1회차 · 청크 단위 직독직해

> 영어 어순 그대로 앞에서부터 의미를 받아들이는 것이 목표입니다. 한국어 번역도 영어 순서를 따릅니다.

### 문단 1 · Monolingual retrieval

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Table 2 reports | 표 2는 보고한다 |  |
| performance | 성능을 |  |
| for six models | 여섯 모델의 |  |
| under the four | 네 가지 |  |
| evaluation conditions. | 평가 조건에서. |  |
| In the Korean-to-Korean condition, | 한국어–한국어 조건에서, |  |
| nDCG@10 ranged | nDCG@10은 범위였다 | range 범위에 걸치다 |
| from 0.61 (Model F) | 0.61(모델 F)부터 |  |
| to 0.74 (Model A). | 0.74(모델 A)까지. |  |
| Model A | 모델 A는 |  |
| also achieved | 또한 달성했다 | achieve 달성하다 |
| the highest Recall@10 (0.89) | 가장 높은 Recall@10(0.89)과 |  |
| and MRR@10 (0.70). | MRR@10(0.70)을. |  |
| However, | 그러나, |  |
| the difference | 차이는 |  |
| between Model A | 모델 A와 |  |
| and the second-ranked Model C | 2위인 모델 C 사이의 | second-ranked 2위의 |
| was small | 작았고 |  |
| and not statistically significant | 통계적으로 유의하지 않았다 | statistically significant 통계적으로 유의한 |
| (ΔnDCG@10 = 0.012; | (ΔnDCG@10 = 0.012; |  |
| 95% CI, −0.008 to 0.031). | 95% 신뢰구간 −0.008에서 0.031). |  |
| Differences | 차이는 |  |
| between Model A | 모델 A와 |  |
| and Models D–F | 모델 D–F 사이의 |  |
| remained significant | 유의한 상태로 남았다 | remain 남다 |
| after Holm correction. | 홈 보정 후에도. | correction 보정 |
| Results | 결과는 |  |
| in the English-to-English condition | 영어–영어 조건의 |  |
| followed a similar pattern, | 비슷한 양상을 따랐으며, | pattern 양상 |
| with nDCG@10 | nDCG@10은 |  |
| ranging from 0.65 to 0.76. | 0.65에서 0.76 범위였다. |  |

### 문단 2 · Cross-lingual retrieval

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| All models | 모든 모델은 |  |
| performed worse | 더 낮은 성능을 보였다 | perform 수행하다, 성능을 보이다 |
| in cross-lingual conditions | 교차 언어 조건에서 |  |
| than in monolingual conditions. | 단일 언어 조건에서보다. |  |
| The decline in nDCG@10 | nDCG@10의 하락은 | decline 하락 |
| from Korean-to-Korean | 한국어–한국어에서 |  |
| to Korean-to-English | 한국어–영어로의 |  |
| ranged from 0.06 (Model C) | 0.06(모델 C)부터 |  |
| to 0.21 (Model E). | 0.21(모델 E)까지였다. |  |
| Because the decline | 하락 폭이 ~했기 때문에 |  |
| varied substantially | 상당히 달랐기 때문에 | vary 다르다 · substantially 상당히 |
| between models, | 모델 간에, |  |
| the ranking changed: | 순위가 바뀌었다: | ranking 순위 |
| Model C achieved | 모델 C가 달성했고 |  |
| the highest nDCG@10 | 가장 높은 nDCG@10을 |  |
| in both cross-lingual conditions | 두 교차 언어 조건 모두에서 |  |
| (0.67 for Korean-to-English | (한국어–영어 0.67 |  |
| and 0.69 for English-to-Korean), | 영어–한국어 0.69), |  |
| whereas Model A | 반면 모델 A는 |  |
| ranked third. | 3위를 기록했다. | rank (순위를) 차지하다 |

### 문단 3 · Agreement with the general benchmark

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Rankings | 순위는 |  |
| on the domain benchmark | 분야 벤치마크에서의 |  |
| showed | 보였다 |  |
| only weak correspondence | 약한 대응만을 | correspondence 대응 |
| with rankings | 순위와 |  |
| derived from | ~에서 도출된 |  |
| the general benchmark | 일반 벤치마크에서 |  |
| (Kendall's τ = 0.33 | (켄달 τ = 0.33 |  |
| for the Korean-to-Korean condition | 한국어–한국어 조건에서 |  |
| and 0.20 | 그리고 0.20 |  |
| for the cross-lingual average). | 교차 언어 평균에서). | average 평균 |
| Notably, | 주목할 만하게도, | notably 특히 |
| Model E, | 모델 E는, |  |
| which ranked second | 2위를 차지한 |  |
| on the general benchmark, | 일반 벤치마크에서, |  |
| ranked fifth | 5위를 차지했고 |  |
| in the domain | 분야 |  |
| monolingual condition | 단일 언어 조건에서 |  |
| and last | 그리고 꼴찌를 |  |
| in both cross-lingual conditions. | 두 교차 언어 조건 모두에서. |  |
| With six models, | 여섯 모델로는, |  |
| however, | 그러나, |  |
| these rank correlations | 이 순위 상관은 | rank correlation 순위 상관 |
| are imprecise, | 부정확하며, | imprecise 부정확한 |
| and the observed values | 그리고 관찰된 값은 |  |
| are compatible | 양립 가능하다 | compatible with ~와 양립하는 |
| with a wide range | 넓은 범위와 |  |
| of underlying agreement. | 기저 일치 정도의. | underlying 기저의 |

### 문단 4 · Inference cost

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Encoding the full corpus | 전체 말뭉치를 인코딩하는 것은 | encode 인코딩하다 |
| required | 필요로 했다 |  |
| between 2 and 11 minutes | 2분에서 11분 사이를 |  |
| per model | 모델당 |  |
| on a single workstation GPU, | 단일 워크스테이션 GPU에서, | workstation 워크스테이션 |
| with smaller models | 더 작은 모델이 |  |
| generally faster; | 대체로 더 빨랐다; |  |
| Model C, | 모델 C는, |  |
| the best cross-lingual performer, | 교차 언어 최고 성능 모델인, | performer 성능을 보이는 것 |
| required 6 minutes. | 6분이 걸렸다. |  |

---

## 2회차 · 문장 단위 직독직해

> 한 문장을 한 호흡에 읽는 연습입니다. 1회차에서 끊었던 지점을 의식하되, 멈추지 않고 이어 읽습니다.

### 문단 1 · Monolingual retrieval

**① Table 2 reports performance for six models under the four evaluation conditions.**
표 2는 네 가지 평가 조건에서 여섯 모델의 성능을 보여 준다.

**② In the Korean-to-Korean condition, nDCG@10 ranged from 0.61 (Model F) to 0.74 (Model A).**
한국어–한국어 조건에서 nDCG@10은 0.61(모델 F)부터 0.74(모델 A)까지였다.
어휘: range 범위에 걸치다

**③ Model A also achieved the highest Recall@10 (0.89) and MRR@10 (0.70).**
모델 A는 Recall@10(0.89)과 MRR@10(0.70)에서도 가장 높았다.
어휘: achieve 달성하다

**④ However, the difference between Model A and the second-ranked Model C was small and not statistically significant (ΔnDCG@10 = 0.012; 95% CI, −0.008 to 0.031).**
그러나 모델 A와 2위인 모델 C의 차이는 작았고 통계적으로 유의하지 않았다(ΔnDCG@10 = 0.012, 95% 신뢰구간 −0.008~0.031).
어휘: second-ranked 2위의 · statistically significant 통계적으로 유의한

**⑤ Differences between Model A and Models D–F remained significant after Holm correction.**
모델 A와 모델 D–F의 차이는 홈 보정 후에도 유의했다.
어휘: remain 남다 · correction 보정

**⑥ Results in the English-to-English condition followed a similar pattern, with nDCG@10 ranging from 0.65 to 0.76.**
영어–영어 조건의 결과도 비슷한 양상이었고, nDCG@10은 0.65에서 0.76 범위였다.
어휘: pattern 양상

### 문단 2 · Cross-lingual retrieval

**⑦ All models performed worse in cross-lingual conditions than in monolingual conditions.**
모든 모델이 단일 언어 조건보다 교차 언어 조건에서 낮은 성능을 보였다.
어휘: perform 수행하다, 성능을 보이다

**⑧ The decline in nDCG@10 from Korean-to-Korean to Korean-to-English ranged from 0.06 (Model C) to 0.21 (Model E).**
한국어–한국어에서 한국어–영어로 바뀔 때 nDCG@10의 하락 폭은 0.06(모델 C)부터 0.21(모델 E)까지였다.
어휘: decline 하락

**⑨ Because the decline varied substantially between models, the ranking changed: Model C achieved the highest nDCG@10 in both cross-lingual conditions (0.67 for Korean-to-English and 0.69 for English-to-Korean), whereas Model A ranked third.**
하락 폭이 모델마다 크게 달라 순위가 바뀌었다. 모델 C가 두 교차 언어 조건 모두에서 가장 높은 nDCG@10(한국어–영어 0.67, 영어–한국어 0.69)을 기록했고, 모델 A는 3위였다.
어휘: vary 다르다 · substantially 상당히 · ranking 순위 · rank (순위를) 차지하다

### 문단 3 · Agreement with the general benchmark

**⑩ Rankings on the domain benchmark showed only weak correspondence with rankings derived from the general benchmark (Kendall's τ = 0.33 for the Korean-to-Korean condition and 0.20 for the cross-lingual average).**
분야 벤치마크의 순위는 일반 벤치마크에서 도출한 순위와 약하게만 대응했다(켄달 τ: 한국어–한국어 조건 0.33, 교차 언어 평균 0.20).
어휘: correspondence 대응 · average 평균

**⑪ Notably, Model E, which ranked second on the general benchmark, ranked fifth in the domain monolingual condition and last in both cross-lingual conditions.**
특히 일반 벤치마크에서 2위였던 모델 E는 분야 단일 언어 조건에서 5위, 두 교차 언어 조건에서는 모두 꼴찌였다.
어휘: notably 특히

**⑫ With six models, however, these rank correlations are imprecise, and the observed values are compatible with a wide range of underlying agreement.**
그러나 모델이 여섯 개뿐이라 이 순위 상관은 부정확하며, 관찰된 값은 실제 일치 정도가 넓은 범위 어디에 있든 나올 수 있는 값이다.
어휘: rank correlation 순위 상관 · imprecise 부정확한 · compatible with ~와 양립하는 · underlying 기저의

### 문단 4 · Inference cost

**⑬ Encoding the full corpus required between 2 and 11 minutes per model on a single workstation GPU, with smaller models generally faster; Model C, the best cross-lingual performer, required 6 minutes.**
단일 워크스테이션 GPU에서 전체 말뭉치를 인코딩하는 데 모델당 2–11분이 걸렸고, 대체로 작은 모델이 빨랐다. 교차 언어 성능이 가장 좋았던 모델 C는 6분이 걸렸다.
어휘: encode 인코딩하다 · workstation 워크스테이션 · performer 성능을 보이는 것

---

## 참고 문헌

Dror, R., Baumer, G., Shlomov, S., & Reichart, R. (2018). The hitchhiker's guide to testing statistical significance in natural language processing. In *Proceedings of the 56th Annual Meeting of the Association for Computational Linguistics* (ACL 2018).

**가상 결과에 대한 주석.** D03 서론, D06 방법에 이어지는 가상 연구의 결과 절입니다. 모델명은 A–F로 익명화했고 모든 수치는 연습용으로 설정했습니다. 켄달 τ는 모델 6개(쌍 15개)에서 가능한 값(1/15 단위)에 맞췄고(0.33 = 5/15, 0.20 = 3/15), 모델 C의 교차 언어 값은 한국어–한국어 값(0.74 − 0.012 ≈ 0.73)에서 하락 폭 0.06을 뺀 값과 맞춰 두었습니다.

## 학술 영어 포인트

### 1. ML 결과 절에서 유의성을 다루는 원칙

| 피해야 할 서술 | 이 글의 서술 |
|---|---|
| Model A **outperformed** Model C. | the difference between Model A and the second-ranked Model C **was small and not statistically significant** (Δ = 0.012; 95% CI, −0.008 to 0.031) |
| Model A is the best model. | Model A **achieved the highest** nDCG@10 (단일 언어 조건에 한정) |
| The general benchmark **does not predict** domain performance. | rankings… **showed only weak correspondence**… **With six models, however, these rank correlations are imprecise** |

ML 논문에서 흔한 실수는 표에서 가장 높은 숫자를 굵게 표시하고 "능가했다(outperformed)"고 쓰는 것입니다. 차이의 신뢰구간이 0을 포함하면 그 차이는 이 자료로 구별되지 않는다고 보고해야 합니다(Dror 외, 2018).

### 2. 순위 변화 보고하기

> **Because the decline varied substantially between models, the ranking changed**: Model C achieved the highest… **whereas** Model A ranked third.

단일 언어 조건의 1위가 교차 언어 조건에서 3위로 내려간 것은 이 결과 절에서 가장 중요한 관찰입니다. 원인(하락 폭의 차이) → 결과(순위 변화) → 구체적 수치의 순서로 보고합니다.

### 3. 작은 표본 통계량의 불확실성

> With six models, however, these rank correlations are imprecise, and the observed values are **compatible with a wide range of underlying agreement**.

"compatible with"는 관찰값이 여러 가능성과 양립한다는 뜻으로, 최근 통계 보고에서 "significant / not significant"라는 이분법 대신 권장되는 표현입니다. 모델 6개의 순위 상관은 대단히 불안정하므로, 결과 절에서 미리 단서를 다는 것이 정직합니다.

### 4. 세 분야의 결과 절 비교 (D07–D09)

| 항목 | D07 (RP) | D08 (EN) | D09 (ML) |
|---|---|---|---|
| 핵심 수치 | 측정값 ± 확장 불확도 | 오즈비·위험비 + 95% CI | 지표 차이 Δ + 95% CI |
| 분포 요약 | 중앙값·사분위 범위 (중도절단 고려) | 평균(SD), 중앙값(IQR) | 범위 (ranged from… to…) |
| 특유의 쟁점 | 검출 한계 미만 값 | 연관과 인과의 구분 | 유의하지 않은 차이의 과대 해석 |
| 공통 원칙 | 결과 절에서는 보고하고, 해석은 논의 절로 |

### 5. 분야 어휘

| 영어 | 한국어 | 영어 | 한국어 |
|---|---|---|---|
| second-ranked | 2위의 | rank correlation | 순위 상관 |
| statistically significant | 통계적으로 유의한 | compatible with | ~와 양립하는 |
| after Holm correction | 홈 보정 후 | underlying agreement | 기저 일치 정도 |
| monolingual / cross-lingual | 단일 언어 / 교차 언어 | inference cost | 추론 비용 |
| decline in nDCG | nDCG 하락 | workstation GPU | 워크스테이션 GPU |

## 핵심 어휘 정리 (Domain Track 어휘장 D09)

| 어휘 | 뜻 | 어휘 | 뜻 |
|---|---|---|---|
| range from A to B | A부터 B까지 걸치다 | vary substantially | 크게 달라지다 |
| achieve the highest | 가장 높은 값을 기록하다 | rank third | 3위를 하다 |
| not statistically significant | 통계적으로 유의하지 않은 | weak correspondence | 약한 대응 |
| remain significant | 유의성이 유지되다 | notably | 특히 |
| follow a similar pattern | 비슷한 양상을 보이다 | imprecise | 부정확한 |
| perform worse | 성능이 더 낮다 | performer | (성능을 보이는) 모델 |

---

## 낭독 기록표

| 회차 | 날짜 | 소요 시간 | WPM (256 ÷ 분) | 막힌 문장 번호 |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |
| 6 | | | | |
| 7 | | | | |
| 8 | | | | |
| 9 | | | | |

---

*Original essay written for the 30-part reading series. Next: D10. Interpreting the Principal Findings (논의: 주요 결과 해석)*
