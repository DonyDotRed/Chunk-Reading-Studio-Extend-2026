# D06. Designing a Retrieval Evaluation Protocol
### 검색 평가 프로토콜 설계 (방법: 벤치마크 구축과 평가 절차)

| 항목 | 내용 |
|---|---|
| 시리즈 | Domain Track · Unit B 방법 (6/18) · 분야: ML·LLM 평가 |
| 수준 | 대학원·연구자 · CEFR C1–C2 |
| 분량 | 약 350단어 · 6문단 · 16문장 |
| 문체 | 연구 논문 방법 절 (가상 연구, D03의 후속, 컴퓨터과학 관례) |
| 핵심 문법 | 재현 가능성을 위한 세부 기술 (버전, 접두어, 정규화, 정확 탐색), 주석자 간 신뢰도 보고, 지표와 통계 검정 기술, 한계의 선제적 언급 |
| 미리보기 | 부트스트랩 신뢰구간과 순위 상관의 보고 (D09) |

---

## 학습 방법

| 단계 | 할 일 | 권장 횟수 |
|---|---|---|
| 1회차 | 청크 단위 직독직해. 청크마다 끊어 소리 내어 읽고 바로 한국어 뜻을 떠올린다 | 3회 |
| 2회차 | 문장 단위 직독직해. 한 문장을 한 호흡으로 읽고 의미를 확인한다 | 3회 |
| 3회차 | 원문만 보고 처음부터 끝까지 낭독한다. 시간을 재서 기록한다 | 3회 이상 |

낭독 속도는 분당 단어 수(WPM)로 기록합니다. 350단어를 3분에 읽으면 약 117 WPM입니다. 회독이 거듭될수록 속도가 오르고 끊기는 지점이 줄어드는지 확인하세요.

---

## 0. 원문 (Full Text)

> **Corpus**
>
> The retrieval corpus was constructed from a set of radiation protection documents available in parallel English and Korean versions. Each document was segmented into passages of approximately 200 to 300 tokens at paragraph boundaries, and English and Korean passages were aligned manually so that each English passage had a corresponding Korean passage covering the same content. The final corpus contained 2,400 aligned passage pairs.
>
> **Queries and relevance judgments**
>
> Two subject-matter experts independently wrote 300 queries in Korean, each targeting information contained in one or more passages; English versions were then produced by professional translation and reviewed for terminological accuracy. To reduce lexical overlap with the target passages, experts were instructed to formulate queries as practitioners would ask them rather than by copying passage wording. Relevance was judged on a three-point scale (0, not relevant; 1, partially relevant; 2, highly relevant). Inter-annotator agreement, measured on a random subset of 60 queries, was substantial (weighted Cohen's kappa = 0.78), and disagreements were resolved by discussion.
>
> **Models and retrieval setup**
>
> Several publicly available multilingual embedding models with fewer than 600 million parameters were evaluated without fine-tuning. For each model, passages and queries were encoded with the model's recommended prefixes and maximum sequence length, embeddings were L2-normalized, and retrieval was performed by exact cosine-similarity search over the full corpus. Model versions were fixed by recording repository commit identifiers.
>
> **Evaluation conditions and metrics**
>
> Each model was evaluated under four conditions: Korean queries against Korean passages, English against English, Korean against English, and English against Korean. Performance was measured using Recall@k for k = 1, 5, and 10, mean reciprocal rank at 10 (MRR@10), and normalized discounted cumulative gain at 10 (nDCG@10), with nDCG computed from graded relevance judgments.
>
> **Statistical analysis**
>
> Differences between models were assessed using paired bootstrap resampling over queries with 10,000 resamples, yielding 95 percent confidence intervals for each pairwise difference. P values were adjusted for multiple comparisons using the Holm procedure. Agreement between rankings on the domain benchmark and on a general benchmark was quantified with Kendall's tau.
>
> **Contamination**
>
> Because the pretraining data of the evaluated models are not fully disclosed, contamination by the source documents cannot be excluded; this possibility is examined further in the Discussion.

---

## 1회차 · 청크 단위 직독직해

> 영어 어순 그대로 앞에서부터 의미를 받아들이는 것이 목표입니다. 한국어 번역도 영어 순서를 따릅니다.

### 문단 1 · Corpus

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| The retrieval corpus | 검색 말뭉치는 | corpus 말뭉치 |
| was constructed | 구축되었다 | construct 구축하다 |
| from a set | 한 세트로부터 |  |
| of radiation protection documents | 방사선 방호 문서들의 |  |
| available | 이용 가능한 |  |
| in parallel English | 영어와 |  |
| and Korean versions. | 한국어 병렬판으로. | parallel 병렬의 |
| Each document | 각 문서는 |  |
| was segmented | 분할되었다 | segment 분할하다 |
| into passages | 구절들로 | passage 구절 |
| of approximately | 대략 |  |
| 200 to 300 tokens | 200–300 토큰의 | token 토큰 |
| at paragraph boundaries, | 문단 경계에서, | boundary 경계 |
| and English and Korean passages | 그리고 영어와 한국어 구절은 |  |
| were aligned manually | 수작업으로 정렬되었다 | align 정렬하다 · manually 수작업으로 |
| so that | ~하도록 |  |
| each English passage | 각 영어 구절이 |  |
| had a corresponding | 대응하는 | corresponding 대응하는 |
| Korean passage | 한국어 구절을 가지도록 |  |
| covering the same content. | 같은 내용을 담은. |  |
| The final corpus | 최종 말뭉치는 |  |
| contained | 포함했다 |  |
| 2,400 aligned passage pairs. | 2,400개의 정렬된 구절 쌍을. | pair 쌍 |

### 문단 2 · Queries and relevance judgments

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Two subject-matter experts | 두 명의 분야 전문가가 | subject-matter expert 분야 전문가 |
| independently wrote | 독립적으로 작성했다 | independently 독립적으로 |
| 300 queries in Korean, | 한국어 질의 300개를, | query 질의 |
| each targeting information | 각각 정보를 겨냥한 | target 겨냥하다 |
| contained | 담긴 |  |
| in one or more passages; | 하나 이상의 구절에; |  |
| English versions | 영어판은 |  |
| were then produced | 그다음 만들어졌고 |  |
| by professional translation | 전문 번역으로 | professional 전문적인 |
| and reviewed | 그리고 검토되었다 | review 검토하다 |
| for terminological accuracy. | 용어의 정확성에 대해. | terminological 용어상의 · accuracy 정확성 |
| To reduce | 줄이기 위해 | reduce 줄이다 |
| lexical overlap | 어휘 중복을 | lexical 어휘의 · overlap 중복 |
| with the target passages, | 대상 구절과의, |  |
| experts were instructed | 전문가들은 지시받았다 | instruct 지시하다 |
| to formulate queries | 질의를 작성하도록 | formulate 작성하다, 구성하다 |
| as practitioners | 실무자들이 | practitioner 실무자 |
| would ask them | 물을 법한 방식으로 |  |
| rather than | ~가 아니라 |  |
| by copying | 베끼는 방식으로 |  |
| passage wording. | 구절의 표현을. | wording 표현 |
| Relevance | 적합성은 | relevance 적합성 |
| was judged | 판정되었다 | judge 판정하다 |
| on a three-point scale | 3점 척도로 | scale 척도 |
| (0, not relevant; | (0, 무관; |  |
| 1, partially relevant; | 1, 부분 적합; | partially 부분적으로 |
| 2, highly relevant). | 2, 높은 적합). |  |
| Inter-annotator agreement, | 주석자 간 일치도는, | inter-annotator 주석자 간 · agreement 일치도 |
| measured | 측정된 | measure 측정하다 |
| on a random subset | 무작위 부분 집합에서 | random 무작위의 · subset 부분 집합 |
| of 60 queries, | 60개 질의의, |  |
| was substantial | 상당했으며 | substantial 상당한 |
| (weighted Cohen's kappa = 0.78), | (가중 코헨 카파 = 0.78), |  |
| and disagreements | 그리고 불일치는 | disagreement 불일치 |
| were resolved | 해소되었다 | resolve 해소하다 |
| by discussion. | 논의를 통해. |  |

### 문단 3 · Models and retrieval setup

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Several publicly available | 공개적으로 이용 가능한 여러 | publicly 공개적으로 |
| multilingual embedding models | 다국어 임베딩 모델이 | multilingual 다국어의 |
| with fewer than | ~보다 적은 |  |
| 600 million parameters | 6억 개의 매개변수를 가진 | parameter 매개변수 |
| were evaluated | 평가되었다 |  |
| without fine-tuning. | 미세 조정 없이. | fine-tuning 미세 조정 |
| For each model, | 각 모델에 대해, |  |
| passages and queries | 구절과 질의는 |  |
| were encoded | 인코딩되었고 | encode 인코딩하다 |
| with the model's | 그 모델의 |  |
| recommended prefixes | 권장 접두어와 | prefix 접두어 |
| and maximum sequence length, | 최대 시퀀스 길이로, | sequence length 시퀀스 길이 |
| embeddings | 임베딩은 |  |
| were L2-normalized, | L2 정규화되었으며, | normalize 정규화하다 |
| and retrieval | 그리고 검색은 |  |
| was performed | 수행되었다 |  |
| by exact | 정확한 | exact 정확한 |
| cosine-similarity search | 코사인 유사도 탐색으로 | cosine similarity 코사인 유사도 |
| over the full corpus. | 전체 말뭉치에 대해. |  |
| Model versions | 모델 버전은 |  |
| were fixed | 고정되었다 | fix 고정하다 |
| by recording | 기록함으로써 | record 기록하다 |
| repository commit identifiers. | 저장소 커밋 식별자를. | repository 저장소 · identifier 식별자 |

### 문단 4 · Evaluation conditions and metrics

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Each model | 각 모델은 |  |
| was evaluated | 평가되었다 |  |
| under four conditions: | 네 가지 조건에서: | condition 조건 |
| Korean queries | 한국어 질의 대 |  |
| against Korean passages, | 한국어 구절, |  |
| English against English, | 영어 대 영어, |  |
| Korean against English, | 한국어 대 영어, |  |
| and English against Korean. | 그리고 영어 대 한국어. |  |
| Performance | 성능은 | performance 성능 |
| was measured | 측정되었다 |  |
| using Recall@k | Recall@k를 사용하여 | recall 재현율 |
| for k = 1, 5, and 10, | k = 1, 5, 10에 대해, |  |
| mean reciprocal rank | 평균 역순위 | reciprocal rank 역순위 |
| at 10 (MRR@10), | 10에서의 (MRR@10), |  |
| and normalized discounted | 그리고 정규화 할인 | normalized 정규화된 |
| cumulative gain at 10 | 10에서의 누적 이득 | cumulative gain 누적 이득 |
| (nDCG@10), | (nDCG@10), |  |
| with nDCG | nDCG는 |  |
| computed | 계산되면서 | compute 계산하다 |
| from graded | 등급화된 | graded 등급화된 |
| relevance judgments. | 적합성 판정으로부터. | judgment 판정 |

### 문단 5 · Statistical analysis

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Differences | 차이는 |  |
| between models | 모델 간의 |  |
| were assessed | 평가되었다 | assess 평가하다 |
| using paired | 짝지은 | paired 짝지은 |
| bootstrap resampling | 부트스트랩 재표집을 사용하여 | bootstrap 부트스트랩 · resampling 재표집 |
| over queries | 질의 단위의 |  |
| with 10,000 resamples, | 10,000회 재표집으로, |  |
| yielding | 산출하면서 | yield 산출하다 |
| 95 percent | 95% |  |
| confidence intervals | 신뢰구간을 | confidence interval 신뢰구간 |
| for each pairwise difference. | 각 쌍별 차이에 대한. | pairwise 쌍별의 |
| P values | P 값은 |  |
| were adjusted | 조정되었다 | adjust 조정하다 |
| for multiple comparisons | 다중 비교에 대해 | multiple comparisons 다중 비교 |
| using the Holm procedure. | 홈 절차를 사용하여. | procedure 절차 |
| Agreement | 일치는 |  |
| between rankings | 순위 간의 | ranking 순위 |
| on the domain benchmark | 분야 벤치마크에서의 |  |
| and on a general benchmark | 그리고 일반 벤치마크에서의 |  |
| was quantified | 정량화되었다 | quantify 정량화하다 |
| with Kendall's tau. | 켄달의 타우로. |  |

### 문단 6 · Contamination

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Because the pretraining data | 사전 학습 데이터가 ~하기 때문에 | pretraining 사전 학습 |
| of the evaluated models | 평가된 모델들의 |  |
| are not fully disclosed, | 완전히 공개되지 않았기 때문에, | disclose 공개하다 |
| contamination | 오염은 | contamination 오염 |
| by the source documents | 원문 문서에 의한 |  |
| cannot be excluded; | 배제될 수 없다; | exclude 배제하다 |
| this possibility | 이 가능성은 |  |
| is examined further | 더 검토된다 |  |
| in the Discussion. | 논의 절에서. |  |

---

## 2회차 · 문장 단위 직독직해

> 한 문장을 한 호흡에 읽는 연습입니다. 1회차에서 끊었던 지점을 의식하되, 멈추지 않고 이어 읽습니다.

### 문단 1 · Corpus

**① The retrieval corpus was constructed from a set of radiation protection documents available in parallel English and Korean versions.**
검색 말뭉치는 영어와 한국어 병렬판이 있는 방사선 방호 문서들로 구축했다.
어휘: corpus 말뭉치 · construct 구축하다 · parallel 병렬의

**② Each document was segmented into passages of approximately 200 to 300 tokens at paragraph boundaries, and English and Korean passages were aligned manually so that each English passage had a corresponding Korean passage covering the same content.**
각 문서는 문단 경계에서 약 200–300 토큰 길이의 구절로 나누었고, 영어 구절마다 같은 내용을 담은 한국어 구절이 대응하도록 수작업으로 정렬했다.
어휘: segment 분할하다 · passage 구절 · token 토큰 · boundary 경계 · align 정렬하다 · manually 수작업으로 · corresponding 대응하는

**③ The final corpus contained 2,400 aligned passage pairs.**
최종 말뭉치에는 정렬된 구절 쌍 2,400개가 들어 있었다.
어휘: pair 쌍

### 문단 2 · Queries and relevance judgments

**④ Two subject-matter experts independently wrote 300 queries in Korean, each targeting information contained in one or more passages; English versions were then produced by professional translation and reviewed for terminological accuracy.**
분야 전문가 두 명이 하나 이상의 구절에 담긴 정보를 겨냥해 한국어 질의 300개를 각자 작성했고, 영어판은 전문 번역 후 용어 정확성을 검토했다.
어휘: subject-matter expert 분야 전문가 · independently 독립적으로 · query 질의 · target 겨냥하다 · professional 전문적인 · review 검토하다 · terminological 용어상의 · accuracy 정확성

**⑤ To reduce lexical overlap with the target passages, experts were instructed to formulate queries as practitioners would ask them rather than by copying passage wording.**
대상 구절과의 어휘 중복을 줄이기 위해, 전문가들에게는 구절의 표현을 그대로 옮기지 말고 실무자가 실제로 물을 법한 방식으로 질의를 쓰도록 했다.
어휘: reduce 줄이다 · lexical 어휘의 · overlap 중복 · instruct 지시하다 · formulate 작성하다, 구성하다 · practitioner 실무자 · wording 표현

**⑥ Relevance was judged on a three-point scale (0, not relevant; 1, partially relevant; 2, highly relevant).**
적합성은 3점 척도(0 무관, 1 부분 적합, 2 높은 적합)로 판정했다.
어휘: relevance 적합성 · judge 판정하다 · scale 척도 · partially 부분적으로

**⑦ Inter-annotator agreement, measured on a random subset of 60 queries, was substantial (weighted Cohen's kappa = 0.78), and disagreements were resolved by discussion.**
무작위로 고른 질의 60개에서 측정한 주석자 간 일치도는 상당한 수준이었고(가중 코헨 카파 0.78), 불일치는 논의로 해소했다.
어휘: inter-annotator 주석자 간 · agreement 일치도 · measure 측정하다 · random 무작위의 · subset 부분 집합 · substantial 상당한 · disagreement 불일치 · resolve 해소하다

### 문단 3 · Models and retrieval setup

**⑧ Several publicly available multilingual embedding models with fewer than 600 million parameters were evaluated without fine-tuning.**
매개변수 6억 개 미만의 공개 다국어 임베딩 모델 여러 개를 미세 조정 없이 평가했다.
어휘: publicly 공개적으로 · multilingual 다국어의 · parameter 매개변수 · fine-tuning 미세 조정

**⑨ For each model, passages and queries were encoded with the model's recommended prefixes and maximum sequence length, embeddings were L2-normalized, and retrieval was performed by exact cosine-similarity search over the full corpus.**
각 모델에서 구절과 질의는 해당 모델의 권장 접두어와 최대 시퀀스 길이로 인코딩했고, 임베딩은 L2 정규화했으며, 검색은 전체 말뭉치에 대한 정확한 코사인 유사도 탐색으로 수행했다.
어휘: encode 인코딩하다 · prefix 접두어 · sequence length 시퀀스 길이 · normalize 정규화하다 · exact 정확한 · cosine similarity 코사인 유사도

**⑩ Model versions were fixed by recording repository commit identifiers.**
모델 버전은 저장소 커밋 식별자를 기록해 고정했다.
어휘: fix 고정하다 · record 기록하다 · repository 저장소 · identifier 식별자

### 문단 4 · Evaluation conditions and metrics

**⑪ Each model was evaluated under four conditions: Korean queries against Korean passages, English against English, Korean against English, and English against Korean.**
각 모델은 한국어 질의–한국어 구절, 영어–영어, 한국어–영어, 영어–한국어의 네 조건에서 평가했다.
어휘: condition 조건

**⑫ Performance was measured using Recall@k for k = 1, 5, and 10, mean reciprocal rank at 10 (MRR@10), and normalized discounted cumulative gain at 10 (nDCG@10), with nDCG computed from graded relevance judgments.**
성능은 k = 1, 5, 10에서의 Recall@k, MRR@10, nDCG@10으로 측정했으며, nDCG는 등급화된 적합성 판정으로 계산했다.
어휘: performance 성능 · recall 재현율 · reciprocal rank 역순위 · normalized 정규화된 · cumulative gain 누적 이득 · compute 계산하다 · graded 등급화된 · judgment 판정

### 문단 5 · Statistical analysis

**⑬ Differences between models were assessed using paired bootstrap resampling over queries with 10,000 resamples, yielding 95 percent confidence intervals for each pairwise difference.**
모델 간 차이는 질의 단위의 짝지은 부트스트랩 재표집(10,000회)으로 평가해 각 쌍별 차이의 95% 신뢰구간을 구했다.
어휘: assess 평가하다 · paired 짝지은 · bootstrap 부트스트랩 · resampling 재표집 · yield 산출하다 · confidence interval 신뢰구간 · pairwise 쌍별의

**⑭ P values were adjusted for multiple comparisons using the Holm procedure.**
P 값은 홈(Holm) 절차로 다중 비교를 보정했다.
어휘: adjust 조정하다 · multiple comparisons 다중 비교 · procedure 절차

**⑮ Agreement between rankings on the domain benchmark and on a general benchmark was quantified with Kendall's tau.**
분야 벤치마크 순위와 일반 벤치마크 순위의 일치 정도는 켄달 타우로 정량화했다.
어휘: ranking 순위 · quantify 정량화하다

### 문단 6 · Contamination

**⑯ Because the pretraining data of the evaluated models are not fully disclosed, contamination by the source documents cannot be excluded; this possibility is examined further in the Discussion.**
평가한 모델들의 사전 학습 데이터가 완전히 공개되지 않았으므로 원문 문서에 의한 오염 가능성을 배제할 수 없으며, 이 가능성은 논의 절에서 더 검토한다.
어휘: pretraining 사전 학습 · disclose 공개하다 · contamination 오염 · exclude 배제하다

---

## 참고 문헌

Järvelin, K., & Kekäläinen, J. (2002). Cumulated gain-based evaluation of IR techniques. *ACM Transactions on Information Systems, 20*(4), 422–446.

Holm, S. (1979). A simple sequentially rejective multiple test procedure. *Scandinavian Journal of Statistics, 6*(2), 65–70.

Efron, B., & Tibshirani, R. J. (1993). *An introduction to the bootstrap*. Chapman & Hall.

**가상 연구에 대한 주석.** D03 서론에 이어지는 가상 연구의 방법 절입니다. 말뭉치 규모(2,400쌍), 질의 수(300개), 카파 값(0.78), 매개변수 상한(6억 개)은 예시로 설정한 값입니다. nDCG의 정의는 Järvelin & Kekäläinen(2002)을, 다중 비교 보정은 Holm(1979)을 따랐습니다. 가중 카파 0.78을 "substantial"로 표현한 것은 Landis & Koch의 관례적 구간 해석(0.61–0.80)에 따른 것인데, 이 구간은 임의적이라는 비판도 있으므로 실제 원고에서는 수치를 함께 보고하는 것이 좋습니다.

## 학술 영어 포인트

### 1. 재현 가능성을 위한 세부 기술

컴퓨터과학 방법 절의 핵심은 **다른 연구자가 같은 결과를 다시 얻을 수 있는가**입니다.

| 재현 요소 | 이 글의 기술 | 빠뜨리면 생기는 문제 |
|---|---|---|
| 데이터 분할 | segmented into passages of approximately 200 to 300 tokens at paragraph boundaries | 구절 길이가 다르면 검색 난이도가 달라짐 |
| 모델 입력 형식 | encoded with the model's recommended prefixes and maximum sequence length | 접두어 누락 시 일부 모델 성능이 크게 하락 |
| 유사도 계산 | L2-normalized… exact cosine-similarity search | 근사 탐색이면 결과에 탐색 오차가 섞임 |
| 버전 고정 | recording repository commit identifiers | 모델 업데이트로 결과가 바뀜 |
| 미세 조정 여부 | evaluated without fine-tuning | 비교 조건 불명확 |

### 2. 누수(leakage)와 오염(contamination)을 다루는 두 가지 방식

| 방식 | 이 글의 예 |
|---|---|
| **설계로 줄이기** | To reduce lexical overlap with the target passages, experts were instructed to formulate queries as practitioners would ask them rather than by copying passage wording. |
| **배제할 수 없음을 인정하고 논의로 넘기기** | Because the pretraining data… are not fully disclosed, contamination… **cannot be excluded; this possibility is examined further in the Discussion.** |

통제할 수 있는 것은 방법으로 통제하고, 통제할 수 없는 것은 방법 절에서 미리 밝혀 두는 것이 정직한 서술입니다. 심사자가 지적하기 전에 먼저 말하면 신뢰도가 올라갑니다.

### 3. 신뢰도·통계 보고의 표준 표현

| 항목 | 표현 |
|---|---|
| 주석자 간 신뢰도 | Inter-annotator agreement, measured on a random subset of 60 queries, was substantial (weighted Cohen's kappa = 0.78) |
| 불일치 처리 | disagreements were resolved by discussion |
| 차이 검정 | paired bootstrap resampling over queries with 10,000 resamples, yielding 95% confidence intervals |
| 다중 비교 | P values were adjusted for multiple comparisons using the Holm procedure |
| 순위 일치 | quantified with Kendall's tau |

**"over queries"에 주목하세요.** 부트스트랩의 재표집 단위가 질의라는 뜻입니다. 재표집 단위를 밝히지 않으면 신뢰구간의 의미가 모호해집니다.

### 4. 분야 어휘

| 영어 | 한국어 | 영어 | 한국어 |
|---|---|---|---|
| segment into passages | 구절로 분할하다 | L2-normalized | L2 정규화된 |
| align | 정렬하다 | exact search | 정확 탐색 |
| lexical overlap | 어휘 중복 | mean reciprocal rank | 평균 역순위 |
| relevance judgment | 적합성 판정 | graded relevance | 등급화된 적합성 |
| inter-annotator agreement | 주석자 간 일치도 | paired bootstrap | 짝지은 부트스트랩 |
| recommended prefix | 권장 접두어 | contamination | (평가 데이터) 오염 |

## 핵심 어휘 정리 (Domain Track 어휘장 D06)

| 어휘 | 뜻 | 어휘 | 뜻 |
|---|---|---|---|
| corresponding | 대응하는 | substantial | 상당한 |
| terminological accuracy | 용어 정확성 | resolve by discussion | 논의로 해소하다 |
| formulate | 작성하다 | quantify | 정량화하다 |
| practitioner | 실무자 | pairwise | 쌍별의 |
| wording | 표현 | disclose | 공개하다 |
| subset | 부분 집합 | cannot be excluded | 배제할 수 없다 |

---

## 낭독 기록표

| 회차 | 날짜 | 소요 시간 | WPM (350 ÷ 분) | 막힌 문장 번호 |
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

*Original essay written for the 30-part reading series. Next: D07. Reporting Doses Near Detection Limits (결과: 불확도와 검출 한계)*
