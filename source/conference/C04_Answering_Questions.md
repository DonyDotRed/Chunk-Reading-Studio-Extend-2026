# C04. Answering Questions
### 답변하기: 동의, 부분 동의, 모를 때, 범위 밖 질문, 비판적 질문

| 항목 | 내용 |
|---|---|
| 상황 | 질의응답에서 질문을 이해한 뒤 답변하는 순간 (C03의 다음 단계) |
| 목표 | 30–60초 안에 핵심부터 답하고, 모르는 것은 정직하게, 비판에는 방어하지 않고 응답한다 |
| 연결 자료 | D15 심사 답변서 (같은 태도의 구어 버전), D16 예상 질문 |

---

## 1. 상황

질의응답 답변은 짧을수록 좋습니다. 좋은 답변은 대체로 **짧은 답 → 근거 한두 개 → (필요하면) 한계나 다음 단계**의 세 부분으로 되어 있고, 30–60초 안에 끝납니다. 긴 배경 설명부터 시작하면 질문자와 좌장이 모두 초조해집니다.

질문의 성격에 따라 첫마디가 달라집니다. 동의할 때, 부분적으로만 동의할 때, 모를 때, 연구 범위 밖일 때, 비판적일 때의 패턴을 미리 익혀 두면 당황하지 않고 답할 수 있습니다. 태도는 D15 심사 답변서와 같습니다. 인정할 것은 인정하고, 반론은 근거로 정중하게 합니다.

## 2. 핵심 패턴

### 2-1. 답변의 기본 구조

| 단계 | 패턴 | 예문 |
|---|---|---|
| ① 짧은 답 | Yes. / No. / In short, … / The short answer is… | The short answer is yes, we did. |
| ② 근거 | That's because… / In our data, … | In our data, the ratio stayed close to one for most tasks. |
| ③ 한계·다음 단계 | That said, … / We'd like to look at this in our next study. | That said, we only had one outage, so we'd like to confirm this with more data. |
| 확인 | Does that answer your question? | (답이 길어졌거나 질문이 복잡했을 때) |

### 2-2. 질문 유형별 첫마디

| 유형 | 패턴 | 예문 |
|---|---|---|
| 동의 | You're right that… / I completely agree. | You're right that the sample is small. |
| 부분 동의 | That's partly true, but… / I agree up to a point. | That's partly true, but the ranking change was consistent across both cross-lingual directions. |
| 정중한 반론 | I see your point, but our data suggest… / I'm not sure I'd go that far. | I see your point, but our data suggest the difference is mainly due to geometry. |
| 모를 때 | I'm not sure, to be honest. / I don't know, but my guess would be… | I'm not sure, to be honest, but my guess would be that posture plays a role. |
| 수치가 없을 때 | I don't have that number with me, but I'd be happy to send it to you. | I don't have the exact Recall at one for Model E with me, but I'd be happy to send it to you after the session. |
| 범위 밖 | That's beyond the scope of this study, but… / We didn't look at that, but… | We didn't look at rerankers in this study, but that's a natural next step. |
| 비판적 질문 | I understand your concern. / That's a fair criticism. | That's a fair criticism. Let me explain why we made that choice. |
| 질문이 아닌 의견 | Thank you for the comment. / That's a very helpful perspective. | Thank you for the comment. I agree that contractors are an important group. |
| 자리를 옮기자 | Perhaps we could discuss this in more detail after the session. | That's a complex issue. Perhaps we could discuss it in more detail during the break. |

## 3. 모델 대화: ML 발표 후 까다로운 질문 세 개

> D03·D06·D09의 검색 연구 발표 후 질의응답입니다. Q1–Q3은 서로 다른 청중, P는 발표자입니다.

| # | 화자 | 영어 | 한국어 | 유형 |
|---|---|---|---|---|
| 1 | Q1 | With only six models and three hundred queries, isn't it risky to say that general benchmarks don't predict domain performance? | 모델 여섯 개와 질의 300개로 일반 벤치마크가 분야 성능을 예측하지 못한다고 말하는 건 위험하지 않나요? | 비판 |
| 2 | P | That's a fair criticism, and I agree we should be careful. | 타당한 비판이고, 조심해야 한다는 데 동의합니다. | 비판 → 동의 |
| 3 | P | We're not saying that general benchmarks are useless. | 일반 벤치마크가 쓸모없다는 뜻은 아닙니다. | ① |
| 4 | P | What we saw is that the ranking changed in the cross-lingual setting, and that change was consistent in both directions. | 저희가 본 것은 교차 언어 조건에서 순위가 바뀌었고, 그 변화가 양방향 모두에서 일관되었다는 점입니다. | ② |
| 5 | P | The correlation itself is imprecise with six models, so I'd treat it as a warning sign rather than a firm conclusion. | 모델 여섯 개로 낸 상관계수 자체는 부정확하므로, 확고한 결론이라기보다 경고 신호로 보시는 게 맞습니다. | ③ |
| 6 | Q2 | Did you try adding a reranker? That usually fixes a lot of cross-lingual problems. | 재순위화 모델을 추가해 보셨나요? 그러면 교차 언어 문제가 많이 해결되던데요. | 범위 밖 |
| 7 | P | We didn't look at rerankers in this study, because we wanted to isolate the effect of the embedding model itself. | 이번 연구에서는 임베딩 모델 자체의 효과만 분리해 보고 싶어서 재순위화 모델은 다루지 않았습니다. | 범위 밖 + 이유 |
| 8 | P | But you're right that it's an obvious next step, and we're planning to test it. | 하지만 말씀하신 대로 당연한 다음 단계이고, 시험해 볼 계획입니다. | ③ |
| 9 | Q3 | What was the Recall at one for Model E in the Korean-to-English condition? | 모델 E의 한국어–영어 조건 Recall@1은 얼마였나요? | 수치 질문 |
| 10 | P | I don't have the exact number with me, but it was the lowest of the six. | 정확한 수치는 지금 가지고 있지 않지만, 여섯 모델 중 가장 낮았습니다. | 수치 없음 |
| 11 | P | I'd be happy to send you the full table after the session. | 세션이 끝나면 전체 표를 보내 드리겠습니다. | 다음 단계 |

**주목할 점.** 1번의 비판에 발표자는 방어하지 않고 먼저 인정합니다(2번). 그다음 주장의 범위를 좁히고(3번: 쓸모없다는 게 아니다), 실제로 관찰한 것을 근거로 들며(4번), 마지막으로 해석의 강도를 낮춥니다(5번). D12의 한계 진술을 말로 옮긴 것과 같은 구조입니다. 10번은 모르는 수치를 지어내지 않으면서, 아는 범위(가장 낮았다)까지는 답합니다.

## 4. 드릴

### 4-1. 3단 답변 만들기

아래 질문에 ① 짧은 답 → ② 근거 → ③ 한계·다음 단계로 30–60초 동안 답하고 녹음하세요.

| 질문 | 예시 답안 |
|---|---|
| (EN 연구) Why did you use 70% as the cut-off for time in range? | The short answer is that it's the target recommended by the international consensus. It's also widely used in clinical practice, so the results are easy to interpret. That said, we'd like to look at other cut-offs, for example in older patients, where a lower target is often recommended. |
| (RP 연구) Would your conclusion change for a different type of reactor? | It might. Our fields were dominated by cobalt-60, and the ratio close to one depends on that. In a plant with more beta contamination, we'd expect more cases like the valve work. So I'd be cautious about generalizing beyond our plant. |
| (내 연구) 자기 연구에 대해 예상되는 질문 하나를 쓰고 답해 보세요. | |

### 4-2. 반응 연습: 첫마디 고르기

| 질문 | 유형 | 첫마디 |
|---|---|---|
| Your follow-up period seems quite short for microvascular outcomes. | 비판 (타당) | That's a fair point. / You're right that… |
| So your results show that CGM prevents complications? | 과잉 해석 | I'm not sure I'd go that far. Our study shows an association, not prevention. |
| How does this compare with the data from medical staff? | 범위 밖 | We didn't compare directly, but… |
| I think contractors are the real problem here. (의견) | 질문 아님 | Thank you for the comment. I agree that… |
| What was the exact detection limit? (모름) | 수치 없음 | I don't have the exact figure with me, but… |

## 5. 자주 하는 실수

| 피해야 할 답변 | 더 나은 답변 | 설명 |
|---|---|---|
| I don't know. (단독) | I'm not sure, to be honest, but my guess would be… / I don't know, but it's a good question for future work. | "모른다"에 한 문장을 더하면 성의 있는 답이 됨 |
| Sorry, my English is not good. (답변 전마다) | (바로 답하기) | 사과는 한 번이면 충분하고, 대부분의 청중은 영어 실력보다 내용에 집중함 |
| (배경 설명부터 2분) | The short answer is… | 짧은 답을 먼저 |
| Your question is wrong. / That's not correct. | I see your point, but our data suggest… | 질문자를 틀렸다고 하지 않고 자료로 말함 |
| Yes, but… (모든 답의 시작) | You're right that… / That's partly true, but… | 동의의 정도를 구분해서 표현 |
| (모르는 수치를 짐작으로 말하기) | I don't have that number with me, but I'd be happy to send it to you. | 틀린 수치는 신뢰를 크게 떨어뜨림 |

## 6. 자기 점검

- [ ] 첫 문장에서 짧은 답(Yes/No/In short)을 먼저 했다
- [ ] 답변이 60초를 넘지 않았다
- [ ] 비판적 질문에 방어적 표현 대신 인정 → 범위 조정 → 근거로 답했다
- [ ] 모르는 것은 모른다고 하고, 아는 범위까지만 답했다
- [ ] 연구 범위 밖 질문에는 "다루지 않은 이유"를 한 문장으로 말했다
