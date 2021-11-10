## nlc_to_nlu_kor 프로젝트 설명

nlc_to_nlu_kor는 기존 Watson NLC의 deprecation으로 Watson NLU 서비스를 NLC와 비슷하게 이용 할 수 있게한 예제입니다.

## 참고한 문서 (refernced documents)

* [NLC 마이그레이션](https://cloud.ibm.com/docs/natural-language-classifier?topic=natural-language-classifier-migrating)
* [ipynb 예제 파일](https://github.com/watson-developer-cloud/doc-tutorial-downloads/blob/master/natural-language-understanding/custom_classifications_example.ipynb)

## 환경

* [Python 3.5 and above](https://docs.python-guide.org/starting/install3/osx/)
* [Jupyterlab: Installation with pip 참고](https://jupyter.org/install)
* [ibm-watson python 라이브러리](https://github.com/watson-developer-cloud/python-sdk)
* [NLU 인스턴스 사전 생성](https://www.ibm.com/cloud/watson-natural-language-understanding)
* CSV 데이터 NLC에서 다운로드 (예제 CSV 파일이 프로젝트에 같이 있습니다.)

## 사용 순서

1. clone 한 폴더에서 아래 커맨드로 Jupyter notebook 열기
```sh
   jupyter notebook
  ```
  
2. nlc_to_nlu.ipynb 파일 열기
3. IBM cloud에서 IAM 키 및 NLU 인스턴스에서 서비스 URL 확인하여 코드상 아래의 키와 URL 부분 입력
```sh
   uthenticator = IAMAuthenticator('IAM API 키')
   
   nlu = NaturalLanguageUnderstandingV1(
         version='2021-03-25',
         authenticator=authenticator
         )
      
   nlu.set_service_url(
         'https://api.kr-seo....NLU 인스턴스 페이지의 URL...')
   ```
4. 순서대로 실행하여 동작 확인
