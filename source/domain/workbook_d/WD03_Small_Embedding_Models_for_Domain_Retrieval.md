# 역번역 워크북 · D03. Small Embedding Models for Domain Retrieval
### 도메인 검색을 위한 소형 임베딩 모델 (서론: 공백 점유)

| 항목 | 내용 |
|---|---|
| 원본 | D03_Small_Embedding_Models_for_Domain_Retrieval.md |
| 트랙 | Domain Track (C1–C2) |
| 문장 수 / 단어 수 | 20문장 / 약 373단어 |
| 집중 포인트 | CARS 모형 Move 3 (목적 진술, 연구 질문, 기여 명시, 논문 구성 안내), 1인칭 복수 we, 열거형 연구 질문 |
| 권장 소요 시간 | 1차 풀이 약 35분 (채점·섀도잉 별도) |

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

**①** 검색 증강 생성(RAG)은 대형 언어 모델을 전문 분야에 맞춰 쓰는 데 널리 활용되는 접근법이 되었다.  
<sub>힌트 (17단어): retrieval 검색 · augment 증강하다 · approach 접근법 · adapt 맞추다, 적응시키다 · specialized 전문화된 · domain 분야</sub>  
✍️ 

**②** RAG 시스템은 모델 매개변수에 저장된 지식에만 의존하지 않고, 외부 문서 모음에서 관련 구절을 검색해 모델에 맥락으로 제공한다.  
<sub>힌트 (29단어): rely on ~에 의존하다 · solely 전적으로 · parameter 매개변수 · retrieve 검색하다, 가져오다 · relevant 관련된 · passage 구절 · external 외부의 · collection 모음 · supply 제공하다 · context 맥락</sub>  
✍️ 

**③** 따라서 최종 답변의 품질은 검색 구성 요소, 특히 질의와 문서를 표현하는 데 쓰이는 임베딩 모델에 크게 좌우된다.  
<sub>힌트 (26단어): depend on ~에 달려 있다 · component 구성 요소 · embedding 임베딩 · represent 표현하다 · query 질의</sub>  
✍️ 

### 문단 2

**④** 임베딩 모델은 흔히 MTEB(Massive Text Embedding Benchmark) 같은 공개 벤치마크를 근거로 선택된다.  
<sub>힌트 (19단어): select 선택하다 · benchmark 벤치마크</sub>  
✍️ 

**⑤** 이런 벤치마크는 여러 과제에서 모델을 비교하는 데 유용하지만, 테스트 데이터가 주로 일반 분야 텍스트로 되어 있어 그 성능이 전문 용어를 쓰는 기술 분야로 그대로 이어지지 않을 수 있다.  
<sub>힌트 (32단어): task 과제 · test collection 테스트 모음 · consist of ~로 이루어지다 · general-domain 일반 분야의 · performance 성능 · transfer 전이되다 · technical 기술적인 · terminology 용어</sub>  
✍️ 

**⑥** 이 한계는 규제 문서나 기술 문서가 영어와 다른 언어로 함께 존재하고 사용자가 어느 언어로든 질의할 수 있는 이중 언어 환경에서 특히 중요하다.  
<sub>힌트 (28단어): relevant 관련된 · bilingual 이중 언어의 · pose (질문을) 하다 · either 둘 중 어느 쪽</sub>  
✍️ 

**⑦** 게다가 엄격한 데이터 보안 요건 아래 운영되는 조직은 로컬 하드웨어에 배포할 수 있는 소형 모델을 선호하는 경우가 많은데, 이 범주는 리더보드 비교에서 상대적으로 덜 주목받는다.  
<sub>힌트 (27단어): organization 조직 · requirement 요건 · prefer 선호하다 · deploy 배포하다 · local 로컬의 · category 범주 · leaderboard 순위표</sub>  
✍️ 

### 문단 3

**⑧** 본 연구에서는 방사선 방호 분야의 영어·한국어 병렬 문서 말뭉치에서 소형 다국어 임베딩 모델의 검색 성능을 평가한다.  
<sub>힌트 (23단어): evaluate 평가하다 · multilingual 다국어의 · parallel corpus 병렬 말뭉치</sub>  
✍️ 

**⑨** 구체적으로 세 가지 연구 질문을 다룬다.  
<sub>힌트 (6단어): specifically 구체적으로 · research question 연구 질문</sub>  
✍️ 

**⑩** 첫째, 질의와 문서가 같은 언어일 때 소형 모델들의 성능은 서로 어떻게 비교되는가?  
<sub>힌트 (18단어): —</sub>  
✍️ 

**⑪** 둘째, 한국어 질의로 영어 구절을 찾아야 하는 교차 언어 검색(또는 그 반대)에서 성능은 얼마나 떨어지는가?  
<sub>힌트 (21단어): decline 떨어지다 · cross-lingual 교차 언어의 · vice versa 그 반대도 마찬가지</sub>  
✍️ 

**⑫** 셋째, 일반 벤치마크의 순위는 이 분야에서의 순위를 어느 정도 예측하는가?  
<sub>힌트 (16단어): to what extent 어느 정도로 · derive 도출하다 · predict 예측하다</sub>  
✍️ 

### 문단 4

**⑬** 본 연구의 기여는 세 가지다.  
<sub>힌트 (4단어): contribution 기여 · threefold 세 겹의</sub>  
✍️ 

**⑭** 첫째, 분야 전문가가 검증한 질의–구절 쌍으로 구성된 분야 특화 검색 벤치마크를 구축한다.  
<sub>힌트 (14단어): construct 구축하다 · domain-specific 분야 특화의 · pair 쌍 · validate 검증하다 · subject-matter expert 분야 전문가</sub>  
✍️ 

**⑮** 둘째, Recall@k와 nDCG 같은 표준 지표를 사용해 단일 언어 조건과 교차 언어 조건에서 여러 소형 임베딩 모델을 체계적으로 비교한 결과를 보고한다.  
<sub>힌트 (27단어): systematic 체계적인 · monolingual 단일 언어의 · condition 조건 · metric 지표 · recall 재현율 · normalized 정규화된 · cumulative gain 누적 이득</sub>  
✍️ 

**⑯** 마지막으로, 일반 순위와 분야 특화 순위의 대응 관계를 분석해, 비슷한 환경에서 모델을 고를 때 쓸 수 있는 실용적 지침을 제시한다.  
<sub>힌트 (19단어): analyze 분석하다 · correspondence 대응 · guidance 지침 · selection 선택</sub>  
✍️ 

### 문단 5

**⑰** 이 논문의 나머지 부분은 다음과 같이 구성된다.  
<sub>힌트 (9단어): remainder 나머지 · organize 구성하다 · as follows 다음과 같이</sub>  
✍️ 

**⑱** 2절에서는 임베딩 평가와 분야 적응에 관한 관련 연구를 검토한다.  
<sub>힌트 (11단어): review 검토하다 · related work 관련 연구 · adaptation 적응</sub>  
✍️ 

**⑲** 3절에서는 말뭉치, 질의 구축 방법, 평가 절차를 기술한다.  
<sub>힌트 (10단어): corpus 말뭉치 · construction 구축 · protocol 절차</sub>  
✍️ 

**⑳** 4절에서 결과를 제시하고, 5절에서 그 함의와 한계를 논의한 뒤, 6절에서 결론을 맺는다.  
<sub>힌트 (17단어): present 제시하다 · discuss 논의하다 · implication 함의 · conclude 결론을 맺다</sub>  
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

specialized domain (전문 분야) · threefold (세 가지의) · rely solely on (~에만 의존하다) · validate (검증하다) · consist largely of (주로 ~로 이루어지다) · correspondence (대응 관계) · transfer to (~로 전이되다) · the remainder of (~의 나머지) · pose a query (질의하다) · as follows (다음과 같이) · to what extent (어느 정도로) · vice versa (그 반대도 마찬가지)

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
| ⑰ | | | | | | | |
| ⑱ | | | | | | | |
| ⑲ | | | | | | | |
| ⑳ | | | | | | | |

**1차 합계:** ____ / 60점  ·  **가장 많은 오류 코드:** ____

---

## Part D. 정답과 섀도잉 스크립트 (풀이 후 확인)

> 끊어 읽기 표시( / )는 1회차 청크 경계입니다. 섀도잉은 음성 없이 시작해도 됩니다. 먼저 끊어 읽기 단위로 소리 내어 읽고, 익숙해지면 표시를 무시하고 한 호흡에 읽으세요.

### 문단 1

**①** Retrieval-augmented generation (RAG) has become a widely used approach for adapting large language models to specialized domains.  
<sub>↳ Retrieval-augmented generation (RAG) / has become / a widely used approach / for adapting / large language models / to specialized domains.</sub>

**②** Instead of relying solely on knowledge stored in model parameters, a RAG system retrieves relevant passages from an external document collection and supplies them to the model as context.  
<sub>↳ Instead of relying solely / on knowledge / stored in model parameters, / a RAG system retrieves / relevant passages / from an external / document collection / and supplies them / to the model / as context.</sub>

**③** The quality of the final answer therefore depends heavily on the retrieval component, and in particular on the embedding model used to represent queries and documents.  
<sub>↳ The quality / of the final answer / therefore depends heavily / on the retrieval component, / and in particular / on the embedding model / used to represent / queries and documents.</sub>

### 문단 2

**④** Embedding models are commonly selected on the basis of public benchmarks such as the Massive Text Embedding Benchmark (MTEB).  
<sub>↳ Embedding models / are commonly selected / on the basis of / public benchmarks / such as / the Massive Text Embedding Benchmark (MTEB).</sub>

**⑤** Such benchmarks are valuable for comparing models across many tasks, but their test collections consist largely of general-domain text, and performance on them may not transfer to technical domains with specialized terminology.  
<sub>↳ Such benchmarks / are valuable / for comparing models / across many tasks, / but their test collections / consist largely / of general-domain text, / and performance on them / may not transfer / to technical domains / with specialized terminology.</sub>

**⑥** This limitation is particularly relevant in bilingual settings, where regulatory or technical documents exist in both English and another language, and users may pose queries in either language.  
<sub>↳ This limitation / is particularly relevant / in bilingual settings, / where regulatory / or technical documents / exist in both English / and another language, / and users / may pose queries / in either language.</sub>

**⑦** Moreover, organizations operating under strict data-security requirements often prefer small models that can be deployed on local hardware, a category that receives less attention in leaderboard comparisons.  
<sub>↳ Moreover, / organizations / operating / under strict data-security requirements / often prefer / small models / that can be deployed / on local hardware, / a category / that receives less attention / in leaderboard comparisons.</sub>

### 문단 3

**⑧** In this study, we evaluate small multilingual embedding models for retrieval over a parallel corpus of English and Korean documents in radiation protection.  
<sub>↳ In this study, / we evaluate / small multilingual / embedding models / for retrieval / over a parallel corpus / of English and Korean documents / in radiation protection.</sub>

**⑨** Specifically, we address three research questions.  
<sub>↳ Specifically, / we address / three research questions.</sub>

**⑩** First, how do small models compare with one another when queries and documents are in the same language?  
<sub>↳ First, / how do small models / compare with one another / when queries and documents / are in the same language?</sub>

**⑪** Second, how much does performance decline in cross-lingual retrieval, where a Korean query must retrieve an English passage, or vice versa?  
<sub>↳ Second, / how much / does performance decline / in cross-lingual retrieval, / where a Korean query / must retrieve / an English passage, / or vice versa?</sub>

**⑫** Third, to what extent do rankings derived from a general benchmark predict rankings in this domain?  
<sub>↳ Third, / to what extent / do rankings / derived from / a general benchmark / predict rankings / in this domain?</sub>

### 문단 4

**⑬** Our contributions are threefold.  
<sub>↳ Our contributions / are threefold.</sub>

**⑭** We construct a domain-specific retrieval benchmark consisting of query–passage pairs validated by subject-matter experts.  
<sub>↳ We construct / a domain-specific / retrieval benchmark / consisting of / query–passage pairs / validated / by subject-matter experts.</sub>

**⑮** We report a systematic comparison of several small embedding models under monolingual and cross-lingual conditions, using standard metrics including recall at k and normalized discounted cumulative gain.  
<sub>↳ We report / a systematic comparison / of several / small embedding models / under monolingual / and cross-lingual conditions, / using standard metrics / including recall at k / and normalized discounted / cumulative gain.</sub>

**⑯** Finally, we analyze the correspondence between general and domain-specific rankings, offering practical guidance for model selection in similar settings.  
<sub>↳ Finally, / we analyze / the correspondence / between general / and domain-specific rankings, / offering practical guidance / for model selection / in similar settings.</sub>

### 문단 5

**⑰** The remainder of this paper is organized as follows.  
<sub>↳ The remainder / of this paper / is organized / as follows.</sub>

**⑱** Section 2 reviews related work on embedding evaluation and domain adaptation.  
<sub>↳ Section 2 reviews / related work / on embedding evaluation / and domain adaptation.</sub>

**⑲** Section 3 describes the corpus, query construction, and evaluation protocol.  
<sub>↳ Section 3 describes / the corpus, / query construction, / and evaluation protocol.</sub>

**⑳** Section 4 presents the results, and Section 5 discusses their implications and limitations before Section 6 concludes.  
<sub>↳ Section 4 presents / the results, / and Section 5 discusses / their implications / and limitations / before Section 6 / concludes.</sub>

---

*원본 에세이: D03_Small_Embedding_Models_for_Domain_Retrieval.md · 이 워크북은 원본의 2회차 번역과 1회차 청크에서 자동 생성되었습니다.*
