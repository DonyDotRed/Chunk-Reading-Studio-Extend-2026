# D15. Responding to Reviewers
### 심사 의견에 답하기 (연구 전달: 심사 답변서)

| 항목 | 내용 |
|---|---|
| 시리즈 | Domain Track · Unit E 연구 전달 (15/18) · 분야: ML·LLM 평가 |
| 수준 | 대학원·연구자 · CEFR C1–C2 |
| 분량 | 약 346단어 · 10문단 · 21문장 |
| 문체 | 심사 답변서 (response to reviewers, 가상 연구 D03·D06·D09·D12의 수정 과정) |
| 핵심 문법 | 감사와 수용 (We agree with the reviewer…), 부분 수용과 정중한 반론 (We respectfully note…), 수정 위치 명시 (page, lines), 방어적 표현 피하기 |
| 미리보기 | 학회 발표 원고 (D16) |

---

## 학습 방법

| 단계 | 할 일 | 권장 횟수 |
|---|---|---|
| 1회차 | 청크 단위 직독직해. 청크마다 끊어 소리 내어 읽고 바로 한국어 뜻을 떠올린다 | 3회 |
| 2회차 | 문장 단위 직독직해. 한 문장을 한 호흡으로 읽고 의미를 확인한다 | 3회 |
| 3회차 | 원문만 보고 처음부터 끝까지 낭독한다. 시간을 재서 기록한다 | 3회 이상 |

낭독 속도는 분당 단어 수(WPM)로 기록합니다. 346단어를 3분에 읽으면 약 115 WPM입니다. 회독이 거듭될수록 속도가 오르고 끊기는 지점이 줄어드는지 확인하세요.

---

## 0. 원문 (Full Text)

> We thank the editor and the reviewers for their careful reading of our manuscript and for their constructive comments. We have revised the manuscript accordingly. Below, we respond to each comment in turn; changes in the manuscript are highlighted, and page and line numbers refer to the revised version.
>
> **Reviewer 1 · Comment 1**
>
> The authors state that Model A achieved the best monolingual performance, but the difference from Model C does not appear to be significant.
>
> **Response**
>
> We agree with the reviewer and thank them for this observation. The difference between Models A and C was not statistically significant, and our original wording could have implied otherwise. We have revised the Results (page 7, lines 12–15) to state that the two models could not be distinguished on the basis of our data, and we have removed the term "best-performing" from the Abstract.
>
> **Reviewer 1 · Comment 2**
>
> Contamination of pretraining data could explain some of the differences between models.
>
> **Response**
>
> We acknowledge this possibility, which we had noted briefly in the Methods. Because pretraining corpora are not fully documented, we cannot rule it out. We have therefore expanded the Discussion (page 10, lines 4–11) to describe the possible direction of this bias and to propose a check using documents published after the release of the evaluated models.
>
> **Reviewer 2 · Comment 1**
>
> Why were only six models evaluated? Larger models are widely available.
>
> **Response**
>
> We appreciate this question. Our study was designed for settings in which models must run on local hardware under data-security constraints, and we therefore restricted the evaluation to models with fewer than 600 million parameters. We have clarified this rationale in the Introduction (page 2, lines 20–24). We respectfully note that including larger models would address a different question; however, we agree that it would be informative and have added it as a direction for future work.
>
> **Reviewer 2 · Comment 2**
>
> Kendall's tau computed from six models is unstable.
>
> **Response**
>
> We fully agree. In the revised manuscript, we report the tau values together with bootstrap confidence intervals and have softened our interpretation accordingly (page 8, lines 3–9).
>
> We believe these revisions have strengthened the manuscript and hope that it is now suitable for publication.

---

## 1회차 · 청크 단위 직독직해

> 영어 어순 그대로 앞에서부터 의미를 받아들이는 것이 목표입니다. 한국어 번역도 영어 순서를 따릅니다.

### 문단 1

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| We thank the editor | 우리는 편집자에게 감사한다 |  |
| and the reviewers | 그리고 심사위원들에게 | reviewer 심사위원 |
| for their careful reading | 그들의 꼼꼼한 검토에 대해 |  |
| of our manuscript | 우리 원고의 |  |
| and for their | 그리고 그들의 |  |
| constructive comments. | 건설적인 의견에 대해. | constructive 건설적인 |
| We have revised | 우리는 수정했다 | revise 수정하다 |
| the manuscript | 원고를 |  |
| accordingly. | 그에 따라. | accordingly 그에 따라 |
| Below, | 아래에서, |  |
| we respond | 우리는 답한다 | respond to ~에 답하다 |
| to each comment | 각 의견에 |  |
| in turn; | 차례로; | in turn 차례로 |
| changes | 변경 사항은 |  |
| in the manuscript | 원고의 |  |
| are highlighted, | 강조 표시되어 있으며, | highlight 강조 표시하다 |
| and page and line numbers | 그리고 쪽과 줄 번호는 |  |
| refer to | 가리킨다 | refer to ~을 가리키다 |
| the revised version. | 수정본을. |  |

### 문단 2 · Reviewer 1 · Comment 1

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| The authors state | 저자들은 진술한다 |  |
| that Model A | 모델 A가 |  |
| achieved | 달성했다고 |  |
| the best | 최고의 |  |
| monolingual performance, | 단일 언어 성능을, |  |
| but the difference | 하지만 차이는 |  |
| from Model C | 모델 C와의 |  |
| does not appear | ~해 보이지 않는다 |  |
| to be significant. | 유의해. |  |

### 문단 3 · Response

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| We agree | 우리는 동의한다 |  |
| with the reviewer | 심사위원의 의견에 |  |
| and thank them | 그리고 그들에게 감사한다 |  |
| for this observation. | 이 지적에 대해. | observation 지적, 관찰 |
| The difference | 그 차이는 |  |
| between Models A and C | 모델 A와 C 사이의 |  |
| was not | ~이 아니었으며 |  |
| statistically significant, | 통계적으로 유의하지, |  |
| and our original wording | 그리고 우리의 원래 표현은 | wording 표현 |
| could have implied | 암시했을 수 있다 | imply 암시하다 |
| otherwise. | 그렇지 않다고. | otherwise 달리 |
| We have revised | 우리는 수정했다 |  |
| the Results | 결과 절을 |  |
| (page 7, lines 12–15) | (7쪽, 12–15줄) |  |
| to state | 진술하도록 | state 진술하다 |
| that the two models | 두 모델이 |  |
| could not be distinguished | 구별될 수 없었다고 | distinguish 구별하다 |
| on the basis | 근거로 |  |
| of our data, | 우리 자료를, |  |
| and we have removed | 그리고 우리는 삭제했다 | remove 삭제하다 |
| the term | 표현을 | term 용어, 표현 |
| "best-performing" | "최고 성능의"라는 |  |
| from the Abstract. | 초록에서. |  |

### 문단 4 · Reviewer 1 · Comment 2

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Contamination | 오염이 | contamination 오염 |
| of pretraining data | 사전 학습 데이터의 |  |
| could explain | 설명할 수 있다 |  |
| some of the differences | 차이의 일부를 |  |
| between models. | 모델 간의. |  |

### 문단 5 · Response

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| We acknowledge | 우리는 인정한다 | acknowledge 인정하다 |
| this possibility, | 이 가능성을, |  |
| which we had noted | 우리가 언급했었던 | note 언급하다 |
| briefly | 간략하게 | briefly 간략히 |
| in the Methods. | 방법 절에서. |  |
| Because pretraining corpora | 사전 학습 말뭉치가 ~하기 때문에 |  |
| are not fully documented, | 완전히 문서화되어 있지 않기 때문에, |  |
| we cannot rule it out. | 우리는 그것을 배제할 수 없다. | rule out 배제하다 |
| We have therefore expanded | 따라서 우리는 확장했다 | expand 확장하다 |
| the Discussion | 논의 절을 |  |
| (page 10, lines 4–11) | (10쪽, 4–11줄) |  |
| to describe | 기술하도록 |  |
| the possible direction | 가능한 방향을 |  |
| of this bias | 이 편향의 | bias 편향 |
| and to propose | 그리고 제안하도록 |  |
| a check | 점검을 |  |
| using documents | 문서를 사용하는 |  |
| published after the release | 출시 이후에 발표된 |  |
| of the evaluated models. | 평가된 모델들의. |  |

### 문단 6 · Reviewer 2 · Comment 1

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Why were | 왜 ~되었는가 |  |
| only six models | 여섯 모델만 |  |
| evaluated? | 평가되었는가? |  |
| Larger models | 더 큰 모델들은 |  |
| are widely available. | 널리 이용 가능하다. |  |

### 문단 7 · Response

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| We appreciate | 우리는 감사한다 | appreciate 감사하다 |
| this question. | 이 질문에. |  |
| Our study | 우리 연구는 |  |
| was designed | 설계되었고 |  |
| for settings | 환경을 위해 |  |
| in which models | 그 안에서 모델이 |  |
| must run | 실행되어야 하는 |  |
| on local hardware | 로컬 하드웨어에서 |  |
| under data-security constraints, | 데이터 보안 제약하에서, | constraint 제약 |
| and we therefore restricted | 그래서 우리는 제한했다 | restrict 제한하다 |
| the evaluation | 평가를 |  |
| to models | 모델들로 |  |
| with fewer than | ~보다 적은 |  |
| 600 million parameters. | 6억 개 매개변수를 가진. |  |
| We have clarified | 우리는 명확히 했다 | clarify 명확히 하다 |
| this rationale | 이 근거를 | rationale 근거, 이유 |
| in the Introduction | 서론에서 |  |
| (page 2, lines 20–24). | (2쪽, 20–24줄). |  |
| We respectfully note | 우리는 정중히 언급한다 | respectfully 정중하게 |
| that including | 포함하는 것은 |  |
| larger models | 더 큰 모델을 |  |
| would address | 다룰 것이라고 |  |
| a different question; | 다른 질문을; |  |
| however, | 그러나, |  |
| we agree | 우리는 동의한다 |  |
| that it would be informative | 그것이 유익할 것이라는 데 | informative 유익한 |
| and have added it | 그리고 그것을 추가했다 |  |
| as a direction | 방향으로 |  |
| for future work. | 후속 연구의. |  |

### 문단 8 · Reviewer 2 · Comment 2

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| Kendall's tau | 켄달 타우는 |  |
| computed | 계산된 |  |
| from six models | 여섯 모델로부터 |  |
| is unstable. | 불안정하다. | unstable 불안정한 |

### 문단 9 · Response

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| We fully agree. | 전적으로 동의한다. |  |
| In the revised manuscript, | 수정 원고에서, |  |
| we report | 우리는 보고한다 |  |
| the tau values | 타우 값을 |  |
| together with | ~와 함께 |  |
| bootstrap | 부트스트랩 |  |
| confidence intervals | 신뢰구간과 |  |
| and have softened | 그리고 완화했다 | soften 완화하다 |
| our interpretation | 우리의 해석을 |  |
| accordingly | 그에 따라 |  |
| (page 8, lines 3–9). | (8쪽, 3–9줄). |  |

### 문단 10

| 영어 청크 | 직독직해 | 주요 어휘 |
|---|---|---|
| We believe | 우리는 믿는다 |  |
| these revisions | 이 수정 사항들이 |  |
| have strengthened | 강화했다고 | strengthen 강화하다 |
| the manuscript | 원고를 |  |
| and hope | 그리고 바란다 |  |
| that it is now suitable | 그것이 이제 적합하기를 | suitable 적합한 |
| for publication. | 출판에. | publication 출판 |

---

## 2회차 · 문장 단위 직독직해

> 한 문장을 한 호흡에 읽는 연습입니다. 1회차에서 끊었던 지점을 의식하되, 멈추지 않고 이어 읽습니다.

### 문단 1

**① We thank the editor and the reviewers for their careful reading of our manuscript and for their constructive comments.**
원고를 꼼꼼히 검토하고 건설적인 의견을 주신 편집자와 심사위원께 감사드립니다.
어휘: reviewer 심사위원 · constructive 건설적인

**② We have revised the manuscript accordingly.**
의견에 따라 원고를 수정했습니다.
어휘: revise 수정하다 · accordingly 그에 따라

**③ Below, we respond to each comment in turn; changes in the manuscript are highlighted, and page and line numbers refer to the revised version.**
아래에서 각 의견에 차례로 답합니다. 원고의 변경 사항은 강조 표시했으며, 쪽·줄 번호는 수정본 기준입니다.
어휘: respond to ~에 답하다 · in turn 차례로 · highlight 강조 표시하다 · refer to ~을 가리키다

### 문단 2 · Reviewer 1 · Comment 1

**④ The authors state that Model A achieved the best monolingual performance, but the difference from Model C does not appear to be significant.**
저자들은 모델 A가 최고의 단일 언어 성능을 보였다고 기술하지만, 모델 C와의 차이는 유의하지 않아 보입니다.

### 문단 3 · Response

**⑤ We agree with the reviewer and thank them for this observation.**
심사위원의 의견에 동의하며, 이 지적에 감사드립니다.
어휘: observation 지적, 관찰

**⑥ The difference between Models A and C was not statistically significant, and our original wording could have implied otherwise.**
모델 A와 C의 차이는 통계적으로 유의하지 않았으며, 원래 표현은 그렇지 않은 것처럼 읽힐 수 있었습니다.
어휘: wording 표현 · imply 암시하다 · otherwise 달리

**⑦ We have revised the Results (page 7, lines 12–15) to state that the two models could not be distinguished on the basis of our data, and we have removed the term "best-performing" from the Abstract.**
결과 절(7쪽, 12–15줄)을 두 모델이 본 자료로는 구별되지 않는다는 내용으로 수정했고, 초록에서 "최고 성능의"라는 표현을 삭제했습니다.
어휘: state 진술하다 · distinguish 구별하다 · remove 삭제하다 · term 용어, 표현

### 문단 4 · Reviewer 1 · Comment 2

**⑧ Contamination of pretraining data could explain some of the differences between models.**
사전 학습 데이터의 오염이 모델 간 차이의 일부를 설명할 수 있습니다.
어휘: contamination 오염

### 문단 5 · Response

**⑨ We acknowledge this possibility, which we had noted briefly in the Methods.**
이 가능성을 인정합니다. 방법 절에서 간략히 언급했던 부분이기도 합니다.
어휘: acknowledge 인정하다 · note 언급하다 · briefly 간략히

**⑩ Because pretraining corpora are not fully documented, we cannot rule it out.**
사전 학습 말뭉치가 완전히 문서화되어 있지 않아 이 가능성을 배제할 수는 없습니다.
어휘: rule out 배제하다

**⑪ We have therefore expanded the Discussion (page 10, lines 4–11) to describe the possible direction of this bias and to propose a check using documents published after the release of the evaluated models.**
그래서 논의 절(10쪽, 4–11줄)을 확장해 이 편향이 어느 방향으로 작용할 수 있는지 기술하고, 평가 모델 출시 이후에 발표된 문서를 이용한 점검 방법을 제안했습니다.
어휘: expand 확장하다 · bias 편향

### 문단 6 · Reviewer 2 · Comment 1

**⑫ Why were only six models evaluated?**
왜 여섯 모델만 평가했습니까?

**⑬ Larger models are widely available.**
더 큰 모델도 널리 공개되어 있습니다.

### 문단 7 · Response

**⑭ We appreciate this question.**
이 질문에 감사드립니다.
어휘: appreciate 감사하다

**⑮ Our study was designed for settings in which models must run on local hardware under data-security constraints, and we therefore restricted the evaluation to models with fewer than 600 million parameters.**
본 연구는 데이터 보안 제약 아래 로컬 하드웨어에서 모델을 실행해야 하는 환경을 위해 설계되었으므로, 평가 대상을 매개변수 6억 개 미만의 모델로 제한했습니다.
어휘: constraint 제약 · restrict 제한하다

**⑯ We have clarified this rationale in the Introduction (page 2, lines 20–24).**
이 근거를 서론(2쪽, 20–24줄)에서 명확히 했습니다.
어휘: clarify 명확히 하다 · rationale 근거, 이유

**⑰ We respectfully note that including larger models would address a different question; however, we agree that it would be informative and have added it as a direction for future work.**
더 큰 모델을 포함하는 것은 다른 질문을 다루는 일이라는 점을 정중히 말씀드립니다. 다만 그것이 유익할 것이라는 데 동의하며, 후속 연구 방향으로 추가했습니다.
어휘: respectfully 정중하게 · informative 유익한

### 문단 8 · Reviewer 2 · Comment 2

**⑱ Kendall's tau computed from six models is unstable.**
여섯 모델로 계산한 켄달 타우는 불안정합니다.
어휘: unstable 불안정한

### 문단 9 · Response

**⑲ We fully agree.**
전적으로 동의합니다.

**⑳ In the revised manuscript, we report the tau values together with bootstrap confidence intervals and have softened our interpretation accordingly (page 8, lines 3–9).**
수정 원고에서는 타우 값을 부트스트랩 신뢰구간과 함께 보고하고, 그에 맞춰 해석을 완화했습니다(8쪽, 3–9줄).
어휘: soften 완화하다

### 문단 10

**㉑ We believe these revisions have strengthened the manuscript and hope that it is now suitable for publication.**
이 수정으로 원고가 더 탄탄해졌다고 믿으며, 이제 출판에 적합하기를 바랍니다.
어휘: strengthen 강화하다 · suitable 적합한 · publication 출판

---

## 학술 영어 포인트

### 1. 답변서의 기본 형식

| 요소 | 원칙 | 이 글의 예 |
|---|---|---|
| 서두 | 감사 + 수정 사실 + 표기 방식 안내 | We thank the editor and the reviewers… page and line numbers refer to the revised version |
| 의견 제시 | 심사위원의 의견을 그대로(또는 요약해) 옮김 | Reviewer 1 · Comment 1: The authors state that… |
| 답변 | 수용 여부 → 이유 → 수정 내용 → 위치 | We agree… / We have revised the Results (page 7, lines 12–15)… |
| 마무리 | 수정이 원고를 강화했다는 진술 | We believe these revisions have strengthened the manuscript… |

**수정 위치(쪽, 줄)를 반드시 명시하세요.** 심사위원이 수정 내용을 찾느라 시간을 쓰지 않게 하는 것이 가장 기본적인 예의이자 재심사를 순조롭게 만드는 방법입니다.

### 2. 수용의 정도에 따른 표현

| 수용 정도 | 표현 | 이 글의 예 |
|---|---|---|
| 전면 수용 | We fully agree. / We agree with the reviewer and thank them for this observation. | Comment 1-1, 2-2 |
| 인정 + 한계 설명 | We acknowledge this possibility… we cannot rule it out. We have therefore… | Comment 1-2 |
| 부분 수용 (정중한 반론) | We appreciate this question… **We respectfully note that**… **however, we agree that**… | Comment 2-1 |

Comment 2-1의 답변 구조를 눈여겨보세요. 심사위원의 제안(더 큰 모델 포함)을 받아들이지 않으면서도, ① 질문에 감사하고 ② 설계 근거를 설명하고 ③ 그 근거를 원고에 명확히 반영했으며 ④ 반론은 "respectfully"로 부드럽게 하고 ⑤ 제안의 가치는 인정해 후속 연구로 수용했습니다.

### 3. 피해야 할 방어적 표현

| 피해야 할 표현 | 대안 |
|---|---|
| The reviewer misunderstood our study. | We have clarified this point in the revised manuscript. |
| This is already stated in the paper. | We had noted this briefly in the Methods and have now expanded… |
| This comment is not relevant. | We respectfully note that this would address a different question… |
| We disagree. | We appreciate this suggestion; however… |

심사위원이 오해했다면 그것은 원고가 불분명했다는 뜻으로 받아들이는 것이 생산적입니다. "We have clarified"는 이런 상황에서 가장 유용한 표현입니다.

### 4. 수정이 연쇄적으로 일어나는 방식

| 심사 의견 | 수정된 절 | 시리즈의 대응 편 |
|---|---|---|
| 1-1 유의하지 않은 차이 | 결과 + 초록 | D09 (이미 반영된 형태) |
| 1-2 오염 | 논의 | D06 방법, D12 한계 |
| 2-1 모델 수 | 서론 + 후속 연구 | D03 서론, D12 |
| 2-2 τ의 불안정성 | 결과 | D09 |

한 의견이 여러 절의 수정으로 이어지는 경우가 많습니다. 특히 초록은 결과 표현이 바뀌면 반드시 함께 고쳐야 합니다(1-1의 "best-performing" 삭제).

## 핵심 어휘 정리 (Domain Track 어휘장 D15)

| 어휘 | 뜻 | 어휘 | 뜻 |
|---|---|---|---|
| constructive comments | 건설적 의견 | rule out | 배제하다 |
| revise accordingly | 그에 따라 수정하다 | rationale | 근거 |
| in turn | 차례로 | clarify | 명확히 하다 |
| refer to | ~을 가리키다 | respectfully note | 정중히 언급하다 |
| imply otherwise | 달리 암시하다 | soften the interpretation | 해석을 완화하다 |
| acknowledge | 인정하다 | suitable for publication | 출판에 적합한 |

---

## 낭독 기록표

| 회차 | 날짜 | 소요 시간 | WPM (346 ÷ 분) | 막힌 문장 번호 |
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

*Original essay written for the 30-part reading series. Next: D16. A Conference Presentation Script (연구 전달: 발표 원고)*
