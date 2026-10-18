# D03. Small Embedding Models for Domain Retrieval
### 도메인 검색을 위한 소형 임베딩 모델 (서론: 공백 점유)

| 항목 | 내용 |
|---|---|
| 시리즈 | Domain Track · Unit A 서론 (3/18) · 분야: ML·LLM 평가 |
| 수준 | 대학원·연구자 · CEFR C1–C2 |
| 분량 | 약 373단어 · 5문단 · 20문장 |
| 문체 | 연구 논문 서론 (가상 연구, 컴퓨터과학 관례) |
| 핵심 문법 | CARS 모형 Move 3 (목적 진술, 연구 질문, 기여 명시, 논문 구성 안내), 1인칭 복수 we, 열거형 연구 질문 |
| 미리보기 | Methods 절의 평가 프로토콜 기술 (D06) |

---

## 학습 방법

| 단계 | 할 일 | 권장 횟수 |
|---|---|---|
| 1회차 | 청크 단위 직독직해. 청크마다 끊어 소리 내어 읽고 바로 한국어 뜻을 떠올린다 | 3회 |
| 2회차 | 문장 단위 직독직해. 한 문장을 한 호흡으로 읽고 의미를 확인한다 | 3회 |
| 3회차 | 원문만 보고 처음부터 끝까지 낭독한다. 시간을 재서 기록한다 | 3회 이상 |

낭독 속도는 분당 단어 수(WPM)로 기록합니다. 373단어를 3분에 읽으면 약 124 WPM입니다. 회독이 거듭될수록 속도가 오르고 끊기는 지점이 줄어드는지 확인하세요.

---

## 0. 원문 (Full Text)

> Retrieval-augmented generation (RAG) has become a widely used approach for adapting large language models to specialized domains. Instead of relying solely on knowledge stored in model parameters, a RAG system retrieves relevant passages from an external document collection and supplies them to the model as context. The quality of the final answer therefore depends heavily on the retrieval component, and in particular on the embedding model used to represent queries and documents.
>
> Embedding models are commonly selected on the basis of public benchmarks such as the Massive Text Embedding Benchmark (MTEB). Such benchmarks are valuable for comparing models across many tasks, but their test collections consist largely of general-domain text, and performance on them may not transfer to technical domains with specialized terminology. This limitation is particularly relevant in bilingual settings, where regulatory or technical documents exist in both English and another language, and users may pose queries in either language. Moreover, organizations operating under strict data-security requirements often prefer small models that can be deployed on local hardware, a category that receives less attention in leaderboard comparisons.
>
> In this study, we evaluate small multilingual embedding models for retrieval over a parallel corpus of English and Korean documents in radiation protection. Specifically, we address three research questions. First, how do small models compare with one another when queries and documents are in the same language? Second, how much does performance decline in cross-lingual retrieval, where a Korean query must retrieve an English passage, or vice versa? Third, to what extent do rankings derived from a general benchmark predict rankings in this domain?
>
> Our contributions are threefold. We construct a domain-specific retrieval benchmark consisting of query–passage pairs validated by subject-matter experts. We report a systematic comparison of several small embedding models under monolingual and cross-lingual conditions, using standard metrics including recall at k and normalized discounted cumulative gain. Finally, we analyze the correspondence between general and domain-specific rankings, offering practical guidance for model selection in similar settings.
>
> The remainder of this paper is organized as follows. Section 2 reviews related work on embedding evaluation and domain adaptation. Section 3 describes the corpus, query construction, and evaluation protocol. Section 4 presents the results, and Section 5 discusses their implications and limitations before Section 6 concludes.

---

## 1회차 · 청크 단위 직독직해

> 영어 어순 그대로 앞에서부터 의미를 받아들이는 것이 목표입니다. 한국어 번역도 영어 순서를 따릅니다.

### 문단 1

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Retrieval-augmented generation (RAG) | 검색 증강 생성(RAG)은 | retrieval 검색 · augment 증강하다 |
| has become | ~이 되었다 |  |
| a widely used approach | 널리 쓰이는 접근법이 | approach 접근법 |
| for adapting | 맞추기 위한 | adapt 맞추다, 적응시키다 |
| large language models | 대형 언어 모델을 |  |
| to specialized domains. | 전문 분야에. | specialized 전문화된 · domain 분야 |
| Instead of relying solely | 전적으로 의존하는 대신 | rely on ~에 의존하다 · solely 전적으로 |
| on knowledge | 지식에 |  |
| stored in model parameters, | 모델 매개변수에 저장된, | parameter 매개변수 |
| a RAG system retrieves | RAG 시스템은 검색한다 | retrieve 검색하다, 가져오다 |
| relevant passages | 관련 구절을 | relevant 관련된 · passage 구절 |
| from an external | 외부의 | external 외부의 |
| document collection | 문서 모음에서 | collection 모음 |
| and supplies them | 그리고 그것들을 제공한다 | supply 제공하다 |
| to the model | 모델에 |  |
| as context. | 맥락으로. | context 맥락 |
| The quality | 품질은 |  |
| of the final answer | 최종 답변의 |  |
| therefore depends heavily | 따라서 크게 좌우된다 | depend on ~에 달려 있다 |
| on the retrieval component, | 검색 구성 요소에, | component 구성 요소 |
| and in particular | 그리고 특히 |  |
| on the embedding model | 임베딩 모델에 | embedding 임베딩 |
| used to represent | 표현하는 데 쓰이는 | represent 표현하다 |
| queries and documents. | 질의와 문서를. | query 질의 |

### 문단 2

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Embedding models | 임베딩 모델은 |  |
| are commonly selected | 흔히 선택된다 | select 선택하다 |
| on the basis of | ~을 근거로 |  |
| public benchmarks | 공개 벤치마크를 | benchmark 벤치마크 |
| such as | ~같은 |  |
| the Massive Text Embedding Benchmark (MTEB). | MTEB 같은. |  |
| Such benchmarks | 그런 벤치마크는 |  |
| are valuable | 가치가 있지만 |  |
| for comparing models | 모델을 비교하는 데 |  |
| across many tasks, | 여러 과제에 걸쳐, | task 과제 |
| but their test collections | 그것들의 테스트 모음은 | test collection 테스트 모음 |
| consist largely | 주로 이루어져 있고 | consist of ~로 이루어지다 |
| of general-domain text, | 일반 분야 텍스트로, | general-domain 일반 분야의 |
| and performance on them | 그리고 그것들에서의 성능은 | performance 성능 |
| may not transfer | 전이되지 않을 수 있다 | transfer 전이되다 |
| to technical domains | 기술 분야로 | technical 기술적인 |
| with specialized terminology. | 전문 용어가 있는. | terminology 용어 |
| This limitation | 이 한계는 |  |
| is particularly relevant | 특히 관련이 있다 | relevant 관련된 |
| in bilingual settings, | 이중 언어 환경에서, | bilingual 이중 언어의 |
| where regulatory | 그곳에서 규제 |  |
| or technical documents | 또는 기술 문서가 |  |
| exist in both English | 영어와 |  |
| and another language, | 다른 언어로 모두 존재하며, |  |
| and users | 그리고 사용자는 |  |
| may pose queries | 질의를 할 수 있다 | pose (질문을) 하다 |
| in either language. | 두 언어 중 어느 쪽으로든. | either 둘 중 어느 쪽 |
| Moreover, | 게다가, |  |
| organizations | 조직들은 | organization 조직 |
| operating | 운영되는 |  |
| under strict data-security requirements | 엄격한 데이터 보안 요건하에서 | requirement 요건 |
| often prefer | 흔히 선호한다 | prefer 선호하다 |
| small models | 소형 모델을 |  |
| that can be deployed | 배포될 수 있는 | deploy 배포하다 |
| on local hardware, | 로컬 하드웨어에, | local 로컬의 |
| a category | 하나의 범주인데 | category 범주 |
| that receives less attention | 덜 주목받는 |  |
| in leaderboard comparisons. | 리더보드 비교에서. | leaderboard 순위표 |

### 문단 3

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| In this study, | 본 연구에서, |  |
| we evaluate | 우리는 평가한다 | evaluate 평가하다 |
| small multilingual | 소형 다국어 | multilingual 다국어의 |
| embedding models | 임베딩 모델을 |  |
| for retrieval | 검색에 대해 |  |
| over a parallel corpus | 병렬 말뭉치에서의 | parallel corpus 병렬 말뭉치 |
| of English and Korean documents | 영어와 한국어 문서로 된 |  |
| in radiation protection. | 방사선 방호 분야의. |  |
| Specifically, | 구체적으로, | specifically 구체적으로 |
| we address | 우리는 다룬다 |  |
| three research questions. | 세 가지 연구 질문을. | research question 연구 질문 |
| First, | 첫째, |  |
| how do small models | 소형 모델들은 어떻게 |  |
| compare with one another | 서로 비교되는가 |  |
| when queries and documents | 질의와 문서가 ~일 때 |  |
| are in the same language? | 같은 언어일 때? |  |
| Second, | 둘째, |  |
| how much | 얼마나 많이 |  |
| does performance decline | 성능이 떨어지는가 | decline 떨어지다 |
| in cross-lingual retrieval, | 교차 언어 검색에서, | cross-lingual 교차 언어의 |
| where a Korean query | 한국어 질의가 |  |
| must retrieve | 검색해야 하는 |  |
| an English passage, | 영어 구절을, |  |
| or vice versa? | 또는 그 반대의 경우에? | vice versa 그 반대도 마찬가지 |
| Third, | 셋째, |  |
| to what extent | 어느 정도까지 | to what extent 어느 정도로 |
| do rankings | 순위가 |  |
| derived from | ~에서 도출된 | derive 도출하다 |
| a general benchmark | 일반 벤치마크에서 |  |
| predict rankings | 순위를 예측하는가 | predict 예측하다 |
| in this domain? | 이 분야에서의? |  |

### 문단 4

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Our contributions | 우리의 기여는 | contribution 기여 |
| are threefold. | 세 가지다. | threefold 세 겹의 |
| We construct | 우리는 구축한다 | construct 구축하다 |
| a domain-specific | 분야 특화 | domain-specific 분야 특화의 |
| retrieval benchmark | 검색 벤치마크를 |  |
| consisting of | ~로 구성된 |  |
| query–passage pairs | 질의–구절 쌍으로 | pair 쌍 |
| validated | 검증된 | validate 검증하다 |
| by subject-matter experts. | 해당 분야 전문가에 의해. | subject-matter expert 분야 전문가 |
| We report | 우리는 보고한다 |  |
| a systematic comparison | 체계적인 비교를 | systematic 체계적인 |
| of several | 여러 |  |
| small embedding models | 소형 임베딩 모델의 |  |
| under monolingual | 단일 언어와 | monolingual 단일 언어의 |
| and cross-lingual conditions, | 교차 언어 조건에서, | condition 조건 |
| using standard metrics | 표준 지표를 사용하여 | metric 지표 |
| including recall at k | k에서의 재현율과 | recall 재현율 |
| and normalized discounted | 정규화 할인 | normalized 정규화된 |
| cumulative gain. | 누적 이득을 포함한. | cumulative gain 누적 이득 |
| Finally, | 마지막으로, |  |
| we analyze | 우리는 분석한다 | analyze 분석하다 |
| the correspondence | 대응 관계를 | correspondence 대응 |
| between general | 일반 순위와 |  |
| and domain-specific rankings, | 분야 특화 순위 사이의, |  |
| offering practical guidance | 실용적 지침을 제공하면서 | guidance 지침 |
| for model selection | 모델 선택을 위한 | selection 선택 |
| in similar settings. | 비슷한 환경에서의. |  |

### 문단 5

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| The remainder | 나머지는 | remainder 나머지 |
| of this paper | 이 논문의 |  |
| is organized | 구성되어 있다 | organize 구성하다 |
| as follows. | 다음과 같이. | as follows 다음과 같이 |
| Section 2 reviews | 2절은 검토한다 | review 검토하다 |
| related work | 관련 연구를 | related work 관련 연구 |
| on embedding evaluation | 임베딩 평가와 |  |
| and domain adaptation. | 분야 적응에 관한. | adaptation 적응 |
| Section 3 describes | 3절은 기술한다 |  |
| the corpus, | 말뭉치, | corpus 말뭉치 |
| query construction, | 질의 구축, | construction 구축 |
| and evaluation protocol. | 그리고 평가 절차를. | protocol 절차 |
| Section 4 presents | 4절은 제시하고 | present 제시하다 |
| the results, | 결과를, |  |
| and Section 5 discusses | 그리고 5절은 논의한다 | discuss 논의하다 |
| their implications | 그것의 함의와 | implication 함의 |
| and limitations | 한계를 |  |
| before Section 6 | 6절이 ~하기 전에 |  |
| concludes. | 결론을 맺기. | conclude 결론을 맺다 |

---

## 2회차 · 문장 단위 직독직해

> 한 문장을 한 호흡에 읽는 연습입니다. 1회차에서 끊었던 지점을 의식하되, 멈추지 않고 이어 읽습니다.

### 문단 1

**① Retrieval-augmented generation (RAG) has become a widely used approach for adapting large language models to specialized domains.**
검색 증강 생성(RAG)은 대형 언어 모델을 전문 분야에 맞춰 쓰는 데 널리 활용되는 접근법이 되었다.
어휘: retrieval 검색 · augment 증강하다 · approach 접근법 · adapt 맞추다, 적응시키다 · specialized 전문화된 · domain 분야

**② Instead of relying solely on knowledge stored in model parameters, a RAG system retrieves relevant passages from an external document collection and supplies them to the model as context.**
RAG 시스템은 모델 매개변수에 저장된 지식에만 의존하지 않고, 외부 문서 모음에서 관련 구절을 검색해 모델에 맥락으로 제공한다.
어휘: rely on ~에 의존하다 · solely 전적으로 · parameter 매개변수 · retrieve 검색하다, 가져오다 · relevant 관련된 · passage 구절 · external 외부의 · collection 모음 · supply 제공하다 · context 맥락

**③ The quality of the final answer therefore depends heavily on the retrieval component, and in particular on the embedding model used to represent queries and documents.**
따라서 최종 답변의 품질은 검색 구성 요소, 특히 질의와 문서를 표현하는 데 쓰이는 임베딩 모델에 크게 좌우된다.
어휘: depend on ~에 달려 있다 · component 구성 요소 · embedding 임베딩 · represent 표현하다 · query 질의

### 문단 2

**④ Embedding models are commonly selected on the basis of public benchmarks such as the Massive Text Embedding Benchmark (MTEB).**
임베딩 모델은 흔히 MTEB(Massive Text Embedding Benchmark) 같은 공개 벤치마크를 근거로 선택된다.
어휘: select 선택하다 · benchmark 벤치마크

**⑤ Such benchmarks are valuable for comparing models across many tasks, but their test collections consist largely of general-domain text, and performance on them may not transfer to technical domains with specialized terminology.**
이런 벤치마크는 여러 과제에서 모델을 비교하는 데 유용하지만, 테스트 데이터가 주로 일반 분야 텍스트로 되어 있어 그 성능이 전문 용어를 쓰는 기술 분야로 그대로 이어지지 않을 수 있다.
어휘: task 과제 · test collection 테스트 모음 · consist of ~로 이루어지다 · general-domain 일반 분야의 · performance 성능 · transfer 전이되다 · technical 기술적인 · terminology 용어

**⑥ This limitation is particularly relevant in bilingual settings, where regulatory or technical documents exist in both English and another language, and users may pose queries in either language.**
이 한계는 규제 문서나 기술 문서가 영어와 다른 언어로 함께 존재하고 사용자가 어느 언어로든 질의할 수 있는 이중 언어 환경에서 특히 중요하다.
어휘: relevant 관련된 · bilingual 이중 언어의 · pose (질문을) 하다 · either 둘 중 어느 쪽

**⑦ Moreover, organizations operating under strict data-security requirements often prefer small models that can be deployed on local hardware, a category that receives less attention in leaderboard comparisons.**
게다가 엄격한 데이터 보안 요건 아래 운영되는 조직은 로컬 하드웨어에 배포할 수 있는 소형 모델을 선호하는 경우가 많은데, 이 범주는 리더보드 비교에서 상대적으로 덜 주목받는다.
어휘: organization 조직 · requirement 요건 · prefer 선호하다 · deploy 배포하다 · local 로컬의 · category 범주 · leaderboard 순위표

### 문단 3

**⑧ In this study, we evaluate small multilingual embedding models for retrieval over a parallel corpus of English and Korean documents in radiation protection.**
본 연구에서는 방사선 방호 분야의 영어·한국어 병렬 문서 말뭉치에서 소형 다국어 임베딩 모델의 검색 성능을 평가한다.
어휘: evaluate 평가하다 · multilingual 다국어의 · parallel corpus 병렬 말뭉치

**⑨ Specifically, we address three research questions.**
구체적으로 세 가지 연구 질문을 다룬다.
어휘: specifically 구체적으로 · research question 연구 질문

**⑩ First, how do small models compare with one another when queries and documents are in the same language?**
첫째, 질의와 문서가 같은 언어일 때 소형 모델들의 성능은 서로 어떻게 비교되는가?

**⑪ Second, how much does performance decline in cross-lingual retrieval, where a Korean query must retrieve an English passage, or vice versa?**
둘째, 한국어 질의로 영어 구절을 찾아야 하는 교차 언어 검색(또는 그 반대)에서 성능은 얼마나 떨어지는가?
어휘: decline 떨어지다 · cross-lingual 교차 언어의 · vice versa 그 반대도 마찬가지

**⑫ Third, to what extent do rankings derived from a general benchmark predict rankings in this domain?**
셋째, 일반 벤치마크의 순위는 이 분야에서의 순위를 어느 정도 예측하는가?
어휘: to what extent 어느 정도로 · derive 도출하다 · predict 예측하다

### 문단 4

**⑬ Our contributions are threefold.**
본 연구의 기여는 세 가지다.
어휘: contribution 기여 · threefold 세 겹의

**⑭ We construct a domain-specific retrieval benchmark consisting of query–passage pairs validated by subject-matter experts.**
첫째, 분야 전문가가 검증한 질의–구절 쌍으로 구성된 분야 특화 검색 벤치마크를 구축한다.
어휘: construct 구축하다 · domain-specific 분야 특화의 · pair 쌍 · validate 검증하다 · subject-matter expert 분야 전문가

**⑮ We report a systematic comparison of several small embedding models under monolingual and cross-lingual conditions, using standard metrics including recall at k and normalized discounted cumulative gain.**
둘째, Recall@k와 nDCG 같은 표준 지표를 사용해 단일 언어 조건과 교차 언어 조건에서 여러 소형 임베딩 모델을 체계적으로 비교한 결과를 보고한다.
어휘: systematic 체계적인 · monolingual 단일 언어의 · condition 조건 · metric 지표 · recall 재현율 · normalized 정규화된 · cumulative gain 누적 이득

**⑯ Finally, we analyze the correspondence between general and domain-specific rankings, offering practical guidance for model selection in similar settings.**
마지막으로, 일반 순위와 분야 특화 순위의 대응 관계를 분석해, 비슷한 환경에서 모델을 고를 때 쓸 수 있는 실용적 지침을 제시한다.
어휘: analyze 분석하다 · correspondence 대응 · guidance 지침 · selection 선택

### 문단 5

**⑰ The remainder of this paper is organized as follows.**
이 논문의 나머지 부분은 다음과 같이 구성된다.
어휘: remainder 나머지 · organize 구성하다 · as follows 다음과 같이

**⑱ Section 2 reviews related work on embedding evaluation and domain adaptation.**
2절에서는 임베딩 평가와 분야 적응에 관한 관련 연구를 검토한다.
어휘: review 검토하다 · related work 관련 연구 · adaptation 적응

**⑲ Section 3 describes the corpus, query construction, and evaluation protocol.**
3절에서는 말뭉치, 질의 구축 방법, 평가 절차를 기술한다.
어휘: corpus 말뭉치 · construction 구축 · protocol 절차

**⑳ Section 4 presents the results, and Section 5 discusses their implications and limitations before Section 6 concludes.**
4절에서 결과를 제시하고, 5절에서 그 함의와 한계를 논의한 뒤, 6절에서 결론을 맺는다.
어휘: present 제시하다 · discuss 논의하다 · implication 함의 · conclude 결론을 맺다

---

## 참고 문헌

Lewis, P., Perez, E., Piktus, A., et al. (2020). Retrieval-augmented generation for knowledge-intensive NLP tasks. In *Advances in Neural Information Processing Systems 33* (NeurIPS 2020).

Muennighoff, N., Tazi, N., Magne, L., & Reimers, N. (2023). MTEB: Massive Text Embedding Benchmark. In *Proceedings of the 17th Conference of the European Chapter of the Association for Computational Linguistics* (EACL 2023).

**가상 연구에 대한 주석.** RAG와 MTEB에 관한 1–2문단의 배경은 실제 문헌에 근거했습니다. 3–5문단의 연구 질문, 기여, 논문 구성은 Move 3 연습용으로 설정한 가상 연구입니다. 실제 투고 원고라면 2문단의 "general-domain text"나 "receives less attention" 같은 주장에 해당 근거(벤치마크 구성 분석이나 관련 연구 인용)를 붙여야 합니다.

## 학술 영어 포인트

### 1. Move 3의 구성 요소

| 단계 | 기능 | 이 글의 표현 | 분야별 빈도 |
|---|---|---|---|
| 목적 진술 | 본 연구가 무엇을 하는가 | **In this study, we evaluate**… | 모든 분야 필수 |
| 연구 질문 | 구체적으로 무엇에 답하는가 | **Specifically, we address three research questions. First,… Second,… Third,…** | 대부분 |
| 기여 명시 | 무엇을 새로 제공하는가 | **Our contributions are threefold.** We construct… We report… Finally, we analyze… | 컴퓨터과학·공학에서 거의 필수, 의학에서는 드묾 |
| 주요 결과 예고 | 핵심 결과를 미리 제시 | (이 글에는 없음) | 분야마다 다름 |
| 논문 구성 안내 | 이후 절의 순서 | **The remainder of this paper is organized as follows.** | 컴퓨터과학·공학에서 흔함 |

**분야 관례의 차이.** "Our contributions are threefold"와 "The remainder of this paper is organized as follows"는 컴퓨터과학 논문에서는 표준적이지만, 임상 의학 논문의 서론에는 거의 쓰이지 않습니다. 임상 논문은 D02처럼 짧은 목적 문장으로 서론을 끝내는 것이 일반적입니다. 같은 Move 3라도 투고 분야에 맞춰 길이와 구성을 조절해야 합니다.

### 2. 연구 질문의 형식

| 형식 | 예 | 특징 |
|---|---|---|
| 직접 의문문 | **How much does performance decline** in cross-lingual retrieval? | 명료함, 컴퓨터과학에서 흔함 |
| 간접 의문문 | We examined **how frequently HbA1c and TIR disagree**. (D02) | 문장 흐름이 자연스러움 |
| 가설 진술 | We hypothesized that… | 확증적 연구에서 사용 |

세 질문이 **비교 → 변화량 → 예측력**으로 점점 일반화되는 순서라는 점에 주목하세요. 연구 질문을 나열할 때는 논리적 진행이 보이도록 배치하는 것이 좋습니다.

### 3. 1인칭 복수 we

컴퓨터과학, 공학, 그리고 점점 많은 자연과학 분야에서 "we"는 표준적입니다. 능동태로 행위자를 분명히 해 문장이 짧고 명확해집니다. 반면 일부 임상·생의학 학술지는 여전히 수동태("The present study examined…")를 선호합니다. D01–D03을 비교해 보면, D01과 D02는 "the present study"를, D03은 "we"를 썼습니다.

### 4. 분야 어휘

| 영어 | 한국어 | 영어 | 한국어 |
|---|---|---|---|
| retrieval-augmented generation | 검색 증강 생성 | parallel corpus | 병렬 말뭉치 |
| embedding model | 임베딩 모델 | cross-lingual retrieval | 교차 언어 검색 |
| query / passage | 질의 / 구절 | recall at k (Recall@k) | k에서의 재현율 |
| benchmark / leaderboard | 벤치마크 / 순위표 | nDCG | 정규화 할인 누적 이득 |
| deploy on local hardware | 로컬 하드웨어에 배포하다 | subject-matter expert | 분야 전문가 |
| domain adaptation | 분야 적응 | evaluation protocol | 평가 절차 |

## 핵심 어휘 정리 (Domain Track 어휘장 D03)

| 어휘 | 뜻 | 어휘 | 뜻 |
|---|---|---|---|
| specialized domain | 전문 분야 | threefold | 세 가지의 |
| rely solely on | ~에만 의존하다 | validate | 검증하다 |
| consist largely of | 주로 ~로 이루어지다 | correspondence | 대응 관계 |
| transfer to | ~로 전이되다 | the remainder of | ~의 나머지 |
| pose a query | 질의하다 | as follows | 다음과 같이 |
| to what extent | 어느 정도로 | vice versa | 그 반대도 마찬가지 |

---

## 낭독 기록표

| 회차 | 날짜 | 소요 시간 | WPM (373 ÷ 분) | 막힌 문장 번호 |
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

*Original essay written for the 30-part reading series. Next: D04. Calibration Traceability in Personal Dosimetry (방법: 측정 체계 기술)*
