# 자문 : 취업의 문을 열다

* 자기소개서 기반 모의면접
* 웹사이트 바로 이동(링크)

자문은 자기소개서와 기존 면접 질문 간의 유사도 파악을 통해 얻어진 면접 질문으로 모의 면접 체험을 제공하는 웹사이트입니다. 이 웹사이트는 이화여자대학교 컴퓨터공학 21-2 캡스톤디자인프로젝트 11조 초코칩쿠키의 프로젝트 결과입니다.

### Browser compatibility
다음과 같은 환경에서 사용을 권장합니다.

PC의 경우
* Chrome
* Edge 
* Safari

모바일의 경우
* Chrome
* WebView Android
* Safari on iOS
* Samsung Internet

### Architecture
![구조도](https://user-images.githubusercontent.com/43198971/141683940-5b16e940-d8ec-49c2-b9c6-c489c07ea9ea.png)

프로젝트의 시스템 플로우를 표기한 구조도입니다.

### 핵심 기능
* 입력받은 자기소개서의 각 문장과 기존 면접 질문 간의 유사도를 판별하여 가장 적절한 면접 질문을 추출합니다.
* 사용자가 선택한 면접 유형에 따라 면접 질문을 제시하여 모의 면접을 진행합니다.
* 진행한 모의 면접의 질문과 답변은 텍스트, 음성 파일로 저장되어 사용자가 직접 확인할 수 있습니다.

### 사용 방법
시연 영상 : (유튜브 링크)

(캡쳐본 넣어서 사용법 설명)

### Data
초기 데이터는 잡코리아 크롤링 데이터를 익명화 후 정제하여 수집하였습니다.
* 면접 질문 : 5,690
* 자기소개서 문장 : 15,649

학습을 위해, 수집한 데이터를 tf-idf 알고리즘을 활용하여 유사도를 파악하는 방식으로 [면접 질문-자기소개서 문장] 데이터셋을 제작하였습니다.
* 유사한 데이터쌍 : 141,113
* 유사하지 않은 데이터쌍 : 143,774

### 유사도 모델
자문의 유사도 판단 모델에는 다음과 같은 기술을 사용하였습니다.
* MaLSTM : 코사인 유사도를 대신해 맨하탄 거리(L1)을 이용한 LSTM 모델

### 웹페이지
자문 웹페이지 개발은 다음과 같은 환경에서 진행되었습니다.
* Flask
* jQuery
* HTML5
* CSS
* JavaScript

또한 모의 면접 진행에 사용된 TTS, STT 기술을 위해 다음과 같은 패키지/라이브러리를 이용하였습니다.
* TTS :  
* STT :
