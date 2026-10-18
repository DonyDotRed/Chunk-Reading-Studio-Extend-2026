# D12. Limitations and Future Work
### 한계와 후속 연구 (논의: 한계 진술과 연구 제안)

| 항목 | 내용 |
|---|---|
| 시리즈 | Domain Track · Unit D 논의 (12/18) · 분야: ML·LLM 평가 |
| 수준 | 대학원·연구자 · CEFR C1–C2 |
| 분량 | 약 327단어 · 5문단 · 15문장 |
| 문체 | 연구 논문 논의 절의 한계·후속 연구 부분 (가상 연구, D03·D06·D09의 완결) |
| 핵심 문법 | 한계의 열거와 영향 방향 (First… Second…, which may have…), 완화 요인 병기 (Although…, …), 후속 연구 제안 (Future work should…, would allow…), 결론 문단 |
| 미리보기 | 구조화 초록 (D13) |

---

## 학습 방법

| 단계 | 할 일 | 권장 횟수 |
|---|---|---|
| 1회차 | 청크 단위 직독직해. 청크마다 끊어 소리 내어 읽고 바로 한국어 뜻을 떠올린다 | 3회 |
| 2회차 | 문장 단위 직독직해. 한 문장을 한 호흡으로 읽고 의미를 확인한다 | 3회 |
| 3회차 | 원문만 보고 처음부터 끝까지 낭독한다. 시간을 재서 기록한다 | 3회 이상 |

낭독 속도는 분당 단어 수(WPM)로 기록합니다. 327단어를 3분에 읽으면 약 109 WPM입니다. 회독이 거듭될수록 속도가 오르고 끊기는 지점이 줄어드는지 확인하세요.

---

## 0. 원문 (Full Text)

> Several limitations of this study should be acknowledged. First, the benchmark was constructed from a single collection of documents in one domain, and its queries were written by two experts rather than collected from actual users. Expert-written queries tend to be well formed and terminologically precise, whereas real users often pose short, ambiguous, or misspelled queries; the reported scores may therefore overestimate performance in deployment. In addition, the corpus consisted of formal regulatory text; performance on informal material such as internal memos or operating logs may differ.
>
> Second, because the pretraining corpora of the evaluated models are not fully documented, we cannot exclude the possibility that some source documents were included in training data. Although the parallel design makes it unlikely that contamination would affect all models equally, such exposure could have inflated the scores of particular models.
>
> Third, only six models were evaluated, which limits the precision of the rank correlation analysis and precludes firm conclusions about the relationship between general and domain-specific performance. The selection was constrained by the requirement that each model run on local hardware, and larger models might show a different pattern. Finally, retrieval metrics are proxies for the quality of generated answers. We did not evaluate end-to-end RAG performance, and improvements in nDCG@10 may not translate proportionally into better answers.
>
> These limitations suggest several directions for future work. Collecting queries from practitioners during actual use would allow an assessment of robustness to realistic query variation. Including documents published after the release of the evaluated models would provide a partial check against contamination. Future studies should also examine whether hybrid retrieval, combining lexical and dense methods, or lightweight domain adaptation can narrow the cross-lingual gap observed here, and should evaluate answer quality directly through expert grading.
>
> Despite these limitations, the study demonstrates that general benchmark rankings are an unreliable guide to model selection for bilingual technical retrieval, and that cross-lingual performance in particular should be measured directly before a model is deployed.

---

## 1회차 · 청크 단위 직독직해

> 영어 어순 그대로 앞에서부터 의미를 받아들이는 것이 목표입니다. 한국어 번역도 영어 순서를 따릅니다.

### 문단 1

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Several limitations | 몇 가지 한계는 |  |
| of this study | 이 연구의 |  |
| should be acknowledged. | 인정되어야 한다. | acknowledge 인정하다 |
| First, | 첫째, |  |
| the benchmark | 벤치마크는 |  |
| was constructed | 구축되었다 |  |
| from a single collection | 단일 모음으로부터 |  |
| of documents | 문서들의 |  |
| in one domain, | 한 분야의, |  |
| and its queries | 그리고 그 질의들은 |  |
| were written | 작성되었다 |  |
| by two experts | 두 전문가에 의해 |  |
| rather than collected | 수집된 것이 아니라 |  |
| from actual users. | 실제 사용자로부터. |  |
| Expert-written queries | 전문가가 작성한 질의는 |  |
| tend to be | ~한 경향이 있다 |  |
| well formed | 잘 짜여 있고 | well formed 잘 구성된 |
| and terminologically precise, | 용어상 정확하며, | terminologically 용어상 · precise 정확한 |
| whereas real users | 반면 실제 사용자는 |  |
| often pose | 흔히 던진다 | pose (질문을) 하다 |
| short, ambiguous, | 짧고, 모호하며, | ambiguous 모호한 |
| or misspelled queries; | 또는 철자가 틀린 질의를; | misspelled 철자가 틀린 |
| the reported scores | 보고된 점수는 |  |
| may therefore overestimate | 따라서 과대평가할 수 있다 | overestimate 과대평가하다 |
| performance | 성능을 |  |
| in deployment. | 실제 배포 환경에서의. | deployment 배포 |
| In addition, | 게다가, |  |
| the corpus | 말뭉치는 |  |
| consisted of | 구성되었다 |  |
| formal regulatory text; | 격식 있는 규제 문서로; | formal 격식 있는 |
| performance | 성능은 |  |
| on informal material | 비격식 자료에서의 | informal 비격식의 |
| such as internal memos | 내부 메모나 | memo 메모 |
| or operating logs | 운전 일지 같은 | operating log 운전 일지 |
| may differ. | 다를 수 있다. |  |

### 문단 2

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Second, | 둘째, |  |
| because the pretraining corpora | 사전 학습 말뭉치가 ~하기 때문에 | corpus–corpora 말뭉치 |
| of the evaluated models | 평가된 모델들의 |  |
| are not fully documented, | 완전히 문서화되어 있지 않기 때문에, | document 문서화하다 |
| we cannot exclude | 우리는 배제할 수 없다 |  |
| the possibility | 가능성을 |  |
| that some source documents | 일부 원문 문서가 |  |
| were included | 포함되었을 |  |
| in training data. | 학습 데이터에. |  |
| Although | 비록 ~하지만 |  |
| the parallel design | 병렬 설계가 |  |
| makes it unlikely | 가능성을 낮추지만 | unlikely 그럴 것 같지 않은 |
| that contamination | 오염이 |  |
| would affect | 영향을 미쳤을 |  |
| all models equally, | 모든 모델에 똑같이, | equally 똑같이 |
| such exposure | 그런 노출은 | exposure 노출 |
| could have inflated | 부풀렸을 수 있다 | inflate 부풀리다 |
| the scores | 점수를 |  |
| of particular models. | 특정 모델들의. |  |

### 문단 3

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Third, | 셋째, |  |
| only six models | 여섯 모델만이 |  |
| were evaluated, | 평가되었고, |  |
| which limits | 이는 제한한다 |  |
| the precision | 정밀도를 | precision 정밀도 |
| of the rank correlation analysis | 순위 상관 분석의 |  |
| and precludes | 그리고 불가능하게 한다 | preclude 불가능하게 하다 |
| firm conclusions | 확고한 결론을 |  |
| about the relationship | 관계에 대한 |  |
| between general | 일반 |  |
| and domain-specific performance. | 그리고 분야 특화 성능 사이의. |  |
| The selection | 선택은 |  |
| was constrained | 제약되었고 | constrain 제약하다 |
| by the requirement | 요건에 의해 |  |
| that each model | 각 모델이 |  |
| run on local hardware, | 로컬 하드웨어에서 실행되어야 한다는, |  |
| and larger models | 그리고 더 큰 모델들은 |  |
| might show | 보일 수 있다 |  |
| a different pattern. | 다른 양상을. |  |
| Finally, | 마지막으로, |  |
| retrieval metrics | 검색 지표는 | metric 지표 |
| are proxies | 대리 지표이다 | proxy 대리 지표 |
| for the quality | 품질에 대한 |  |
| of generated answers. | 생성된 답변의. |  |
| We did not evaluate | 우리는 평가하지 않았다 |  |
| end-to-end | 종단 간 | end-to-end 종단 간의 |
| RAG performance, | RAG 성능을, |  |
| and improvements | 그리고 개선이 |  |
| in nDCG@10 | nDCG@10의 |  |
| may not translate | 이어지지 않을 수 있다 | translate into ~로 이어지다 |
| proportionally | 비례하여 | proportionally 비례하여 |
| into better answers. | 더 나은 답변으로. |  |

### 문단 4

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| These limitations | 이 한계들은 |  |
| suggest | 시사한다 |  |
| several directions | 몇 가지 방향을 | direction 방향 |
| for future work. | 후속 연구를 위한. |  |
| Collecting queries | 질의를 수집하는 것은 |  |
| from practitioners | 실무자로부터 |  |
| during actual use | 실제 사용 중에 |  |
| would allow | 가능하게 할 것이다 |  |
| an assessment | 평가를 | assessment 평가 |
| of robustness | 강건성의 | robustness 강건성 |
| to realistic query variation. | 현실적인 질의 변동에 대한. | variation 변동 |
| Including documents | 문서를 포함하는 것은 |  |
| published | 발표된 |  |
| after the release | 출시 이후에 | release 출시 |
| of the evaluated models | 평가된 모델들의 |  |
| would provide | 제공할 것이다 |  |
| a partial check | 부분적 점검을 |  |
| against contamination. | 오염에 대한. |  |
| Future studies | 후속 연구는 |  |
| should also examine | 또한 살펴보아야 한다 |  |
| whether hybrid retrieval, | 혼합 검색이 ~하는지 | hybrid retrieval 혼합 검색 |
| combining lexical | 어휘 기반 |  |
| and dense methods, | 그리고 밀집 방법을 결합한, | dense 밀집의 |
| or lightweight | 또는 경량 | lightweight 경량의 |
| domain adaptation | 분야 적응이 |  |
| can narrow | 좁힐 수 있는지를 | narrow 좁히다 |
| the cross-lingual gap | 교차 언어 격차를 |  |
| observed here, | 여기서 관찰된, |  |
| and should evaluate | 그리고 평가해야 한다 |  |
| answer quality directly | 답변 품질을 직접 |  |
| through expert grading. | 전문가 채점을 통해. | grading 채점 |

### 문단 5

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Despite these limitations, | 이 한계들에도 불구하고, |  |
| the study demonstrates | 이 연구는 보여 준다 | demonstrate 보여 주다 |
| that general benchmark rankings | 일반 벤치마크 순위가 |  |
| are an unreliable guide | 신뢰할 수 없는 지침이라는 것을 | unreliable 신뢰할 수 없는 |
| to model selection | 모델 선택의 |  |
| for bilingual | 이중 언어 |  |
| technical retrieval, | 기술 문서 검색을 위한, |  |
| and that cross-lingual performance | 그리고 교차 언어 성능은 |  |
| in particular | 특히 |  |
| should be measured directly | 직접 측정되어야 한다는 것을 |  |
| before a model | 모델이 ~되기 전에 |  |
| is deployed. | 배포되기. |  |

---

## 2회차 · 문장 단위 직독직해

> 한 문장을 한 호흡에 읽는 연습입니다. 1회차에서 끊었던 지점을 의식하되, 멈추지 않고 이어 읽습니다.

### 문단 1

**① Several limitations of this study should be acknowledged.**
이 연구의 몇 가지 한계를 밝혀 둔다.
어휘: acknowledge 인정하다

**② First, the benchmark was constructed from a single collection of documents in one domain, and its queries were written by two experts rather than collected from actual users.**
첫째, 벤치마크는 한 분야의 단일 문서 모음으로 구축했고, 질의는 실제 사용자에게서 수집한 것이 아니라 전문가 두 명이 작성했다.

**③ Expert-written queries tend to be well formed and terminologically precise, whereas real users often pose short, ambiguous, or misspelled queries; the reported scores may therefore overestimate performance in deployment.**
전문가가 쓴 질의는 대체로 잘 짜여 있고 용어가 정확한 반면 실제 사용자는 짧거나 모호하거나 철자가 틀린 질의를 자주 던지므로, 보고된 점수는 실제 배포 환경의 성능을 과대평가할 수 있다.
어휘: well formed 잘 구성된 · terminologically 용어상 · precise 정확한 · pose (질문을) 하다 · ambiguous 모호한 · misspelled 철자가 틀린 · overestimate 과대평가하다 · deployment 배포

**④ In addition, the corpus consisted of formal regulatory text; performance on informal material such as internal memos or operating logs may differ.**
게다가 말뭉치는 격식 있는 규제 문서로만 이루어져 있어, 내부 메모나 운전 일지 같은 비격식 자료에서는 성능이 다를 수 있다.
어휘: formal 격식 있는 · informal 비격식의 · memo 메모 · operating log 운전 일지

### 문단 2

**⑤ Second, because the pretraining corpora of the evaluated models are not fully documented, we cannot exclude the possibility that some source documents were included in training data.**
둘째, 평가한 모델들의 사전 학습 말뭉치가 완전히 문서화되어 있지 않아, 일부 원문 문서가 학습 데이터에 포함되었을 가능성을 배제할 수 없다.
어휘: corpus–corpora 말뭉치 · document 문서화하다

**⑥ Although the parallel design makes it unlikely that contamination would affect all models equally, such exposure could have inflated the scores of particular models.**
병렬 설계 덕분에 오염이 모든 모델에 똑같이 영향을 주었을 가능성은 낮지만, 그런 노출이 특정 모델의 점수를 부풀렸을 수는 있다.
어휘: unlikely 그럴 것 같지 않은 · equally 똑같이 · exposure 노출 · inflate 부풀리다

### 문단 3

**⑦ Third, only six models were evaluated, which limits the precision of the rank correlation analysis and precludes firm conclusions about the relationship between general and domain-specific performance.**
셋째, 평가한 모델이 여섯 개뿐이어서 순위 상관 분석의 정밀도가 낮고, 일반 성능과 분야 특화 성능의 관계에 대해 확고한 결론을 내릴 수 없다.
어휘: precision 정밀도 · preclude 불가능하게 하다

**⑧ The selection was constrained by the requirement that each model run on local hardware, and larger models might show a different pattern.**
모델 선택은 로컬 하드웨어에서 실행되어야 한다는 요건에 따라 제한되었으며, 더 큰 모델에서는 다른 양상이 나타날 수 있다.
어휘: constrain 제약하다

**⑨ Finally, retrieval metrics are proxies for the quality of generated answers.**
마지막으로, 검색 지표는 생성된 답변 품질의 대리 지표일 뿐이다.
어휘: metric 지표 · proxy 대리 지표

**⑩ We did not evaluate end-to-end RAG performance, and improvements in nDCG@10 may not translate proportionally into better answers.**
종단 간 RAG 성능은 평가하지 않았으며, nDCG@10이 개선된다고 답변이 그만큼 좋아지지는 않을 수 있다.
어휘: end-to-end 종단 간의 · translate into ~로 이어지다 · proportionally 비례하여

### 문단 4

**⑪ These limitations suggest several directions for future work.**
이런 한계는 후속 연구의 몇 가지 방향을 시사한다.
어휘: direction 방향

**⑫ Collecting queries from practitioners during actual use would allow an assessment of robustness to realistic query variation.**
실제 사용 중에 실무자의 질의를 수집하면, 현실적인 질의 변동에 대해 모델이 얼마나 강건한지 평가할 수 있을 것이다.
어휘: assessment 평가 · robustness 강건성 · variation 변동

**⑬ Including documents published after the release of the evaluated models would provide a partial check against contamination.**
평가한 모델들이 출시된 이후에 발표된 문서를 포함하면 오염 여부를 부분적으로 점검할 수 있을 것이다.
어휘: release 출시

**⑭ Future studies should also examine whether hybrid retrieval, combining lexical and dense methods, or lightweight domain adaptation can narrow the cross-lingual gap observed here, and should evaluate answer quality directly through expert grading.**
후속 연구는 어휘 기반 방법과 밀집 방법을 결합한 혼합 검색이나 경량 분야 적응이 여기서 관찰한 교차 언어 격차를 좁힐 수 있는지 살펴보고, 전문가 채점으로 답변 품질을 직접 평가해야 한다.
어휘: hybrid retrieval 혼합 검색 · dense 밀집의 · lightweight 경량의 · narrow 좁히다 · grading 채점

### 문단 5

**⑮ Despite these limitations, the study demonstrates that general benchmark rankings are an unreliable guide to model selection for bilingual technical retrieval, and that cross-lingual performance in particular should be measured directly before a model is deployed.**
이런 한계에도 불구하고, 이 연구는 일반 벤치마크 순위가 이중 언어 기술 문서 검색용 모델을 고르는 데 믿을 만한 지침이 되지 못하며, 특히 교차 언어 성능은 모델을 배포하기 전에 직접 측정해야 함을 보여 준다.
어휘: demonstrate 보여 주다 · unreliable 신뢰할 수 없는

---

## 학술 영어 포인트

### 1. 한계 진술의 3요소

좋은 한계 진술은 단순히 "~가 부족했다"로 끝나지 않고, **무엇이 부족했는지 → 결과에 어떤 방향으로 영향을 주는지 → (있다면) 완화 요인**의 세 요소를 담습니다.

| 한계 | ① 무엇이 | ② 영향의 방향 | ③ 완화 요인 |
|---|---|---|---|
| 첫째 | queries were written by two experts rather than collected from actual users | the reported scores **may therefore overestimate** performance in deployment | — |
| 둘째 | pretraining corpora… are not fully documented | such exposure **could have inflated** the scores of particular models | **Although** the parallel design makes it unlikely that contamination would affect all models equally |
| 셋째 | only six models were evaluated | limits the precision… **precludes firm conclusions** | — |
| 마지막 | retrieval metrics are proxies | improvements in nDCG@10 **may not translate proportionally** into better answers | — |

**영향의 방향(과대평가인가, 과소평가인가)**을 밝히는 것이 핵심입니다. 독자는 이를 보고 결과를 어느 쪽으로 보정해서 읽어야 할지 판단할 수 있습니다.

### 2. 한계와 후속 연구를 1대1로 잇기

| 한계 | 후속 연구 제안 |
|---|---|
| 전문가 작성 질의 | Collecting queries from practitioners during actual use **would allow** an assessment of robustness |
| 오염 가능성 | Including documents published after the release… **would provide** a partial check against contamination |
| 교차 언어 격차 (D09 결과) | **should** also **examine** whether hybrid retrieval… or lightweight domain adaptation can narrow the cross-lingual gap |
| 검색 지표 = 대리 지표 | **should evaluate** answer quality directly through expert grading |

후속 연구 제안이 한계와 연결되지 않으면 막연한 소망 목록이 됩니다. **"would allow / would provide"(가정법)**는 제안된 연구의 기대 효과를, **"should"**는 권고를 나타냅니다.

### 3. 마무리 문단: 한계에도 불구하고 남는 것

> **Despite these limitations, the study demonstrates that**…

한계를 길게 서술한 뒤에는 "그럼에도 이 연구가 확실히 보여 주는 것"으로 끝맺습니다. 이때 결론의 범위는 한계를 반영해 좁혀야 합니다. 이 글은 "일반 벤치마크는 쓸모없다"가 아니라 "이중 언어 기술 문서 검색에서는 신뢰할 수 없는 지침이며, 교차 언어 성능은 직접 측정해야 한다"고 범위를 한정했습니다.

### 4. 세 연구의 완결: 서론에서 논의까지

| 연구 | 서론의 공백 | 결과의 핵심 | 논의의 결론 |
|---|---|---|---|
| RP (D01→D04→D07→D10) | 원전에서 몸통 선량계가 수정체 선량의 적절한 대리 지표인가? | Hp(3)/Hp(10) 중앙값 1.08, 예외 6쌍 | 대다수 작업은 충분, 오염 기기 근접 작업에는 차등적 접근 |
| EN (D02→D05→D08→D11) | HbA1c가 목표치인 환자에서 TIR 불일치의 의미는? | 불일치 24.3%, HR 1.46 | 목표치 HbA1c 환자에서도 연관 유지 (선행 연구 확장) |
| ML (D03→D06→D09→D12) | 일반 벤치마크 순위가 분야 성능을 예측하는가? | τ = 0.33, 교차 언어에서 순위 역전 | 교차 언어 성능은 배포 전 직접 측정 필요 |

### 5. 분야 어휘

| 영어 | 한국어 | 영어 | 한국어 |
|---|---|---|---|
| well-formed query | 잘 구성된 질의 | end-to-end evaluation | 종단 간 평가 |
| performance in deployment | 배포 환경 성능 | robustness | 강건성 |
| pretraining corpora | 사전 학습 말뭉치 | hybrid retrieval | 혼합 검색 |
| inflate the scores | 점수를 부풀리다 | lexical vs dense | 어휘 기반 vs 밀집 |
| proxy | 대리 지표 | lightweight domain adaptation | 경량 분야 적응 |

## 핵심 어휘 정리 (Domain Track 어휘장 D12)

| 어휘 | 뜻 | 어휘 | 뜻 |
|---|---|---|---|
| should be acknowledged | 인정되어야 한다 | preclude | 불가능하게 하다 |
| ambiguous | 모호한 | translate into | ~로 이어지다 |
| overestimate | 과대평가하다 | proportionally | 비례하여 |
| cannot exclude the possibility | 가능성을 배제할 수 없다 | would allow | 가능하게 할 것이다 |
| make it unlikely that | ~할 가능성을 낮추다 | narrow the gap | 격차를 좁히다 |
| inflate | 부풀리다 | despite these limitations | 이 한계들에도 불구하고 |

---

## 낭독 기록표

| 회차 | 날짜 | 소요 시간 | WPM (327 ÷ 분) | 막힌 문장 번호 |
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

*Original essay written for the 30-part reading series. Next: D13. Writing a Structured Abstract (연구 전달: 초록)*
