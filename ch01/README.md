## 1장: 컴퓨터는 데이터에서 배운다

**번역서 저장소에 있는 주피터 노트북 대부분은 파이썬 환경을 준비할 필요가 없으며 구글 코랩(Colab)에서 바로 실행할 수 있습니다**

### 기존 콘다(Conda) 사용자: 새로운 콘다 환경 만들기 (선택사항)

이미 콘다를 사용하고 있다면 다음 명령으로 저장소의 `main` 폴더에서 새로운 콘다 환경(`pyml-book`)에 필요한 패키지를 모두 설치할 수 있습니다.

```
make -f Makefile
```

### 파이썬 환경 설정하기 (수동)

이 장에는 코드 예제가 없지만 다음 장을 진행하기 전에 파이썬 환경을 설정하고 확인하는 것이 좋습니다.

자세한 설정 가이드는 1장의 ***파이썬과 PIP에서 패키지 설치*** 절을 참고하세요.

**콘다**

콘다를 사용한다면 다음처럼 새로운 환경을 만들 수 있습니다(콘다는 [Miniforge](https://github.com/conda-forge/miniforge)로 설치하는 것을 추천합니다).

```bash
conda create -n "pyml-book" python=3.9 numpy=1.21.2 scipy=1.7.0 scikit-learn=1.0 matplotlib=3.4.3 pandas=1.3.2
```

환경을 만든 후에 활성화합니다.

```bash
conda activate "pyml-book"
```

**Pip와 virtualenv**

`pip`를 선호한다면 다음 명령으로 필요한 패키지를 설치할 수 있습니다.

```bash
pip install numpy==1.21.2 scipy==1.7.0 scikit-learn==1.0 matplotlib==3.4.3 pandas==1.3.2
```

하지만 새로운 가상 환경을 만드는 것이 권장됩니다. [virtualenv](https://virtualenv.pypa.io/en/latest/)를 사용하여 다음처럼 특정 파이썬 버전을 사용하는 가상 환경을 만들 수 있습니다.

```bash
pip install virtualenv
cd /path/to/where/you/want/your/environment
virtualenv pyml-book
source pyml-book/bin/activate 
```

환경을 활성화한 후 필요한 패키지를 설치합니다.

```bash
pip install numpy==1.21.2 scipy==1.7.0 scikit-learn==1.0 matplotlib==3.4.3 pandas==1.3.2
```

### 파이썬 환경 확인하기

책의 예제를 위해 적절히 파이썬 환경이 구축되었는지 테스트하기 위해 이 저장소의 최상단 폴더에 있는 [`../python_environment_check.py`](../python_environment_check.py) 스크립트를 실행하세요.

다음처럼 `python_environment_check.py` 스크립트를 실행합니다.

    python python_environment_check.py

출력은 다음과 같습니다.

```python
(base) sebastian@MacBook-Air ~/Desktop/Python-Machine-Learning-PyTorch-Edition/ch01 % python ../python_environment_check.py
[OK] Your Python version is 3.9.6 | packaged by conda-forge | (default, Jul 11 2021, 03:35:11)
[Clang 11.1.0 ]
[OK] numpy 1.21.2
[OK] scipy 1.7.0
[OK] matplotlib 3.4.3
[OK] sklearn 1.0
[OK] pandas 1.3.2
```

### 주피터 노트북

이 저장소에 있는 .ipynb 파일은 예제 코드를 담고 있는 주피터 노트북(Jupyter notebook)입니다.

일반적인 .py 스크립트와 달리 주피터 노트북은 여러 가지 내용을 한 파일에 담을 수 있습니다.

- 코드
- 코드 실행 결과
- 그래프
- 막다운(Markdown)과 수식 표현을 위한 레이텍(LaTeX)을 지원하는 문서

최신 버전 설치에 대해서는 https://jupyter.org/install 웹사이트를 참고하세요.

주피터 노트북을 열 수 있는 공식 애플리케이션은 원래 주피터 노트북과 새로운 주피터 랩(Lab) 두 가지 입니다(VS Code도 주피터 노트북을 지원합니다). 이 저장소에 있는 노트북은 두 애플리케이션에서 모두 열 수 있습니다.

다음 명령으로 주피터 랩을 설치할 수 있습니다.

```bash
conda install -c conda-forge jupyterlab
```

또는

```bash
pip install jupyterlab
```