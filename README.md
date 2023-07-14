# StockAutoTrader | 주식 자동매매 시스템


<!-- ############################################################ -->
## 개요

주식 자동매매 시스템의 프로젝트의 원본 레포지토리는 KiwoomTraderV2 입니다.
내부 알고리즘을 공개할 수 없기 때문에 KiwoomTraderV2 프로젝트는 비공개입니다. 

따라서, 본 'StockAutoTrader' 레포지토리는 트레이딩 알고리즘을 제외한 데이터 분석 결과의 시각화 산출물을 외부에 공개하는 것만을 목적으로 합니다.
(현재 포트폴리오 구성 목적으로 지속적으로 빌드업/업데이트 중이니 양해바랍니다)

웹페이지를 통한 데이터 시각화는 구축 예정입니다. (서버 비용 문제로 완성도 80% 수준까지 올라왔을 때 공개 예정) 그전까지는 Jupyter 환경에서 이용바랍니다.


StockAutoTrader 프로젝트에 대한 간략한 설명은 다음과 같습니다.

1. KiwoomTraderV2 프로젝트의 내부 패키지를 직접 임포트하지 않고 일부 시각화 소스코드만 복사해서 재사용합니다.

2. KiwoomTraderV2 에서 자제 분석 완료한 데이터를 외부파일형태(JSON 또는 CSV) 로 변환하여 제공합니다. 원본 데이터는 제공하지 않으며 분석하여 재생성된 데이터만 시각화를 위해 제공합니다.



<!-- ############################################################ -->
## 환경설정

Python 3.9 이상에서 Jupyter Notebook 을 통해 분석 결과를 확인하실 수 있습니다. 

### 파이썬64비트 가상환경 구성

1. python3.9이상-64bit Installer 로 설치

    https://www.python.org/downloads

2. Pythin Virtual Environment 구성

    https://docs.python.org/3/tutorial/venv.html

3. 필수 패키지 설치

    pip install -r requirements.txt




### 쥬피터 환경설정 (64비트 환경에서만 사용)

1. 커멘드라인에서 글로벌환경에서 한번만 쥬피터 설치

    pip install jupyter

2. 가상환경 커멘드라인에서 ipykernel 설치

    pip install ipykernel

3. 가상환경 커멘드라인에서 새로운 가상환경 쥬피터를 설치

    python -m ipykernel install --name=YOUR_ENV_NAME

4. 파일탐색기에서 C:\ProgramData\jupyter\kernels\YOUR_ENV_NAME 로 이동

5. kernels.json 파일에서  python.exe 경로 수정

    {
        "argv": [
            "{YOUR_DOWNLOAD_PATH}\\StockAutoTrader\\YOUR_ENV_NAME\\Scripts\\python.exe",
            "-m",
            "ipykernel_launcher",
            "-f",
            "{connection_file}"
        ],
        "display_name": "YOUR_ENV_NAME",
        "language": "python"
    }

6. 관리자권한으로 커멘드라인에서 노트북 실행

    jupyter notebook

7. 노트북에서 커널 변경

    메뉴 / Kernel / Change kernel