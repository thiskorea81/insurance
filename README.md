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
