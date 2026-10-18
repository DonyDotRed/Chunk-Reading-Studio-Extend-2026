# 역번역 워크북 · D06. Designing a Retrieval Evaluation Protocol
### 검색 평가 프로토콜 설계 (방법: 벤치마크 구축과 평가 절차)

| 항목 | 내용 |
|---|---|
| 원본 | D06_Designing_a_Retrieval_Evaluation_Protocol.md |
| 트랙 | Domain Track (C1–C2) |
| 문장 수 / 단어 수 | 16문장 / 약 350단어 |
| 집중 포인트 | 재현 가능성을 위한 세부 기술 (버전, 접두어, 정규화, 정확 탐색), 주석자 간 신뢰도 보고, 지표와 통계 검정 기술, 한계의 선제적 언급 |
| 권장 소요 시간 | 1차 풀이 약 29분 (채점·섀도잉 별도) |

## 진행 순서

1. **Part A** 한국어 문장을 보고 영어로 씁니다. 처음에는 힌트를 보며 풀고, 복습 때는 힌트를 가리고 풉니다.
2. **Part D** 정답과 비교해 **Part C**에 점수(0–3)와 오류 유형 코드를 적습니다. 채점 기준은 `00W_Backtranslation_Guide.md`에 있습니다.
3. **Part D**의 끊어 읽기 스크립트로 정답 문장을 섀도잉합니다.
4. **Part B** 리텔링을 원문을 보지 않고 수행합니다.
5. 1일·3일·7일·21일 뒤에 2점 이하 문장만 다시 풉니다.

> 한국어 번역은 직역이 아니라 자연스러운 의역입니다. 정답과 문장 구조가 달라도 의미와 핵심 어휘가 맞으면 높은 점수를 주세요.

---

## Part A. 역번역 문제

### 문단 1 · Corpus

**①** 검색 말뭉치는 영어와 한국어 병렬판이 있는 방사선 방호 문서들로 구축했다.  
<sub>힌트 (19단어): corpus 말뭉치 · construct 구축하다 · parallel 병렬의</sub>  
✍️ 

**②** 각 문서는 문단 경계에서 약 200–300 토큰 길이의 구절로 나누었고, 영어 구절마다 같은 내용을 담은 한국어 구절이 대응하도록 수작업으로 정렬했다.  
<sub>힌트 (37단어): segment 분할하다 · passage 구절 · token 토큰 · boundary 경계 · align 정렬하다 · manually 수작업으로 · corresponding 대응하는</sub>  
✍️ 

**③** 최종 말뭉치에는 정렬된 구절 쌍 2,400개가 들어 있었다.  
<sub>힌트 (8단어): pair 쌍</sub>  
✍️ 

### 문단 2 · Queries and relevance judgments

**④** 분야 전문가 두 명이 하나 이상의 구절에 담긴 정보를 겨냥해 한국어 질의 300개를 각자 작성했고, 영어판은 전문 번역 후 용어 정확성을 검토했다.  
<sub>힌트 (31단어): subject-matter expert 분야 전문가 · independently 독립적으로 · query 질의 · target 겨냥하다 · professional 전문적인 · review 검토하다 · terminological 용어상의 · accuracy 정확성</sub>  
✍️ 

**⑤** 대상 구절과의 어휘 중복을 줄이기 위해, 전문가들에게는 구절의 표현을 그대로 옮기지 말고 실무자가 실제로 물을 법한 방식으로 질의를 쓰도록 했다.  
<sub>힌트 (25단어): reduce 줄이다 · lexical 어휘의 · overlap 중복 · instruct 지시하다 · formulate 작성하다, 구성하다 · practitioner 실무자 · wording 표현</sub>  
✍️ 

**⑥** 적합성은 3점 척도(0 무관, 1 부분 적합, 2 높은 적합)로 판정했다.  
<sub>힌트 (16단어): relevance 적합성 · judge 판정하다 · scale 척도 · partially 부분적으로</sub>  
✍️ 

**⑦** 무작위로 고른 질의 60개에서 측정한 주석자 간 일치도는 상당한 수준이었고(가중 코헨 카파 0.78), 불일치는 논의로 해소했다.  
<sub>힌트 (23단어): inter-annotator 주석자 간 · agreement 일치도 · measure 측정하다 · random 무작위의 · subset 부분 집합 · substantial 상당한 · disagreement 불일치 · resolve 해소하다</sub>  
✍️ 

### 문단 3 · Models and retrieval setup

**⑧** 매개변수 6억 개 미만의 공개 다국어 임베딩 모델 여러 개를 미세 조정 없이 평가했다.  
<sub>힌트 (16단어): publicly 공개적으로 · multilingual 다국어의 · parameter 매개변수 · fine-tuning 미세 조정</sub>  
✍️ 

**⑨** 각 모델에서 구절과 질의는 해당 모델의 권장 접두어와 최대 시퀀스 길이로 인코딩했고, 임베딩은 L2 정규화했으며, 검색은 전체 말뭉치에 대한 정확한 코사인 유사도 탐색으로 수행했다.  
<sub>힌트 (32단어): encode 인코딩하다 · prefix 접두어 · sequence length 시퀀스 길이 · normalize 정규화하다 · exact 정확한 · cosine similarity 코사인 유사도</sub>  
✍️ 

**⑩** 모델 버전은 저장소 커밋 식별자를 기록해 고정했다.  
<sub>힌트 (9단어): fix 고정하다 · record 기록하다 · repository 저장소 · identifier 식별자</sub>  
✍️ 

### 문단 4 · Evaluation conditions and metrics

**⑪** 각 모델은 한국어 질의–한국어 구절, 영어–영어, 한국어–영어, 영어–한국어의 네 조건에서 평가했다.  
<sub>힌트 (22단어): condition 조건</sub>  
✍️ 

**⑫** 성능은 k = 1, 5, 10에서의 Recall@k, MRR@10, nDCG@10으로 측정했으며, nDCG는 등급화된 적합성 판정으로 계산했다.  
<sub>힌트 (33단어): performance 성능 · recall 재현율 · reciprocal rank 역순위 · normalized 정규화된 · cumulative gain 누적 이득 · compute 계산하다 · graded 등급화된 · judgment 판정</sub>  
✍️ 

### 문단 5 · Statistical analysis

**⑬** 모델 간 차이는 질의 단위의 짝지은 부트스트랩 재표집(10,000회)으로 평가해 각 쌍별 차이의 95% 신뢰구간을 구했다.  
<sub>힌트 (23단어): assess 평가하다 · paired 짝지은 · bootstrap 부트스트랩 · resampling 재표집 · yield 산출하다 · confidence interval 신뢰구간 · pairwise 쌍별의</sub>  
✍️ 

**⑭** P 값은 홈(Holm) 절차로 다중 비교를 보정했다.  
<sub>힌트 (11단어): adjust 조정하다 · multiple comparisons 다중 비교 · procedure 절차</sub>  
✍️ 

**⑮** 분야 벤치마크 순위와 일반 벤치마크 순위의 일치 정도는 켄달 타우로 정량화했다.  
<sub>힌트 (17단어): ranking 순위 · quantify 정량화하다</sub>  
✍️ 

### 문단 6 · Contamination

**⑯** 평가한 모델들의 사전 학습 데이터가 완전히 공개되지 않았으므로 원문 문서에 의한 오염 가능성을 배제할 수 없으며, 이 가능성은 논의 절에서 더 검토한다.  
<sub>힌트 (28단어): pretraining 사전 학습 · disclose 공개하다 · contamination 오염 · exclude 배제하다</sub>  
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

corresponding (대응하는) · substantial (상당한) · terminological accuracy (용어 정확성) · resolve by discussion (논의로 해소하다) · formulate (작성하다) · quantify (정량화하다) · practitioner (실무자) · pairwise (쌍별의) · wording (표현) · disclose (공개하다) · subset (부분 집합) · cannot be excluded (배제할 수 없다)

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
| ⑯ | | | | | | | |

**1차 합계:** ____ / 48점  ·  **가장 많은 오류 코드:** ____

---

## Part D. 정답과 섀도잉 스크립트 (풀이 후 확인)

> 끊어 읽기 표시( / )는 1회차 청크 경계입니다. 섀도잉은 음성 없이 시작해도 됩니다. 먼저 끊어 읽기 단위로 소리 내어 읽고, 익숙해지면 표시를 무시하고 한 호흡에 읽으세요.

### 문단 1 · Corpus

**①** The retrieval corpus was constructed from a set of radiation protection documents available in parallel English and Korean versions.  
<sub>↳ The retrieval corpus / was constructed / from a set / of radiation protection documents / available / in parallel English / and Korean versions.</sub>

**②** Each document was segmented into passages of approximately 200 to 300 tokens at paragraph boundaries, and English and Korean passages were aligned manually so that each English passage had a corresponding Korean passage covering the same content.  
<sub>↳ Each document / was segmented / into passages / of approximately / 200 to 300 tokens / at paragraph boundaries, / and English and Korean passages / were aligned manually / so that / each English passage / had a corresponding / Korean passage / covering the same content.</sub>

**③** The final corpus contained 2,400 aligned passage pairs.  
<sub>↳ The final corpus / contained / 2,400 aligned passage pairs.</sub>

### 문단 2 · Queries and relevance judgments

**④** Two subject-matter experts independently wrote 300 queries in Korean, each targeting information contained in one or more passages; English versions were then produced by professional translation and reviewed for terminological accuracy.  
<sub>↳ Two subject-matter experts / independently wrote / 300 queries in Korean, / each targeting information / contained / in one or more passages; / English versions / were then produced / by professional translation / and reviewed / for terminological accuracy.</sub>

**⑤** To reduce lexical overlap with the target passages, experts were instructed to formulate queries as practitioners would ask them rather than by copying passage wording.  
<sub>↳ To reduce / lexical overlap / with the target passages, / experts were instructed / to formulate queries / as practitioners / would ask them / rather than / by copying / passage wording.</sub>

**⑥** Relevance was judged on a three-point scale (0, not relevant; 1, partially relevant; 2, highly relevant).  
<sub>↳ Relevance / was judged / on a three-point scale / (0, not relevant; / 1, partially relevant; / 2, highly relevant).</sub>

**⑦** Inter-annotator agreement, measured on a random subset of 60 queries, was substantial (weighted Cohen's kappa = 0.78), and disagreements were resolved by discussion.  
<sub>↳ Inter-annotator agreement, / measured / on a random subset / of 60 queries, / was substantial / (weighted Cohen's kappa = 0.78), / and disagreements / were resolved / by discussion.</sub>

### 문단 3 · Models and retrieval setup

**⑧** Several publicly available multilingual embedding models with fewer than 600 million parameters were evaluated without fine-tuning.  
<sub>↳ Several publicly available / multilingual embedding models / with fewer than / 600 million parameters / were evaluated / without fine-tuning.</sub>

**⑨** For each model, passages and queries were encoded with the model's recommended prefixes and maximum sequence length, embeddings were L2-normalized, and retrieval was performed by exact cosine-similarity search over the full corpus.  
<sub>↳ For each model, / passages and queries / were encoded / with the model's / recommended prefixes / and maximum sequence length, / embeddings / were L2-normalized, / and retrieval / was performed / by exact / cosine-similarity search / over the full corpus.</sub>

**⑩** Model versions were fixed by recording repository commit identifiers.  
<sub>↳ Model versions / were fixed / by recording / repository commit identifiers.</sub>

### 문단 4 · Evaluation conditions and metrics

**⑪** Each model was evaluated under four conditions: Korean queries against Korean passages, English against English, Korean against English, and English against Korean.  
<sub>↳ Each model / was evaluated / under four conditions: / Korean queries / against Korean passages, / English against English, / Korean against English, / and English against Korean.</sub>

**⑫** Performance was measured using Recall@k for k = 1, 5, and 10, mean reciprocal rank at 10 (MRR@10), and normalized discounted cumulative gain at 10 (nDCG@10), with nDCG computed from graded relevance judgments.  
<sub>↳ Performance / was measured / using Recall@k / for k = 1, 5, and 10, / mean reciprocal rank / at 10 (MRR@10), / and normalized discounted / cumulative gain at 10 / (nDCG@10), / with nDCG / computed / from graded / relevance judgments.</sub>

### 문단 5 · Statistical analysis

**⑬** Differences between models were assessed using paired bootstrap resampling over queries with 10,000 resamples, yielding 95 percent confidence intervals for each pairwise difference.  
<sub>↳ Differences / between models / were assessed / using paired / bootstrap resampling / over queries / with 10,000 resamples, / yielding / 95 percent / confidence intervals / for each pairwise difference.</sub>

**⑭** P values were adjusted for multiple comparisons using the Holm procedure.  
<sub>↳ P values / were adjusted / for multiple comparisons / using the Holm procedure.</sub>

**⑮** Agreement between rankings on the domain benchmark and on a general benchmark was quantified with Kendall's tau.  
<sub>↳ Agreement / between rankings / on the domain benchmark / and on a general benchmark / was quantified / with Kendall's tau.</sub>

### 문단 6 · Contamination

**⑯** Because the pretraining data of the evaluated models are not fully disclosed, contamination by the source documents cannot be excluded; this possibility is examined further in the Discussion.  
<sub>↳ Because the pretraining data / of the evaluated models / are not fully disclosed, / contamination / by the source documents / cannot be excluded; / this possibility / is examined further / in the Discussion.</sub>

---

*원본 에세이: D06_Designing_a_Retrieval_Evaluation_Protocol.md · 이 워크북은 원본의 2회차 번역과 1회차 청크에서 자동 생성되었습니다.*
