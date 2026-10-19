# inhatc2026

pandas·matplotlib 실습 노트북(2026)을 모아 둔 저장소입니다. pandas로 표 데이터를 다루는 방법에서 시작해 matplotlib, seaborn, plotly로 시각화하는 실습 노트북과, 실습에 쓴 데이터 파일 및 conda 사용 메모를 담고 있습니다.

## 내용

### pandas

| 파일 | 내용 |
|------|------|
| `pandas1.ipynb` | DataFrame 만들기, `shape`·`dtypes`·`head`·`tail`, 인덱스 지정(`set_index`·`reset_index`), `loc`·`iloc`·불리언 인덱싱, 연습 문제 |
| `pandas2.ipynb` | 조건을 이용한 행·열 선택, `sort_values`·`sort_index` 정렬, `read_csv` 옵션(특정 열만 읽기, 인덱스 지정, 결측치 처리, 일부 행 읽기·건너뛰기) |
| `pandas3.ipynb` | 결측치(`np.nan`, `None`, `pd.NA`)의 차이, `isnull`·`notnull`, `dropna`(`how`·`thresh`·`subset`·`axis`), `fillna` |
| `pandas4.ipynb` | 리스트 컴프리헨션 복습, `MultiIndex`(Series와 DataFrame), 인덱스 이름, 다중 인덱스와 다중 컬럼의 선택 |
| `pandas5.ipynb` | `merge`와 `join`의 차이, one-to-one·many-to-one·many-to-many 결합, `left_on`·`right_on`, 인덱스 기준 결합, 겹치는 컬럼의 접미사(`_x`, `_y`) |
| `pandas6.ipynb` | `set_index`·`stack`·`unstack`, `groupby`, 그룹별 집계(`aggregate`, `nunique`)와 `filter` |
| `pandas_datetime.ipynb` | `datetime`과 `Timestamp`, 문자열과의 변환(`to_datetime`, `strftime`), `DatetimeIndex`, `date_range`, 날짜 기준 슬라이싱, `Timedelta` |

### matplotlib

| 파일 | 내용 |
|------|------|
| `matplotlib1.ipynb` | Figure의 크기·해상도, `plt.subplots`·`add_subplot`·`add_axes`로 Axes 만들기, 배경색·테두리(spines), `savefig`, 제목·축 이름, 한글 글꼴 설정, 선 그래프, 날짜 눈금(major·minor tick) |
| `matplotlib2.ipynb` | Iris, Titanic, `2019.csv` 데이터를 이용한 실습: 선·막대·산점도·히스토그램·박스플롯·파이 차트 |

### seaborn

| 파일 | 내용 |
|------|------|
| `seaborn1.ipynb` | 예제 데이터셋 불러오기(`load_dataset`), category 타입, 분포 그래프(`histplot`), 관계형 그래프(`scatterplot`, `lineplot`, `relplot`), 색상 팔레트 |
| `seaborn2.ipynb` | 범주형 그래프(`barplot`, `countplot`, `boxplot`, `violinplot`, `stripplot`, `swarmplot`, `pointplot`, `catplot`), `pairplot` |
| `seaborn3.ipynb` | `PairGrid`(대각선·상삼각·하삼각 지정)와 `FacetGrid` |

### plotly

| 파일 | 내용 |
|------|------|
| `plotly.ipynb` | `plotly.express`(`scatter`, `line`, `bar`, `histogram`, `box`, `sunburst`, `treemap`, `icicle`)와 `plotly.graph_objects`(`go.Figure`, `add_trace`, `Sankey`, `Scatterpolar`, `Barpolar`, `Funnel`, `Pie`, `Candlestick`) |

### 데이터와 자료

| 파일 | 내용 |
|------|------|
| `2019.csv` | 국가별 순위·점수와 GDP, 사회적 지지, 기대 수명 등의 항목을 담은 표(156행). `matplotlib2.ipynb`에서 사용 |
| `people_data.csv` | 이름, 성별, 이메일, 생년월일, 직업 컬럼으로 이루어진 예제 표(5행). `pandas2.ipynb`에서 사용 |
| `conda.pdf` | conda 가상환경 만들기·삭제·활성화, 패키지 설치, conda와 pip의 차이, 설치된 패키지 확인, VS Code에서 Jupyter 커널 선택하는 방법 |

## 참고

- 모든 노트북은 Python 3 커널(표시 이름 `py310`)로 저장되어 있습니다. VS Code 또는 Jupyter에서 열 수 있습니다.
- 노트북에서 불러오는 패키지는 `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`이고, `plotly.ipynb`는 `yfinance`로 주가 데이터를 내려받는 셀도 포함하므로 실행하려면 인터넷 연결이 필요합니다. `plotly.ipynb` 상단 셀에는 `plotly`와 함께 `nbformat`도 설치해야 한다는 주석이 있습니다.
- `matplotlib1.ipynb`, `matplotlib2.ipynb`, `seaborn1.ipynb`, `seaborn2.ipynb`, `pandas6.ipynb`에는 실행 결과가 저장되어 있지 않습니다. 그림과 출력을 보려면 직접 실행해야 합니다.
- 한글이 포함된 그래프의 글꼴은 `matplotlib1`, `matplotlib2`, `seaborn1`, `seaborn2`, `seaborn3` 노트북에서 Windows 글꼴인 `Malgun Gothic`으로 설정되어 있습니다.
- `matplotlib2.ipynb`는 실행할 때 Iris와 Titanic 데이터를 URL에서 내려받아 `iris.csv`, `titanic.csv`로 저장합니다. 이 두 파일은 저장소에 포함되어 있지 않습니다.
