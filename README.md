# Korean-MWP-dataset
기학습된 언어 모델을 활용한 수학 문장형 문제 풀이 모델을 위한 한국어 데이터셋

## 목표
본 연구는 한글 수학 문장형 문제(MWP, Math Word Problem)를 푸는 심층신경망 기반 모델을 위한 한국어 데이터셋입니다.  
수학 문장형 문제는 자연어로 구성된 서술형 수학 문제에 대해 풀이과정과 해답을 제시하는 문제입니다.

## 데이터 구성
본 한국어 데이터셋은 json 형식의 dictionary들로 이루어져 있습니다.  
아래는 예시 데이터입니다.
```
"10": {
        "question": "자동차 A는 92km/h로 이동하고 있고 자동차 B는 1500m/min으로 이동하고 있습니다. A와 B 중 어느 차가 더 빠릅니까?",
        "equation_op": "[OP_LIST_SOL] A B [OP_LIST_EOL] [OP_LIST_SOL] 92 1500 1000 [OP_DIV] 60 [OP_MUL] [OP_LIST_EOL] 1 [OP_LIST_MAX] [OP_LIST_INDEX] [OP_LIST_POP] [OP_LIST_GET]",
        "qtype": "크기비교",
        "checked": false,
        "INC": {
            "[N0]": "92",
            "[N1]": "1500"
        },
        "IXC": {
            "[X0]": "A",
            "[X1]": "B"
        },
        "IEC": {},
        "ISC": {
            "[S0]": "자동차"
        },
        "IMQ": "[S0] 자동차 [X0] A는 [N0] 92km/h로 이동하고 있고 [S0] 자동차 [X1] B는 [N1] 1500m/min으로 이동하고 있습니다. [X0] A와 [X1] B 중 어느 차가 더 빠릅니까?",
        "NET": "[OP] [X0] [X1] [OP] [OP] [N0] [N1] [C1000] [OP] [C60] [OP] [OP] [C1] [OP] [OP] [OP] [OP]",
        "template": "[OP_LIST_SOL] [X0] [X1] [OP_LIST_EOL] [OP_LIST_SOL] [N0] [N1] [C1000] [OP_DIV] [C60] [OP_MUL] [OP_LIST_EOL] [C1] [OP_LIST_MAX] [OP_LIST_INDEX] [OP_LIST_POP] [OP_LIST_GET]"
    }
```

## 모델
