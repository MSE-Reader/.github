# READER

  READER는 사용자가 같은 양식의 문서를 분석하고 원하는 지표들을 추출하여 주기적으로 분석할 수 있도록 도와주는 웹 애플리케이션입니다. 사용자는 학습용 문서를 제공하고 원하는 지표들을 지정한 후, 추출용 문서를 입력하여 해당 지표들을 엑셀 파일로 정리해서 반환받을 수 있습니다. 또한, 학습된 지표들을 바탕으로 챗봇을 통해 분석할 수 있습니다.

## 주요 기능
- **회원가입 및 로그인**: 사용자는 먼저 계정을 생성하고 로그인하여 애플리케이션에 접속합니다.
- **학습하기**: 학습할 파일을 입력하여 키-밸류 형태의 지표를 설정합니다.
  - Azure OCR을 사용하여 문서의 문자들을 인식합니다.
  - 사용자는 인식된 문자 중 원하는 부분을 'Key'와 'Value'로 설정합니다.
  - 여러 장의 문서에 대해 동일한 지표를 학습시킵니다.
- **모델 학습**: 설정된 키-밸류 페어를 바탕으로 머신러닝 모델을 학습시킵니다.
- **추출하기**: 학습된 모델을 사용하여 새로운 문서에서 지표를 추출하고 엑셀 파일로 반환합니다.
- **챗봇 분석**: 학습된 지표를 바탕으로 사용자와 대화하며 분석 결과를 제공합니다.

## 사용 방법

### 회원가입 및 로그인
1. 웹사이트에 접속하여 회원가입 페이지에서 계정을 생성합니다.
2. 생성한 계정으로 로그인합니다.

### 학습하기
1. 학습하기 페이지에서 학습할 파일을 순차적으로 업로드합니다.
2. 업로드한 파일은 Azure OCR을 통해 문자 인식이 수행됩니다.
3. 인식된 문자들 중 '키'에 해당하는 값을 직접 타이핑해 입력하고, '밸류'에 해당하는 지표들을 마우스 박스 클릭을 통해 선택합니다.
4. 설정된 키-밸류 페어를 저장합니다.
5. 정확도를 위해 여러 장의 문서에 대해 동일한 작업을 반복합니다.
6. 충분한 양의 학습 데이터를 설정한 후, '학습하기' 버튼을 눌러 머신러닝 모델 학습을 시작합니다.

### 추출하기
1. 학습이 완료되면 추출하기 페이지에서 새로운 문서를 업로드합니다.
2. '엑셀 다운로드' 버튼을 눌러 학습된 지표가 추출된 엑셀 파일을 다운로드받습니다.

### 챗봇 사용
1. 챗봇을 통해 학습된 지표를 바탕으로 분석을 요청합니다.
2. 예를 들어, "올해 매출 분석해줘"와 같은 프롬프트를 입력하면 챗봇이 분석 결과를 제공합니다.

## 기술 스택
- **프론트엔드**: React
- **백엔드**: SpringBoot
- **데이터베이스**: MySQL
- **머신러닝**: Python, TensorFlow
- **OCR**: Azure OCR
---

우리들의 READER는 문서 분석과 지표 추출을 자동화하여 사용자의 효율성을 높이고, 챗봇을 통해 더욱 편리한 분석 환경을 제공합니다.
