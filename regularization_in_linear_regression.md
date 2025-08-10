# Regularization in Linear Regression

## 1. 개요
- **Regularization**: 선형 회귀에서 과적합(overfitting)을 방지하기 위한 기법  
- 모델의 **계수(coefficient)** 크기를 억제하는 **패널티(Penalty)** 를 비용 함수에 추가  
- 목적: 훈련 데이터에 과도하게 적합되는 것을 방지하고, 일반화 성능을 향상  

---

## 2. 수식 형태
- **Regularized Cost Function**  
  $$
  J(\theta) = \text{MSE} + \lambda \cdot \text{Penalty Term}
  $$
  - $\lambda$: 패널티 영향도 조절 하이퍼파라미터  
  - Penalty: 계수 크기 측정 방식 (L1, L2 등)  

---

## 3. 선형 회귀(Linear Regression)
- 예측값:
  $$
  \hat{y} = \theta_0 + \theta_1 x_1 + \theta_2 x_2 + \dots + \theta_n x_n
  $$
- 목표: **MSE** 최소화  
- 패널티 없음 → 잡음(noise)에 민감, 과적합 발생 가능  

---

## 4. Ridge vs Lasso
| 기법 | Penalty Type | 특징 |
|------|-------------|------|
| **Linear Regression** | 없음 | 고신호비(SNR) 환경에서 성능 양호, 잡음에 민감 |
| **Ridge Regression** | L2 (계수 제곱합) | 계수 크기 줄임, 모든 변수 유지 |
| **Lasso Regression** | L1 (계수 절댓값 합) | 일부 계수를 0으로 만듦 → **특징 선택(Feature Selection)** 가능 |

---

## 5. 실험 결과 요약
### Sparse Coefficients (고신호비)
- 세 방법 모두 비제로 계수 정확히 예측  
- Lasso: 제로 계수 완벽 검출  
- Linear, Ridge: 제로 계수 검출 다소 부정확  

### Sparse Coefficients (저신호비)
- Linear: 성능 매우 저하, 큰 오차 발생  
- Ridge, Lasso: 비제로 계수 유사한 수준, Lasso가 제로 계수 검출에 강점  

### Non-Sparse Coefficients (고신호비)
- 세 방법 모두 비제로 계수 예측 잘함  
- Ridge 약간 더 오차 발생, Lasso 제로 계수 검출 우수  

### Non-Sparse Coefficients (저신호비)
- Linear: 성능 저하, 음수 계수 발생  
- Ridge: 비제로 계수 예측에서 Lasso보다 약간 우수  
- Lasso: 제로 계수 검출에서 우위  

---

## 6. 테스트 데이터 예측 비교
- **Lasso**: 실제 값과 예측 값이 45° 이상선에 가깝게 분포 → 예측 정확도 높음  
- **MSE**: Lasso가 Ridge, Linear 대비 약 30배 낮음  

---

## 7. 결론
- **Lasso**: 대부분의 시나리오에서 가장 우수, 특히 특징 선택 필요 시 적합  
- **Ridge**: 모든 변수를 유지하면서 과적합 완화  
- **Linear**: 고신호비 환경에서는 괜찮지만, 저신호비·잡음 환경에서 성능 저하  
- Regularization 기법은 선형 회귀의 과적합 문제 해결 및 일반화 성능 향상에 필수  
