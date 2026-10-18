# 역번역 워크북 · D12. Limitations and Future Work
### 한계와 후속 연구 (논의: 한계 진술과 연구 제안)

| 항목 | 내용 |
|---|---|
| 원본 | D12_Limitations_and_Future_Work.md |
| 트랙 | Domain Track (C1–C2) |
| 문장 수 / 단어 수 | 15문장 / 약 327단어 |
| 집중 포인트 | 한계의 열거와 영향 방향 (First… Second…, which may have…), 완화 요인 병기 (Although…, …), 후속 연구 제안 (Future work should…, would allow…), 결론 문단 |
| 권장 소요 시간 | 1차 풀이 약 27분 (채점·섀도잉 별도) |

## 진행 순서

1. **Part A** 한국어 문장을 보고 영어로 씁니다. 처음에는 힌트를 보며 풀고, 복습 때는 힌트를 가리고 풉니다.
2. **Part D** 정답과 비교해 **Part C**에 점수(0–3)와 오류 유형 코드를 적습니다. 채점 기준은 `00W_Backtranslation_Guide.md`에 있습니다.
3. **Part D**의 끊어 읽기 스크립트로 정답 문장을 섀도잉합니다.
4. **Part B** 리텔링을 원문을 보지 않고 수행합니다.
5. 1일·3일·7일·21일 뒤에 2점 이하 문장만 다시 풉니다.

> 한국어 번역은 직역이 아니라 자연스러운 의역입니다. 정답과 문장 구조가 달라도 의미와 핵심 어휘가 맞으면 높은 점수를 주세요.

---

## Part A. 역번역 문제

### 문단 1

**①** 이 연구의 몇 가지 한계를 밝혀 둔다.  
<sub>힌트 (8단어): acknowledge 인정하다</sub>  
✍️ 

**②** 첫째, 벤치마크는 한 분야의 단일 문서 모음으로 구축했고, 질의는 실제 사용자에게서 수집한 것이 아니라 전문가 두 명이 작성했다.  
<sub>힌트 (28단어): —</sub>  
✍️ 

**③** 전문가가 쓴 질의는 대체로 잘 짜여 있고 용어가 정확한 반면 실제 사용자는 짧거나 모호하거나 철자가 틀린 질의를 자주 던지므로, 보고된 점수는 실제 배포 환경의 성능을 과대평가할 수 있다.  
<sub>힌트 (29단어): well formed 잘 구성된 · terminologically 용어상 · precise 정확한 · pose (질문을) 하다 · ambiguous 모호한 · misspelled 철자가 틀린 · overestimate 과대평가하다 · deployment 배포</sub>  
✍️ 

**④** 게다가 말뭉치는 격식 있는 규제 문서로만 이루어져 있어, 내부 메모나 운전 일지 같은 비격식 자료에서는 성능이 다를 수 있다.  
<sub>힌트 (22단어): formal 격식 있는 · informal 비격식의 · memo 메모 · operating log 운전 일지</sub>  
✍️ 

### 문단 2

**⑤** 둘째, 평가한 모델들의 사전 학습 말뭉치가 완전히 문서화되어 있지 않아, 일부 원문 문서가 학습 데이터에 포함되었을 가능성을 배제할 수 없다.  
<sub>힌트 (27단어): corpus–corpora 말뭉치 · document 문서화하다</sub>  
✍️ 

**⑥** 병렬 설계 덕분에 오염이 모든 모델에 똑같이 영향을 주었을 가능성은 낮지만, 그런 노출이 특정 모델의 점수를 부풀렸을 수는 있다.  
<sub>힌트 (24단어): unlikely 그럴 것 같지 않은 · equally 똑같이 · exposure 노출 · inflate 부풀리다</sub>  
✍️ 

### 문단 3

**⑦** 셋째, 평가한 모델이 여섯 개뿐이어서 순위 상관 분석의 정밀도가 낮고, 일반 성능과 분야 특화 성능의 관계에 대해 확고한 결론을 내릴 수 없다.  
<sub>힌트 (27단어): precision 정밀도 · preclude 불가능하게 하다</sub>  
✍️ 

**⑧** 모델 선택은 로컬 하드웨어에서 실행되어야 한다는 요건에 따라 제한되었으며, 더 큰 모델에서는 다른 양상이 나타날 수 있다.  
<sub>힌트 (22단어): constrain 제약하다</sub>  
✍️ 

**⑨** 마지막으로, 검색 지표는 생성된 답변 품질의 대리 지표일 뿐이다.  
<sub>힌트 (11단어): metric 지표 · proxy 대리 지표</sub>  
✍️ 

**⑩** 종단 간 RAG 성능은 평가하지 않았으며, nDCG@10이 개선된다고 답변이 그만큼 좋아지지는 않을 수 있다.  
<sub>힌트 (18단어): end-to-end 종단 간의 · translate into ~로 이어지다 · proportionally 비례하여</sub>  
✍️ 

### 문단 4

**⑪** 이런 한계는 후속 연구의 몇 가지 방향을 시사한다.  
<sub>힌트 (8단어): direction 방향</sub>  
✍️ 

**⑫** 실제 사용 중에 실무자의 질의를 수집하면, 현실적인 질의 변동에 대해 모델이 얼마나 강건한지 평가할 수 있을 것이다.  
<sub>힌트 (17단어): assessment 평가 · robustness 강건성 · variation 변동</sub>  
✍️ 

**⑬** 평가한 모델들이 출시된 이후에 발표된 문서를 포함하면 오염 여부를 부분적으로 점검할 수 있을 것이다.  
<sub>힌트 (17단어): release 출시</sub>  
✍️ 

**⑭** 후속 연구는 어휘 기반 방법과 밀집 방법을 결합한 혼합 검색이나 경량 분야 적응이 여기서 관찰한 교차 언어 격차를 좁힐 수 있는지 살펴보고, 전문가 채점으로 답변 품질을 직접 평가해야 한다.  
<sub>힌트 (33단어): hybrid retrieval 혼합 검색 · dense 밀집의 · lightweight 경량의 · narrow 좁히다 · grading 채점</sub>  
✍️ 

### 문단 5

**⑮** 이런 한계에도 불구하고, 이 연구는 일반 벤치마크 순위가 이중 언어 기술 문서 검색용 모델을 고르는 데 믿을 만한 지침이 되지 못하며, 특히 교차 언어 성능은 모델을 배포하기 전에 직접 측정해야 함을 보여 준다.  
<sub>힌트 (36단어): demonstrate 보여 주다 · unreliable 신뢰할 수 없는</sub>  
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

should be acknowledged (인정되어야 한다) · preclude (불가능하게 하다) · ambiguous (모호한) · translate into (~로 이어지다) · overestimate (과대평가하다) · proportionally (비례하여) · cannot exclude the possibility (가능성을 배제할 수 없다) · would allow (가능하게 할 것이다) · make it unlikely that (~할 가능성을 낮추다) · narrow the gap (격차를 좁히다) · inflate (부풀리다) · despite these limitations (이 한계들에도 불구하고)

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
| ⑭ | | | | | | | |
| ⑮ | | | | | | | |

**1차 합계:** ____ / 45점  ·  **가장 많은 오류 코드:** ____

---

## Part D. 정답과 섀도잉 스크립트 (풀이 후 확인)

> 끊어 읽기 표시( / )는 1회차 청크 경계입니다. 섀도잉은 음성 없이 시작해도 됩니다. 먼저 끊어 읽기 단위로 소리 내어 읽고, 익숙해지면 표시를 무시하고 한 호흡에 읽으세요.

### 문단 1

**①** Several limitations of this study should be acknowledged.  
<sub>↳ Several limitations / of this study / should be acknowledged.</sub>

**②** First, the benchmark was constructed from a single collection of documents in one domain, and its queries were written by two experts rather than collected from actual users.  
<sub>↳ First, / the benchmark / was constructed / from a single collection / of documents / in one domain, / and its queries / were written / by two experts / rather than collected / from actual users.</sub>

**③** Expert-written queries tend to be well formed and terminologically precise, whereas real users often pose short, ambiguous, or misspelled queries; the reported scores may therefore overestimate performance in deployment.  
<sub>↳ Expert-written queries / tend to be / well formed / and terminologically precise, / whereas real users / often pose / short, ambiguous, / or misspelled queries; / the reported scores / may therefore overestimate / performance / in deployment.</sub>

**④** In addition, the corpus consisted of formal regulatory text; performance on informal material such as internal memos or operating logs may differ.  
<sub>↳ In addition, / the corpus / consisted of / formal regulatory text; / performance / on informal material / such as internal memos / or operating logs / may differ.</sub>

### 문단 2

**⑤** Second, because the pretraining corpora of the evaluated models are not fully documented, we cannot exclude the possibility that some source documents were included in training data.  
<sub>↳ Second, / because the pretraining corpora / of the evaluated models / are not fully documented, / we cannot exclude / the possibility / that some source documents / were included / in training data.</sub>

**⑥** Although the parallel design makes it unlikely that contamination would affect all models equally, such exposure could have inflated the scores of particular models.  
<sub>↳ Although / the parallel design / makes it unlikely / that contamination / would affect / all models equally, / such exposure / could have inflated / the scores / of particular models.</sub>

### 문단 3

**⑦** Third, only six models were evaluated, which limits the precision of the rank correlation analysis and precludes firm conclusions about the relationship between general and domain-specific performance.  
<sub>↳ Third, / only six models / were evaluated, / which limits / the precision / of the rank correlation analysis / and precludes / firm conclusions / about the relationship / between general / and domain-specific performance.</sub>

**⑧** The selection was constrained by the requirement that each model run on local hardware, and larger models might show a different pattern.  
<sub>↳ The selection / was constrained / by the requirement / that each model / run on local hardware, / and larger models / might show / a different pattern.</sub>

**⑨** Finally, retrieval metrics are proxies for the quality of generated answers.  
<sub>↳ Finally, / retrieval metrics / are proxies / for the quality / of generated answers.</sub>

**⑩** We did not evaluate end-to-end RAG performance, and improvements in nDCG@10 may not translate proportionally into better answers.  
<sub>↳ We did not evaluate / end-to-end / RAG performance, / and improvements / in nDCG@10 / may not translate / proportionally / into better answers.</sub>

### 문단 4

**⑪** These limitations suggest several directions for future work.  
<sub>↳ These limitations / suggest / several directions / for future work.</sub>

**⑫** Collecting queries from practitioners during actual use would allow an assessment of robustness to realistic query variation.  
<sub>↳ Collecting queries / from practitioners / during actual use / would allow / an assessment / of robustness / to realistic query variation.</sub>

**⑬** Including documents published after the release of the evaluated models would provide a partial check against contamination.  
<sub>↳ Including documents / published / after the release / of the evaluated models / would provide / a partial check / against contamination.</sub>

**⑭** Future studies should also examine whether hybrid retrieval, combining lexical and dense methods, or lightweight domain adaptation can narrow the cross-lingual gap observed here, and should evaluate answer quality directly through expert grading.  
<sub>↳ Future studies / should also examine / whether hybrid retrieval, / combining lexical / and dense methods, / or lightweight / domain adaptation / can narrow / the cross-lingual gap / observed here, / and should evaluate / answer quality directly / through expert grading.</sub>

### 문단 5

**⑮** Despite these limitations, the study demonstrates that general benchmark rankings are an unreliable guide to model selection for bilingual technical retrieval, and that cross-lingual performance in particular should be measured directly before a model is deployed.  
<sub>↳ Despite these limitations, / the study demonstrates / that general benchmark rankings / are an unreliable guide / to model selection / for bilingual / technical retrieval, / and that cross-lingual performance / in particular / should be measured directly / before a model / is deployed.</sub>

---

*원본 에세이: D12_Limitations_and_Future_Work.md · 이 워크북은 원본의 2회차 번역과 1회차 청크에서 자동 생성되었습니다.*
