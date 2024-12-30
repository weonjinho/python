# 📆Day3
# 💡함수
# Numpy 함수
* numpy는 파이썬에서 과학 계산을 위한 필수 라이브러리.
* 대규모 다차원 배열과 행렬 연산을 효율적으로 처리하는 기능을 제공하여 데이터 분석에서 널리 사용.

### 특징
|특징|설명|
|:---:|:---:|
|벡터화 연산 | 모델의 성능을 수치로 표현하여 객관적으로 비교 가능.|
|다양한 수학 함수 | 삼각 함수, 지수 함수, 통계 함수 등 다양한 수학 함수를 제공.|
|배열 생성 및 조작 | 다양한 방법으로 배열을 생성하고, shape을 변경하거나 원하는 요소를 추출.|
|선형대수 연산 | 행렬 곱, 역행렬, 고유값 분해 등 선형대수 연산을 지원.|

### Numpy 함수 예시
|함수|설명|예시|
|:---:|:---:|:---:|
|np.array()|리스트를 Numpy 배열로 변환|import numpy as np <br/> arr = np.array([1,2,3]) <br/> arr |
|np.arange()|주어진 범위 내에서 일정한 간격의 값을 가지는 배열 생성| # arange( 시작값, 종료값, 건너뛰기 )<br/>arr = np.arange(0,10,2)&nbsp; # 2씩 증가|
|np.random.rand()|0과 1사이의 균일 분포를 따르는 난수 생성|# np.random : 난수생성, rand : 0~1난수 <br/>arr = np.random.rand(2,3)|
|np.reshape|배열의 shape 변경|arr = arr.reshape(1,9)|
|np.sum()|배열 요소의 합|np.sum([1,2,3])&nbsp;&nbsp;# 출력값 : 6|
|np.mean()|배열 요소의 평균|np.mean([1,2,3])&nbsp;&nbsp;# 출력값 : 2|
|np.std()|배열 요소의 표준편차 계산|np.std([1,2,3])&nbsp;&nbsp;# 출력값 : 0.816|


### 분산과 표준편차 예시
<table>
        <tr>
            <th>구분</th>
            <th>1번</th>
            <th>2번</th>
            <th>3번</th>
            <th>4번</th>
            <th>5번</th>
        </tr>
        <tr>
            <td>변량</td>
            <td>175</td>
            <td>177</td>
            <td>179</td>
            <td>181</td>
            <td>183</td>
        </tr>
        <tr>
            <td>평균</td>
            <td colspan="5">(175 + 177 + 179 + 181 + 183) / 5 = 179</td>
        </tr>
        <tr>
            <td>편차<br/>(변량-평균)</td>
            <td>175 - 179<br/>= -4</td>
            <td>177 - 179<br/>= -2</td>
            <td>179 - 179<br/>= 0</td>
            <td>181 - 179<br/>= 2</td>
            <td>183 - 179<br/>= 4</td>
        </tr>
        <tr>
            <td>편차제곱</td>
            <td>(-4)² = 16</td>
            <td>(-2)² = 4</td>
            <td>0</td>
            <td>2² = 4</td>
            <td>4² = 16</td>
        </tr>
        <tr>
            <td>분산</td>
            <td colspan="5">(16 + 4 + 0 + 4 + 16) / 5 = 40 / 5 = 8</td>
        </tr>
        <tr>
            <td>표준편차</td>
            <td colspan="5">√8 = 2.828</td>
        </tr>
</table>


# Pandas
* Numpy를 기반으로 하여, 표 형태의 데이터를 효율적으로 처리하고 분석할 수 있는 다양한 함수와 자료 구조를 제공.
* Series (1차원 배열과 유사하며, 각 요소에 인덱스 부여), DataFrame (표 형태의 2차원 데이터를 나타내며, 행과 열로 구성.)
* CSV (comma-separated values) : 몇 가지 필드를 쉼표(,)로 구분한 텍스트 데이터 및 텍스트 파일이다.

### 특징
|특징|설명|
|:---:|:---:|
|데이터 읽기/쓰기|다양한 형식의 데이터 ( CSV, Excel, SQL 등 ) 를 읽고 쓸 수 있음|
|데이터 선택 및 필터링|원하는 데이터를 선택하고 조건에 맞는 데이터를 추출할 수 있음|
|데이터 변형|데이터를 정렬, 그룹화, 평균 등 다양한 방식으로 변형할 수 있음|
|결측치 처리|결측치를 찾고 처리하는 다양한 방법을 제공|
|데이터 시각화|Matplotlib와 연동하여 데이터를 시각화할 수 있음|

### Pandas 함수 예시
|함수|설명|예시|
|:---:|:---:|:---:|
|read_csv()|CSV 파일 읽기|df = pd.read_csv('data.csv')|
|head(), tail()|데이터프레임의 처음 또는 마지막 부분 확인|df.head(), df.tail()|
|shape|데이터프레임의 행과 열 개수 확인|df.shape|
|info()|데이터프레임의 요약 정보 확인|df.info()|
|describe()|데이터프레임의 기본적인 통계 정보 확인|df.describe()|
|loc[], iloc[]|데이터 선택|df.loc['index_name'], df.iloc[0]|
|groupby| 데이터 그룹화 | df.groupby('column_name').mean()|
|sort_values()|데이터 정렬|df.sort_values('column_name')|
|fillna()|결측치 체우기|df.fillna(0)|
|dropna()|결측치 행 삭제|df.dropna()|

* 결측치 : 데이터에서 값이 누락되었거나 비어 있는 상태를 의미합니다.
* 처리 방법 :
   1. 삭제 : 결측치가 적은 경우 행 또는 열을 제거.
   2. 대체 : 평균, 중앙값, 최빈값 등으로 결측치를 채움.
   3. 예측 모델 사용 : 머선러닝 알고리즘으로 결측값 예측 후 대체.

# Matplotlib
* 다양한 종류의 그래프를 생성하여 데이터를 시각적으로 표현.
* 데이터 분석 과정에서 얻은 결과를 효과적으로 전달하는 데 사용.

### 특징
|특징|설명|
|:---:|:---:|
|유연성|다양한 종류의 그래프를 생성할 수 있으며, 그래프의 스타일, 크기, 색상 등을 자유롭계 조절할 수 있음.|
|확장성|다양한 서드파티 라이브러리와 연동하여 더욱 복잡하고 정교한 시각화를 구현할 수 있음.|
|객체 지향 인터페이스|그래프의 각 요소(축, 선, 점 등)를 객체로 다루어 세밀하게 조작할 수 있음.|


### Matplotlib 함수 예시
|함수|설명|에시|
|:---:|:---|:---|
|plt.plot()|선 그래프 생성|plt.plot(x, y)|
|plt.scatter()|산점도 생성|plt.scatter(x,y)|
|plt.bar()|막대 그래프 생성|plt.bar(x, height)|
|plt.hist()|히스토그램 생성|plt.hist(data, bins=20)|
|plt.boxplot()|상자 그림 생성|plt.boxplot(data)|
|plt.pie()|원 그래프 생성|plt.pie(x)|
|plt.subplot()|여러 개의 그래프를 하나의 Figure에 배치|plt.subplot(2,2,1)|
|plt.xlabel()|x축 레이블 설정|plt.xlabel('X축 이름')|
|plt.ylabel()|y축 레이블 설정|plt.ylabel('Y축 이름')|
|plt.title()|그래프 제목 설정|plt.title('그래프 제목')|
|plt.legend()|범례 설정|plt.legend()|
|plt.show()|그래프 출력|plt.show()|

* 범례 : 지도, 그래프, 도표 등에 사용된 기호, 색상, 선의 의미를 설명한 표를 가리킵니다.
*        예 : 지도에서 파란색은 강, 초록색은 숲을 나타낸다는 것을 설명하는 부분.

# Seaborn
* Matplotlib을 기반으로 개발된 파이썬 시각화 라이브러리.
* 통계적 시각화를 위한 고급 인터페이스를 제공, Matplotlib보다 더욱 세련되고 통계적인 시각화를 쉽게 만들 수 있다는 장점.

### 특징
|특징|설명|
|:---:|:---|
|고급 인터페이스|Matplotlib의 복잡한 설정 없이 간결한 코드로 다양한 시각화를 생성할 수 있음.|
|통계적인 시각화|데이터 분포, 상관관계, 회귀 분석 등 통계적인 개념을 시각화하는데 특화됨.|
|매력적인 스타일|기본적으로 제공하는 다양한 스타일 테마를 통해 시각적으로 매력적인 그래프를 생성할 수 있음|
|Seaborn과 Pandas의 원활한 통합|Pandas DataFrame을 직접 입력하여 시각화를 수행할 수 있음|

### Seaborn 함수 예시
|함수|설명|예시|
|:---:|:---:|:---:|
|sns.distplot()|히스토그램과 커널 밀도 추정을 함께 표현|sns.distplot(data.kde=True)|
|sns.boxplot()|상자 그림 생성|sns.boxplot(x='category', y='value', data=df)|
|sns.violinplot()|바이올린 플롯 생성|sns.violinplot(x='category', y='value', data=df)|
|sns.scatterplot()|산점도 생성|sns.scatterplot(x='x', y='y', data=df)|
|sns.pairplot()|여러 변수 간의 관계를 한 번에 시각화|sns.pairplot(df)|
|sns.heatmap()|히트맵 생성|sns.heatmap(corr_matrix)|
|sns.Implot()|선형 회귀 모델 시각화|sns.Implot(x='x', y='y', data=df)|

* 동립 변수 & 종속 변수
        동립 변수 ( Independent Variable )
        원인이나 입력 역할을 합니다.
        변경하거나 조작할 수 있는 변수입니다.
* 종속 변수 ( Dependent Variable )
        결과나 출력 역할을 합니다.
        동립 변수에 따라 변하는 변수입니다.

* 예제1 : 공부 시간과 시험 점수
        동립 변수 : 공부 시간(내가 조절할 수 있는 변수)
        종속 변수 : 시험 점수(공부 시간에 따라 달라지는 결과)





