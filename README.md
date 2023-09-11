# san_check_capstone
#산 CHECK

## 날씨를 통한 산악사고 위험도 예측
- 2023 데이터 활용 부산관광 아이디어 공모전 출품작
- 기간: ‘23년 02월 ~ ‘23년 03월(1개월)
- 성과: 117팀 중 동상(3등) 수상 
- Tools: R, Qgis
- 활용 데이터
  - 소방청 산악사고 데이터 (2017~2021)
  - 기상청 종관 기상 관측 정보 데이터(2017~2021)
<br>


## 1️⃣ 개요
날씨에 따른 산악사고 위험도를 예측하고 수치화 하는 플랫폼을 만들어 산악사고를 예방하고, 피해를 줄이고자 한다.

<br>

## 2️⃣ 문제 재정의
날씨에 따른 산악사고 위험도를 산별로 예측하고 학습된 모델과 날씨 데이터를 결합해 당일의 각 산들의 위험도를 수치화하여 지도상에 표시하는 플랫폼을 개발해, 산악사고의 발생을 예측, 피해를 줄이고자 한다.

<br>

## 3️⃣ 과정 

❶문제정의 ❷데이터 수집 및 가공 ❸데이터 분석 ❹모델학습 ❺플랫폼 개발 ❻사업화


### 👤역할
기획, 데이터 수집,데이터 전처리, API 연동 , 모델 개발
<br>

### 🧐 Main Issues
날씨 데이터의 변수들이 많아서 실제로 연관성이 있는 변수들을 골라내는 것이 어려웠습니다.

### 🛠️ Resolved
<img align="left" src="https://user-images.githubusercontent.com/93497667/232210064-895073a8-147d-4e17-a439-cc1645897280.png" alt="image" width="300"/> 다양한 파라미터 사용 사례를 중심으로 자료를 서치하여, NIJ에서 발행한 공간 통계 분석 프로그램의 워크북을 통해 분석 목적에 따른 5가지 커널 함수 선택법을 학습했습니다. 내비게이션 데이터의 분포가 대역폭 전체에 Moderate 한 영향을 미쳐야 한다고 판단해, **예파네치니코프보다 sharp하고 삼중 가중보다 smooth 한 4차 다항 함수를 선택**했습니다. Python의 사이킷런에는 해당 파라미터가 없었기에, Qgis를 활용해 핵심 지역 3곳을 식별했습니다.

<br>

### 🎯 Result
평일 대비 주말 수요를 96.4% 충족하고, 핵심 관광지 16곳에 정차하는 버스 노선을 기획했습니다. 리스크 대응 방안과 고정비와 변동비를 고려한 운송원가 등을 종합적으로 제시했으며, 사업성 측면에서 우수하다는 평가를 받았습니다.
<br>
### ⭐ Learnd Lessons
&nbsp;&nbsp;&nbsp;&nbsp;➊ ggplot의 세부 조건을 조정하며 **시각화**해보는 경험을 하였습니다. 추후에는 Interactive한 대시보드를 만들어 더욱 효과으로 구현할 수 있는 방향으로 도전하고자 합니다. 
<br>
&nbsp;&nbsp;&nbsp;&nbsp;➋ 데이터를 샘플링하며 **시계열**의 특성을 고려할 수 있다면 더 정확한 인사이트를 도출할 수 있을 것이라는 생각을 했습니다. 심사 평가시 같은 피드백을 받은 바, 추후에는 시계열의 특성을 고려한 샘플링 방법을 학습하여 적용해 보는 방향으로 도전해 보고자 합니다.

<br>
<br>

<div class="image-container">
  <img src="https://user-images.githubusercontent.com/93497667/232216526-99e27c85-daac-4a25-b49a-73c3848aaf25.jpg" alt="image"  width="400"/>
  <img src="https://user-images.githubusercontent.com/93497667/232216651-c00ad08b-0d94-43ef-998b-8851b734d169.jpg" alt="image"  width="400"/>
</div>


- [커널밀도분석(KDE)](https://www.notion.so/TMP-e977f66c09ee453b9e2c05d3869ff5e9?pvs=4)


산악사고 예방을 위한
![image](https://github.com/ASJ0211/san_check_capstone/assets/118821779/e617747e-76be-4533-9875-a5dbb964a96d)
![image](https://github.com/ASJ0211/san_check_capstone/assets/118821779/a49ed31c-329a-42d2-bca2-648c467538ae)
![image](https://github.com/ASJ0211/san_check_capstone/assets/118821779/5092e90a-588d-4f8c-a467-b0935fc458e6)

![image](https://github.com/ASJ0211/san_check_capstone/assets/118821779/2678fc3a-7858-4d7f-9e90-f203e8d4f1b7)
![image](https://github.com/ASJ0211/san_check_capstone/assets/118821779/ebc56223-912c-45f4-aa8b-85fb19f808f4)
![image](https://github.com/ASJ0211/san_check_capstone/assets/118821779/a44165aa-76c3-4704-a4da-c3a0535d06f6)

