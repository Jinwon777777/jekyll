### 1. 정밀도 / 재현율의 맹점
- 정밀도
	- 확실한 경우만 positive, 나머지 모두 negative
	- TP / FP + TP = 1/1+0 = 100%
- 재현율
	- 모두 다 positive로 예측

### 2. F1 Score
- 정밀도 & 재현율 결합
- ![[스크린샷 2024-01-09 오후 7.33.42.png]]
- 정밀도, 재현율 치우치지 않을때 큰 값.
	- e.g) 0.5, 0.5이면 2, 0.4, 0.6이면 0.48

### 3. ROC 곡선 / AUC
- FPR(False Positive Rate)에 따른 TPR 변화 곡선
- Curve밑의 면적이 AUC
	- AUC가 1에 가까울 수록 좋은 지표
	- 0.5이면 Random![[스크린샷 2024-01-09 오후 7.37.14.png]]
- TPR = TP / (FN + TP) == Recall(재현율)
	- Positive인데 잘 예측한 비율
- FPR = FP / (FP + TN) ->Negative를 잘못 예측한 비유
	- Negative인데 잘못 예측한 비율
	- Threshold가 1이면 FPR은 0, 0이면 1
- Threshold 감소에 따라 Negative를 잘못 예측한 것은 적게 줄어들어야 함