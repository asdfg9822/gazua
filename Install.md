# 설치 관련 노트

### Anaconda 설치

[Anaconda 설치 링크](https://www.anaconda.com/download/) 다운받아서 설치하면 끝 !

![Anaconda Default Image](images/anaconda_default.jpg)

### Jupyter Notebook 설치
Anaconda Navigator에서 Jupyter notebook의 install 버튼을 눌러주면 설치 끝
설치가 완료되면 Launch 버튼이 보이고 실행하면 아래와 같은 화면이 나온다

![Jupyter Notebook Excute Image](images/jupyter_default.jpg)

### 라이브러리 설치(필요 시)

#### xgboost


1) Jupyter를 이용한 설치
```
!pip install xgboost
```

2) Anaconda Navigator를 이용한 설치
Environments에서 libxgboost, py-xgboost를 설치하면 된다.

만약 xgboost가 정상적으로 설치되지 않을 경우
Anaconda Navigator > Environments에서
blaze 를 삭제(clear) 후 xgboost를 설치하니 잘됐음

![xgboost_install_anaconda_navigator](images/install_xgboost_ana_navi.png)

#### Natural Language Tookit (NLTK)

오래걸릴 수 있음
```
!pip install nltk

import nltk
nltk.download()
```

#### Cython

```
!pip install Cython
```

#### gensim

```
!pip install --upgrade gensim
```

#### tensorflow

*버전 표시*
* 1.x.x-alpha (내부 테스트용으로 배포 하는 경우가 많음)
* 1.x.x-rc (Release Candidate)
* 1.x.x (Release)
* Nightly build 매일 발생하는 수정사항 포함. 테스트가 되어 있지 않을 수 있어 불안정한 상태

*Python Package Manager를 이용한 버전 확인*
```
# To determine which version you're using:
!pip show tensorflow
```

*라이브러리를 이용한 버전 확인*
```
import tensorflow as tf

print(tf.__version__)
```

*버전 install & upgrade*
```
# 최신 버전으로
# For the current version:
!pip install --upgrade tensorflow

# 특정 버전으로
# For a specific version:
!pip install tensorflow==1.2

# nightly build 란
# For the latest nightly build:
!pip install tf-nightly
```