```python?code_reference&code_event_index=2
import pandas as pd

# Read the CSV file to inspect its columns
try:
    df = pd.read_csv("insurance.csv")
    print(df.head())
    print(df.info())
except Exception as e:
    print(f"Error reading file: {e}")

```

```text?code_stdout&code_event_index=2
   age     sex     bmi  children smoker     region      charges
0   19  female  27.900         0    yes  southwest  16884.92400
1   18    male  33.770         1     no  southeast   1725.55230
2   28    male  33.000         3     no  southeast   4449.46200
3   33    male  22.705         0     no  northwest  21984.47061
4   32    male  28.880         0     no  northwest   3866.85520
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 1338 entries, 0 to 1337
Data columns (total 7 columns):
 #   Column    Non-Null Count  Dtype  
---  ------    --------------  -----  
 0   age       1338 non-null   int64  
 1   sex       1338 non-null   object 
 2   bmi       1338 non-null   float64
 3   children  1338 non-null   int64  
 4   smoker    1338 non-null   object 
 5   region    1338 non-null   object 
 6   charges   1338 non-null   float64
dtypes: float64(2), int64(2), object(3)
memory usage: 73.3+ KB
None

```

네, 알겠습니다. `insurance.csv` 데이터셋에 대한 `README.md` 파일을 GitHub 저장소 형식에 맞춰 작성해 드릴게요.

-----

# 🩺 의료비(보험료) 예측 프로젝트

개인의 신체 정보, 흡연 여부, 자녀 수 등의 데이터를 바탕으로 의료비(보험료) 지출을 예측하는 머신러닝 모델을 실습합니다.

## 📂 데이터셋

  - `insurance.csv`: 개인별 의료비 지출 데이터
  - **GitHub Repository**: `https://github.com/thiskorea81/insurance.git`

## 📊 속성 정보 (Attribute Information)

| 속성명 (영문) | 속성명 (한글) | 설명 |
| :--- | :--- | :--- |
| `age` | **나이** | 가입자의 나이 |
| `sex` | **성별** | `male`(남성), `female`(여성) |
| `bmi` | **체질량지수** | 체질량지수 (몸무게(kg) / (키(m))^2) |
| `children` | **자녀\_수** | 보험이 적용되는 자녀 또는 부양가족의 수 |
| `smoker` | **흡연\_여부** | `yes`(흡연), `no`(비흡연) |
| `region` | **지역** | 미국 내 거주 지역 (예: `southwest`, `southeast`, `northwest`, `northeast`) |
| `charges` | **의료비(보험료)** | 개인이 지출한 총 의료비 (달러). **(예측 대상)** |

## 🚀 구글 코랩(Google Colab)에서 실행하기

구글 코랩 환경에서 아래 코드를 순서대로 실행하여 데이터를 간편하게 불러올 수 있습니다.

### 1\. GitHub 저장소 복제

`!git clone` 명령어를 사용하여 GitHub에 있는 데이터 파일을 코랩 환경으로 가져옵니다.

```python
!git clone https://github.com/thiskorea81/insurance.git
```

### 2\. Pandas로 데이터 불러오기

저장소 복제가 완료되면, `pandas` 라이브러리를 사용하여 `insurance.csv` 파일을 DataFrame으로 불러옵니다.

```python
import pandas as pd

# 복제된 폴더 안의 파일 경로를 지정합니다.
file_path = '/content/insurance/insurance.csv'

# CSV 파일을 DataFrame으로 읽어옵니다.
df = pd.read_csv(file_path)

# 데이터의 첫 5행을 출력하여 잘 불러왔는지 확인합니다.
df.head()
```
