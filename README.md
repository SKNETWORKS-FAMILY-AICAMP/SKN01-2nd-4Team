<div align="center">
    <img src="https://capsule-render.vercel.app/api?type=waving&color=black&height=240&text=SKN01-2nd-4Team&animation=&fontColor=ffffff&fontSize=90" />
</div>
<div align="center">
    <h1><span style="color:pink;">👟it_shoe</span></h1>
    <div><strong>박윤서 민경원 이근 한병찬</div></strog>
    <br><br><br>    
</div>
<div align="center">
    <h2>👨🏻‍💻Tech Stacks</h2>
    <div>
      <img src="https://img.shields.io/badge/Discord-5865F2?style=flat&logo=Discord&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/Git-F05032?style=flat&logo=Git&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=GitHub&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/Slack-4A154B?style=flat&logo=Slack&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/Notion-000000?style=flat&logo=Notion&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/Django-092E20?style=flat&logo=Django&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/PyCharm-000000?style=flat&logo=PyCharm&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=Python&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/Vue.js-4FC08D?style=flat&logo=Vue.js&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/Vuetify-1867C0?style=flat&logo=Vuetify&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=TypeScript&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/VS%20Code-007ACC?style=flat&logo=Visual%20Studio%20Code&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/Axios-5A29E4?style=flat&logo=Axios&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/FastAPI-009688?style=flat&logo=FastAPI&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/Redis-DC382D?style=flat&logo=Redis&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=Docker&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/Machine%20Learning-FF6F00?style=flat&logo=Artificial%20Intelligence&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/Deep%20Learning-003B57?style=flat&logo=Deep%20Learning&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=TensorFlow&logoColor=white" align="left"/>
      <img src="https://img.shields.io/badge/Keras-D00000?style=flat&logo=Keras&logoColor=white" align="left"/>
    </div>
</div>
<br><br>



# SKN01-2nd-4Team
SK Networks Family AI Camp 과정 2차 프로젝트 : Vue + Django + FastAPI 기반 가입 고객 이탈 예측 및 구매 동향 예측  



# 1. 팀 소개
- 팀명 : 이슈이슈
- 멤버 개인 깃허브 계정과 연동

# 2. 프로젝트 개요
- 프로젝트 명 : it_shoe
- 프로젝트 소개 : 러닝유저들을 위한 러닝화 쇼핑 플랫폼 통한 가입 고객 이탈 예측 및 구매 동향 예측
  
- 프로젝트 필요성(배경)
  ![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/eba0767d-c69f-4fb3-ad68-e4ae02e6736e)

- 프로젝트 목표 : 가입 고객 이탈 예측 및 구매 동향 예측

# 3. ⚙️기술 스택
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/506675ed-74f3-46ae-9acc-e53b05b138ee)

# 4. 가설과 가설 검정

- 가설1: 남자 회원이 여성 회원 보다 많을 것이다.
- 가설2: 남성 회원이 여성 회원 보다 대체적으로 구매량이 더 많을 것이다
- 가설3: 나이가 젊을수록 러닝화 구매량이 가장 많을 것이다.
- 가설4: 회원가입 시점과 최근 접속 시점 사이가 짧을수록(= 자주 접속할수록) 회원 이탈률이 낮을 것이다.
- 가설5: 기대수익이 높은 회원일수록 회원 이탈률이 낮을 것이다

<br>아래와 같은 자료를 통해 가설1, 가설2 검증<br>
![image](https://github.com/user-attachments/assets/d6d060b4-e9ab-47ea-94f4-b8b4ea59beba)
![image](https://github.com/user-attachments/assets/bfe65672-84d8-4972-b204-e395633c7572)

<br>아래와 같은 자료를 통해 가설3 검증<br>
```
from datetime import datetime

# 현재 연도
current_year = datetime.now().year

# 나이 계산
data['age'] = current_year - data['birth_year']

# 나이대별 구매량 집계
age_group_quantity = data.groupby('age')['quantity'].sum()

# 시각화
plt.figure(figsize=(12, 6))
age_group_quantity.plot(kind='line', marker='o')
plt.title('Total Quantity Purchased by Age')
plt.xlabel('Age')
plt.ylabel('Total Quantity Purchased')
plt.grid(True)
plt.show()
```
![image](https://github.com/user-attachments/assets/6bc55fd4-d976-4e89-a076-cdd7271778c6)


![image](https://github.com/user-attachments/assets/921c7cfa-a000-4f0f-95a6-fadf919f66cc)
![image](https://github.com/user-attachments/assets/1b22480b-c560-48d9-94be-0ab2c6a26075)
![image](https://github.com/user-attachments/assets/0208e3c4-f78d-4138-b60f-e4565d0795a1)

<br>

![image](https://github.com/user-attachments/assets/ba40b1b5-7705-465b-8962-f97ee8e04588)
<br>
![image](https://github.com/user-attachments/assets/7e679596-616b-4da1-9a26-1e9d64769080)
<br>
해석:
상관관계 히트맵은 각 변수 간의 상관관계를 보여줍니다.
색상의 강도와 색조를 통해 변수 간의 상관계수의 크기와 방향을 알 수 있습니다.
quantity와 total_price는 강한 양의 상관관계(상관계수 ≈ 0.8)를 보이며, 이는 구매량이 많을수록 총 구매 금액이 높아진다는 것을 의미합니다.
age와 total_price는 약한 음의 상관관계(상관계수 ≈ -0.2)를 나타내어, 나이가 많을수록 총 구매 금액이 약간 낮아질 가능성을 시사합니다.
gender와 다른 변수들 간의 상관관계는 대부분 낮거나 미미한 값을 보여, 성별과 다른 변수들 간의 직접적인 연관성은 적다고 해석할 수 있습니다.

![image](https://github.com/user-attachments/assets/2618ffbf-6036-428f-910d-fe1d4637367e)
<br>

해석:
PCA(주성분 분석) 결과는 고차원의 데이터를 2차원 공간으로 투영하여, 데이터의 주요 변동성을 설명하는 두 개의 주성분을 보여줍니다.
주성분 1(PC1)은 전체 변동성의 약 48.0%를 설명하고, 주성분 2(PC2)는 약 25.1%를 설명하여, 두 주성분이 전체 변동성의 73.1%를 설명합니다.
시각화된 그래프에서 각 점은 한 회원을 나타내며, 성별에 따라 색상으로 구분되어 있습니다.
대부분의 데이터가 PC1 방향으로 넓게 분포되어 있으며, 이는 PC1이 데이터의 주요 변동성을 포착하고 있음을 시사합니다.
성별에 따라 군집화된 경향은 크게 보이지 않지만, PCA를 통해 주요 변동성을 설명할 수 있는 변수를 파악하는 데 유용합니다.
<br> 

# 5. Agile Board (애자일 보드)
## WBS를 Agile Board(애자일 보드) 로 변경
```c
실제로 우리는 수업 초반부터 프로세스를 학습하여
과정 전반에 걸쳐 애자일 프로세스를 사용하며 Backlog를 작성하고 있습니다.
그러므로 폭포수 방식의 WBS 보다는 저희가 사용하는 애자일 프로세스에 맞게
애자일 보드의 Status View와 Domain View를 위주로 업로드하기로 하였습니다.
```
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/ebe92f54-e933-417a-9467-ca185f83aa57)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/3a41c2a9-73bd-498e-bd17-ad9ed56cff19)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/df30e61a-e3a2-4c7f-9431-353c49f0efb7)

# 6. Commit History (커밋 이력)
https://github.com/EDDI-RobotAcademy/EES-Django-Backend/commits/main/ <br>
https://github.com/EDDI-RobotAcademy/EES-Vue-Frontend/commits/main/ <br>
https://github.com/EDDI-RobotAcademy/EES-FastAPI-AI/commits/main/

# 7. 발생한 이슈 내역  
![image](https://github.com/user-attachments/assets/35d00105-c105-409a-86b6-e395f23ab96d)
![image](https://github.com/user-attachments/assets/7167b592-9f88-48f1-9a3e-1108e92db1e6)
![image](https://github.com/user-attachments/assets/e6cde16b-088e-436d-8e11-a6f7e0c0ba8b)

# 8. ERD
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/71b10ee9-53aa-413f-bdc9-ea9814f6ec0b)

# 9. 주요 Domain 요소들
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/ebe92f54-e933-417a-9467-ca185f83aa57)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/3a41c2a9-73bd-498e-bd17-ad9ed56cff19)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/df30e61a-e3a2-4c7f-9431-353c49f0efb7)

# 10. 수행결과(테스트/시연 페이지)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/5ce98d93-99f1-4eba-a282-e50bf117db17)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/3b19fab3-10e5-487a-9a5e-239c3e9acd6b)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/3369b2c7-ca6e-4b6d-8c71-564793577172)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/6d9ab801-dde9-4133-98a6-4eff9bb38b1a)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/c855e2c9-98af-43f8-84cc-f6a2958fa7bb)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/a67ab61b-7524-497e-a3d9-d1eaf0a76115)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/f749a9c0-f368-4b69-9218-2b8bb3e6c88c)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/c6a75f2e-35e8-49ee-9ede-fbc033d14710)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/ce40a619-6c27-4ad2-915e-0f612a369e67)

![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/b9d283f5-5af3-4a66-8e64-6de4c391ce4d)
![image](https://github.com/user-attachments/assets/3a866f25-ad61-442a-ad4b-dd5d9f2dcfd6)

![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/93979341-c087-4baa-93f7-e55183e955e3)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/0243d934-984b-4298-9563-d22c42cb52d5)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/319b2a53-2798-4b9d-ae2a-5dd2cdd318ab)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/406b77da-1e0a-4c96-9507-e024e9426ba0)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/fc95d742-0b18-4b63-b191-ad3e70d98cac)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/e50e3bce-f867-47a5-be72-8d70693fed43)
![image](https://github.com/SKNETWORKS-FAMILY-AICAMP/SKN01-2nd-4Team/assets/138251577/fe33f557-662d-4422-98d9-f8e8d63852cc)



# 10. 한 줄 회고
4팀 모두 수고하셨습니다! 많이 배워갑니다!
