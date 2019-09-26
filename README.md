# Data-Analysis-study-with-Python
데이터 분석 공부를 위한 저장소

- Week1
- To do list
    - 파이썬 스터디 
    - 개발 환경 셋팅
    - cmd 윈도우 + r ->cmd
    - 아나콘다 실행 방법 
    - activate py36
    - jupyter notebook
    - 기온 데이터 분석 시작
    - 서울의 기온 데이터 분석
    - 서울이 가장 더웠던 날은 언제였을까?    
- 요약
    - 모두의 데이터분석 병아리반 독파 
    - 구동 및 첫 시작
    - cmd 실행 -> cd workspace -> cd Data-Analysis-study-with Python -> jupyter note book
    - 모두의 데이터분석 - 기온 공공데이터
    - 기상자료데이터 분석하기 csv(Comma Separated Values)파일(콤마로구분된파일)
    - 컨트롤 + 엔터 =실행 쉬프트+엔터=새로운 셀생성 + 실행
    - 주피터 노트북 파일 저장시 csv파일을 저장한 곳과 같은 폴더에 저장하여야 함
    - 분석 1. 데이터를 읽어온다 2. 순차적으로 최고기온 확인 3. 최고 기온 가장 높았던 날짜의 데이터를 저장 4. 최종 저장된 데이터 출력
    - [대괄호는 리스트], 문자열은 ""로 둘러싸여 있음 
    - 숫자 값이 아닌 문자열 값을 더하거나 크기 비교 할 수 없음 
    - 소수점 있는 실수 float()으로 데이터 변환 
    - 누락된 데이터 임의량 지정
    - '탐색', '비교' 기준 값 설정 새로운 값과 비교 -> '기준이 되는 값'을 저장할 공간인 '변수'가 필요 
- 주요 코드
    - import csv
    - f=open('파일이름.확장자') f는 파일 핸들러 
    - f.close()
    - data = csv.reader(f) 객체생성 
    - header = next(data) 맨 윗줄을 헤더 변수에 저장 
    - for row in data :    
- 질문 모음
    -: 어느곳은 하고 어느곳은 왜 안하는가? -> for문과 if등 반복적 이어지는 과정에서 쓰고 마지막에는 안쓴다 : 이어지는 처음에 한번만 쓴다 
    - 숫자와 문자열 사이 띄어쓰기 없이 붙여 쓸 수 있는 방법은? 
    - cmd에서 cd로 경로 타들어갈때 폴더명 다 안치고 바로 쓰는법 
    - data 폴더안에 쥬피터노트북 하나더 만들기 

- week2
- To do list
    - 데이터시각화(matplotlib)
    - 기본 그래프 그리기
    - 내 생일의 기온 변화를 그래프로 그리기
    - 기온 데이터를 다양하게 시각화하기
- 요약
    - matplotlib 라이브러리 그 중 pyplot 모듈 (matlab과 사용법이 유사)
    - plot (꺽은선 그래프)
    - 첫번째 리스트가 x 두번쨰가 y (리스트가 하나일시는 y축 값으로 입력)
    - x축 데이터와 y축 데이터 개수가 맞지 않으면 에러 발생 
    - 1. 라이브러리 불러오기 import mat-.py- as plt 2. 함수에 데이터 입력 plt.plot([리스트]) 3. 그래프 보여주기 plt.show()
    - 만약 그래프가 안 뜰시 %matplotlib inline 적어준다
    - 그래프 옵션(제목 plt.title('제목'), 범례(label) 데이터 입력란에 쉼표 찍고 label='', 색상 color='', 선모양 linestyle='--', 마커모양, 'r.' , 'g^' ) 
    - 그래프 크기 조절하기 plt.figure(figsize=(10,2)) 인치로 1인치는 2.54cm
    - split을 이용해 나눠서 날짜 데이터 추출 
    - int(정수), float(실수)
    - print(len(result))
    - 히스토그램 plt.hist
    - 주사위 시뮬레이션 random.randint
    - bins 가로축의 개수를 설정하는 속성 
    - 상자그림 plt.boxplot
    - 데이터를 월별로 분류 상자 그림으로 그리기 

- 주요코드
    - import matplotlib.pyplot as plt
    - plt.title('plotting'), plt.plot(), plt.show(), plt.legend(loc=7)
    - loc 범례위치 291 / 6 10 5,7 / 384 
    - plt.figure(figsize=(10,2))
    - plt.rc('font', family='Malgun Gothic')  #대문자로 써주어야 한다. 안써주어도 되는 듯 환경마다 다른 듯 하다 
    - plt.rcParams['axes.unicode_minus'] = False #-안보일시 나타내주는
    - for i in range(5):
    dice.append(random.randint(1,6))
    - plt.hist(result, bins=100, color='r')
    - print(sorted(result)) plt.boxplot(result)
    - import numpy as np
result = np.array(result)
print('1/4:'+str(np.percentile(result,25)))
print('2/4:'+str(np.percentile(result,50)))
print('3/4:'+str(np.percentile(result,75)))  정확한 수치 보기
    - plt.style.use('ggplot') 회색배경 격자 무늬
    - plt.boxplot(day,showfliers=False) 이상치 값 보이지 않게 하기
    - plt.figure(figsize=(10,5), dpi=300) Dots per Inch의 약자이다. 실제 크기 1인치

- 질문 
    - 숫자 데이터 음수 양수 같이 있을때 음만 양으로 바꾸는 법  ABS함수?
    - 그래프의 x축 값 수치는 어떻게 변화 시킬 수 있는가?
    - x축이 문제 주사위 시뮬레이션 히스토그램 칸이 난장판인데 해결방법은?

- week3
- To do list
    
- 요약
    

- 주요코드
   

- 질문 
    - print len 실행시 0으로 나오는 문제 해결에 대해 page126,127,128 
     for i in row[106:]:
                      ^
SyntaxError: invalid syntax 문제...
ValueError: could not convert string to float: '2,387' 흠...


- week4
- To do list
    
- 요약
    

- 주요코드
   

- 질문 

- week5
- To do list
    
- 요약
    

- 주요코드
   

- 질문 

- week6
- To do list
    
- 요약
    

- 주요코드
   

- 질문 

- week7
- To do list
    
- 요약
    

- 주요코드
   

- 질문 

- week8
- To do list
    
- 요약
    

- 주요코드
   

- 질문 

- week9
- To do list
    
- 요약
    

- 주요코드
   

- 질문 

- week10
- To do list
    
- 요약
    

- 주요코드
   

- 질문 

- week11
- To do list
    
- 요약
    

- 주요코드
   

- 질문 

- week12
- To do list
    
- 요약
    

- 주요코드
   

- 질문 

- week13
- To do list
    
- 요약
    

- 주요코드
   

- 질문 

- week14
- To do list
    
- 요약
    

- 주요코드
   

- 질문 

- week15
- To do list
    
- 요약
    

- 주요코드
   

- 질문 
    