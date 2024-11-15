# **저출산 원인 분석 프로젝트

<img src="https://github.com/chonny1210/SQL_portfolio/blob/main/PPT/1.png" width="800" height="400">

&nbsp; 



## 📌 프로젝트 개요
🔍 한국은 저출산 문제가 심각한 수준에 이르렀습니다. **합계출산율**은 2022년 기준 0.78명으로, 세계에서 가장 낮은 수준을 기록하고 있습니다. 이 프로젝트는 저출산의 주요 원인을 분석하여, 이를 바탕으로 **정책 제언**을 도출하는 것을 목표로 합니다.


<img src="https://github.com/chonny1210/SQL_portfolio/blob/main/PPT/2.png" width="800" height="400" style="display: block; margin: 0 auto;">
<br>
<img src="https://github.com/chonny1210/SQL_portfolio/blob/main/PPT/3.png" width="800" height="400" style="display: block; margin: 0 auto;">




---



## 📌 관계성 확인:
저출산 문제를 분석하기 위해 4가지 주요 요인을 도출했습니다. 이들은 출산율 감소와 밀접한 연관이 있으며, 각각이 복합적으로 작용하여 저출산 문제를 심화시키고 있습니다.

<div align="center">
    <img src="https://github.com/chonny1210/SQL_portfolio/blob/main/PPT/5.png" width="500" height="400" style="display: block; margin: 0 auto;">
</div>


💸 경제적 부담: 주거비, 교육비, 생활비 등 높은 경제적 부담은 출산에 대한 부정적 인식을 강화합니다.

👩‍🎓 사회적 역할 변화: 여성의 교육 수준 상승과 사회적 역할 확대는 출산보다 개인 경력과 자아 실현을 우선시하는 경향을 증가시켰습니다.

👩‍💼 취업 여건: 고용의 불안정성과 경력 단절 우려는 가임기 여성의 출산 기피 요인으로 작용합니다.

🏡 주거 환경: 높은 주택 가격과 열악한 주거 환경은 출산 의지에 부정적인 영향을 미칩니


---

## 📊 데이터 및 테이블 생성
본 프로젝트에서 사용된 데이터는 **국가통계포털(KOSIS)** 및 **통계청**에서 수집한 자료를 바탕으로 분석을 진행했습니다. 총 **4가지 주요 카테고리**로 나누어 데이터 탐색 및 분석을 수행하였습니다.

| 항목               | 데이터                                      | 주요 컬럼                        |
|--------------------|-------------------------------------------|---------------------------------|
| 💸 **경제적 부담**    | 시·군·구 연령 사업장 규모별 분만 연수         | 사업장 규모, 연령, 지역, 년도       |
| 👩‍🎓 **사회적 역할 변화** | 교육 수준별 인구 수                        | 최종 학력, 미혼율, 성별, 년도       |
| 👩‍💼 **취업 여건**    | 경제활동인구, 고용 여부별 통계               | 실업률, 고용률, 년도               |
| 🏡 **주거 환경**    | 부동산 소비 심리지수                         | 소비 심리지수, 지역, 년도           |

### 📊 데이터 수집 및 분석 방법
- **경제적 부담**: 시·군·구 및 사업장 규모별로 **분만 연수**를 분석하여 경제적 요인이 출산율에 미치는 영향을 파악했습니다.
- **사회적 역할 변화**: **교육 수준**과 **미혼율** 간의 관계를 분석하여 여성의 학력 수준 상승이 출산율에 미치는 영향을 도출했습니다.
- **취업 여건**: **경제활동 참가율**과 **실업률** 데이터를 활용하여 **고용 상태와 출산율의 관계**를 분석했습니다.
- **주거 환경**: **부동산 소비 심리지수**를 통해 **주택 가격 상승과 출산율 감소**의 상관관계를 탐색했습니다.


---


#### 📊 **분석 결과 시각화**

### 1. **<사업장 규모별 출산 수 분석>**
이 그래프는 **2014년부터 2022년까지 사업장 규모별 출산 수의 변화를** 보여줍니다.
![사업장 규모별 출산율 변화](https://github.com/chonny1210/SQL_/blob/main/graph/%EC%82%AC%EC%97%85%EC%9E%A5%EA%B7%9C%EB%AA%A8%EB%B3%84%EC%B6%9C%EC%82%B0%EC%88%98.png)


#### 🔍 주요 인사이트:
- **1-99명 규모의 사업장**에서 출산 수가 가장 크게 감소했습니다. 
  - 2014년 약 **139,000명**이었던 출산 수는 2022년 **80,971명**으로 급격히 줄어들었습니다.
- **100-499명 규모의 사업장**에서도 출산 수가 감소하는 경향을 보였으며, 2014년 **55,923명**에서 2022년 **30,034명**으로 줄어들었습니다.
- **500-999명 규모의 사업장**은 2014년 **23,920명**에서 2022년 **15,105명**으로 출산 수가 줄어들었습니다.
- **1,000명 이상의 대규모 사업장**에서는 출산 수 감소폭이 비교적 적어 **82,688명**에서 **51,984명**으로 감소했습니다.

#### 📌 인사이트 요약:
- **소규모 사업장일수록 출산율이 급격하게 감소**하는 경향이 뚜렷합니다. 이는 소규모 사업장에서 **경제적 지원이 부족**하고, **육아 및 출산 지원 정책이 미비**하기 때문일 가능성이 큽니다.
- 대규모 사업장에서도 출산 수 감소가 나타났지만, 감소폭은 상대적으로 적었습니다. 이는 **대규모 사업장에서 더 나은 육아 지원 정책**이 제공되기 때문으로 추정됩니다.

### 2. **<2015년 대비 2022년 출산율 변화 - 사업장 규모별>**
이 그래프는 **2015년 대비 2022년 출산율 변화율을 사업장 규모별로** 보여줍니다.

![2015년대비 2022년 출산](https://github.com/chonny1210/SQL_/blob/main/graph/2015%EB%85%84%EB%8C%80%EB%B9%842022%EB%85%84%EC%B6%9C%EC%82%B0%EC%9C%A8.png)

#### 🔍 주요 인사이트:
- **1-99명 규모의 사업장**에서 출산율이 **-41.75%** 감소하여 가장 큰 감소폭을 보였습니다.
- **100-499명 규모의 사업장**에서는 **-46.29%**로 더욱 급격한 감소를 보였습니다.
- **500-999명 규모의 사업장**에서는 **-39.93%** 감소하였으며, 이 또한 큰 감소폭을 기록했습니다.
- **1,000명 이상의 대규모 사업장**에서는 **-37.13%**의 감소율을 보였습니다.

#### 📌 인사이트 요약:
- **소규모 사업장일수록 출산율 감소폭이 더 큽니다.** 이는 소규모 사업장에서 근로자들이 **출산과 육아를 병행하기 어려운 근무 환경**과 **지원 부족**으로 인해 출산을 기피하게 되는 결과를 반영합니다.
- 대규모 사업장에서는 비교적 안정된 **육아 지원 제도**가 출산율 감소폭을 줄이는 데 기여한 것으로 보입니다.


### 2.2 👩‍🎓 **사회적 역할 변화 분석**
**여성의 학력 수준이 높아질수록 미혼율 증가**  
📈 2000년과 2020년을 비교했을 때, **여성의 대학원 진학률이 455% 증가**했습니다.

#### 📊 **분석 결과 시각화**
![학력과 미혼율 관계](./images/social_role_change.png)

---

### 2.3 👩‍💼 **취업 여건 분석**
**여성 경제활동 참가율 증가**  
🔍 여성의 경제활동 참가율이 증가하고 있지만, 출산율은 감소하고 있습니다.

#### 📊 **분석 결과 시각화**
![여성 경제활동과 출산율](./images/employment_analysis.png)

---

### 2.4 🏡 **주거 환경 분석**
**부동산 소비 심리지수와 출산율 관계 분석**  
🏙️ 대도시에서 **부동산 소비 심리지수**가 감소함에 따라 출산율 또한 급감하는 추세를 보였습니다.

#### 📊 **분석 결과 시각화**
![부동산 심리지수와 출산율](./images/housing_analysis.png)

---

## 📝 **결론 및 정책 제언**
### 🔑 **주요 인사이트**
1. 💸 **경제적 부담 완화**: 소규모 사업장에 대한 출산 장려책 필요.
2. 👩‍🎓 **여성의 사회적 진입 촉진**: 고학력 여성들이 출산과 경력을 양립할 수 있도록 지원.
3. 👩‍💼 **취업 여건 개선**: 여성 고용의 질을 개선하고, 출산을 장려할 수 있는 정책 필요.
4. 🏡 **주거 환경 개선**: 젊은 세대가 주거 부담 없이 출산을 계획할 수 있도록 공공 주택 공급 확대.

