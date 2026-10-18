# C02. Describing Slides and Data
### 그래프·표 설명하기, 숫자와 단위 읽기

| 항목 | 내용 |
|---|---|
| 상황 | 결과 슬라이드 설명 (그래프, 표, 그림) |
| 목표 | 청중의 시선을 안내하는 순서(무엇을 → 어디를 → 무엇이 보이는지 → 의미)로 설명하고, 숫자와 단위를 정확히 읽는다 |
| 연결 자료 | D07–D09 결과 절, D16 발표 원고 Slide 4 |

---

## 1. 상황

결과 슬라이드를 띄우고 "As you can see, …"라고만 하면, 청중은 아직 축이 무엇인지도 모른 채 결론을 듣게 됩니다. 좋은 설명은 **그래프가 무엇을 보여 주는지 → 축과 기호 → 눈에 띄는 패턴 → 그 의미**의 순서를 따릅니다. 이 순서는 D07–D09에서 연습한 결과 절 서술과 같지만, 말로 할 때는 더 짧고 더 반복적입니다.

## 2. 핵심 패턴

### 2-1. 시선 안내 (4단계)

| 단계 | 패턴 | 예문 |
|---|---|---|
| ① 무엇을 | This slide shows… / Here you can see… | This slide shows the relationship between eye dose and chest dose. |
| ② 축과 기호 | On the x-axis / y-axis, we have… / Each dot represents… | On the x-axis, we have chest dose, and on the y-axis, eye dose. Each dot represents one worker in one work phase. |
| ③ 패턴 | As you can see,… / Notice that… / What stands out here is… | As you can see, most of the dots lie close to the diagonal line. |
| ④ 의미 | This means that… / What this tells us is… | What this tells us is that the chest dosimeter works well for most tasks. |

### 2-2. 비교와 변화

| 패턴 | 예문 |
|---|---|
| A is higher/lower than B. | Cross-lingual scores are lower than monolingual scores for every model. |
| X increases/decreases with Y. | The ratio increases with proximity to contaminated surfaces. |
| There's a sharp drop/rise in… | There's a sharp drop in performance when the query is in Korean and the passage is in English. |
| The difference is small/large. | The difference between Models A and C is small, and it's not statistically significant. |
| The ranking changes completely. | Interestingly, the ranking changes completely in the cross-lingual setting. |
| Let me draw your attention to… | Let me draw your attention to these six red dots in the upper left. |

### 2-3. 말할 때의 완곡 표현

| 글 (논문) | 말 (발표) |
|---|---|
| This pattern suggests a contribution from beta radiation. | We think this is probably due to beta radiation. |
| This explanation should be regarded as provisional. | But I should say this is our best guess. We didn't measure the spectrum. |
| No significant association was observed. | We didn't see a clear difference here, but the confidence interval is wide. |
| The observed values are compatible with a wide range of underlying agreement. | With only six models, I wouldn't put too much weight on this number. |

## 3. 숫자와 단위 읽기

| 표기 | 읽는 법 | 비고 |
|---|---|---|
| 1.08 | one point oh eight | 소수점 뒤는 한 자리씩 읽음. 0은 "oh" 또는 "zero" |
| 0.02 mSv | zero point zero two millisieverts / point oh two millisieverts | 1 미만 값의 단위명 단수·복수는 지침과 화자에 따라 다르며, 말할 때는 복수형이 흔함 |
| 20 mSv per year | twenty millisieverts per year | |
| 0.5 Gy | zero point five gray(s) / half a gray | 1보다 큰 값은 grays (예: two grays) |
| Hp(3) | H-P-three / H-p-three | 분야 관례에 따라 "personal dose equivalent at three millimeters"로 풀기도 함 |
| 24.3% | twenty-four point three percent | |
| 95% CI, 1.02–2.09 | ninety-five percent confidence interval, one point oh two to two point oh nine | 범위의 대시(–)는 "to" |
| HR = 1.46 | a hazard ratio of one point four six | |
| p < 0.05 | p less than zero point oh five | |
| nDCG@10 | n-D-C-G at ten | |
| τ = 0.33 | tau equals zero point three three / Kendall's tau of point three three | |
| 2,184 | two thousand one hundred (and) eighty-four | 미국식은 and 생략이 흔함 |
| 10^−3 | ten to the minus three | |

## 4. 모델 독백: 결과 슬라이드 하나 설명하기

> D09의 결과를 슬라이드 하나로 설명하는 장면입니다(약 1분).

| # | 영어 | 한국어 | 단계 |
|---|---|---|---|
| 1 | This slide shows nDCG at ten for six models under four conditions. | 이 슬라이드는 네 가지 조건에서 여섯 모델의 nDCG@10을 보여 줍니다. | ① |
| 2 | The blue bars are monolingual retrieval, and the orange bars are cross-lingual. | 파란 막대는 단일 언어 검색, 주황 막대는 교차 언어 검색입니다. | ② |
| 3 | What stands out here is that every orange bar is lower than its blue bar. | 여기서 눈에 띄는 것은 모든 주황 막대가 파란 막대보다 낮다는 점입니다. | ③ |
| 4 | But the size of the drop is very different. | 하지만 떨어지는 폭은 크게 다릅니다. | ③ |
| 5 | For Model C, it's only about point oh six, while for Model E, it's more than point two. | 모델 C는 약 0.06에 불과하지만 모델 E는 0.2가 넘습니다. | ③ |
| 6 | So the ranking changes: Model C comes first in the cross-lingual setting, and Model A drops to third. | 그래서 순위가 바뀝니다. 교차 언어에서는 모델 C가 1위로 올라서고, 모델 A는 3위로 내려갑니다. | ③ |
| 7 | What this tells us is that if your users ask questions in a different language from your documents, you really need to test cross-lingual performance directly. | 이것이 알려 주는 것은, 사용자가 문서와 다른 언어로 질문한다면 교차 언어 성능을 반드시 직접 시험해야 한다는 점입니다. | ④ |

## 5. 드릴

### 5-1. 숫자 읽기 (소리 내어, 녹음)

1. The median ratio was 1.08, with an interquartile range of 0.94 to 1.21.
2. 62 of 168 measurements (37%) were below 0.02 mSv.
3. The hazard ratio was 1.46 (95% CI, 1.02–2.09).
4. Kendall's τ was 0.33 for the Korean-to-Korean condition.
5. The limit was reduced from 150 to 20 mSv per year.

<sub>예시 읽기: ① The median ratio was one point oh eight, with an interquartile range of zero point nine four to one point two one. ② Sixty-two of one hundred and sixty-eight measurements, or thirty-seven percent, were below zero point zero two millisieverts. ③ The hazard ratio was one point four six, with a ninety-five percent confidence interval of one point oh two to two point oh nine. ④ Kendall's tau was zero point three three for the Korean-to-Korean condition. ⑤ The limit was reduced from one hundred and fifty to twenty millisieverts per year.</sub>

### 5-2. 4단계 설명 연습

자기 연구의 결과 그래프 하나를 골라 ①–④ 단계로 1분간 설명하고 녹음하세요. 단계마다 2-1의 패턴을 하나 이상 씁니다.

| 단계 | 내 문장 |
|---|---|
| ① This slide shows… | |
| ② On the x-axis… / Each … represents… | |
| ③ As you can see… / What stands out here is… | |
| ④ What this tells us is… | |

## 6. 자주 하는 실수

| 어색한 표현 | 자연스러운 표현 | 설명 |
|---|---|---|
| This graph is showing… | This graph shows… | 슬라이드 설명은 단순 현재가 자연스러움 |
| X-axis is time. | The x-axis shows time. / On the x-axis, we have time. | 관사와 동사 |
| The value is very high. (기준 없이) | The value is about 50% higher than in the control group. | 비교 기준을 말로 밝힘 |
| 2.5 mSvs | 2.5 millisieverts | 기호(mSv)는 복수형 s를 붙이지 않음, 말할 때만 복수형 |
| zero point five percents | zero point five percent | percent는 복수형 없음 |

## 7. 자기 점검

- [ ] 그래프 설명에서 ① 무엇 → ② 축 → ③ 패턴 → ④ 의미의 순서를 지켰다
- [ ] 결론(④)을 축 설명(②)보다 먼저 말하지 않았다
- [ ] 숫자를 소수점 자리까지 정확히 읽었다
- [ ] 단위를 생략하지 않았다
- [ ] 유의하지 않은 차이를 "better"나 "outperformed"로 말하지 않았다
