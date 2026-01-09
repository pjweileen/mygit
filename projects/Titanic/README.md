
## 🔍 Analysis Summary

### 🎯 Objective
Titanic 데이터에서 성별, 객실 등급, 나이 등의 변수가 생존(Survived)에 미친 영향을 파악하고,
기본 전처리/시각화로 주요 패턴과 인사이트를 도출한다.

### 📘 Data
- Source: Kaggle – Titanic (train.csv)
- Rows: 891, Target: `Survived` (0/1)
- Key columns: `Pclass`, `Sex`, `Age`, `Fare`, `SibSp`, `Parch`, `Embarked`, `Cabin`

### 🛠 Methods (EDA Steps)
- 결측치 확인: `Age`, `Cabin`, `Embarked` 결측 다수
- 기본 통계: `describe(include="all")`
- 단변량/이변량 분석: 성별·객실 등급·나이 구간별 생존률 비교
- 시각화: Bar plot, Histogram, Heatmap

### 📈 Key Findings (핵심 인사이트)
- **성별:** 여성 생존률이 남성 대비 크게 높음 (예: Female ≈ 74%, Male ≈ 19%)
- **객실 등급:** 1등석 생존률 > 2등석 > 3등석 (Pclass와 생존 간 강한 연관)
- **나이:** 10세 이하 생존률 상대적으로 높음, 성인은 성별/등급에 따라 차이
- **운임(Fare):** 높은 운임일수록 생존률 증가 경향
- **결측:** `Cabin`은 결측이 많아 존재 여부(HasCabin)로 파생변수 고려

### 🖼 Visuals (Notebook에서 상세)
- Survival by Sex / by Pclass (Bar)
- Age Distribution (Hist)
- Correlation Heatmap (numeric)

### 🚀 Next Steps
- Title(Mr/Mrs/Miss/Master) 파생변수 생성
- FamilySize, IsAlone, HasCabin 변수 추가
- Age/Embarked 결측치 보정
- Logistic Regression 베이스라인 모델 → 교차검증