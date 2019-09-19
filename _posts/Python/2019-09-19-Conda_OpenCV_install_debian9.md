---
title:  "[Conda] OpenCV, Scikit image 설치하기 (Debian)"
last_modified_at:   2019-09-19
author: dsaint31
categories: 
  - Conda
  - Phython
use_math: true
tags: 
  - anaconda
  - linux
---

# [Conda]

Conda는 Anaconda와 달리 패키지들을 최소한으로 유지한다는 장점이 있다.
실제로 필요한 것만 설치해서 쓸 수 있다는 장점은 용량이나 Docker의 이미지로 환경을 관리할 때 큰 장점이다.


* References
  * [Conda](https://docs.conda.io/projects/conda/en/latest/index.html)
    * [Conda Cheat Sheet](https://docs.conda.io/projects/conda/en/latest/_downloads/1f5ecf5a87b1c1a8aaf5a7ab8a7a0ff7/conda-cheatsheet.pdf)
    * Docs > User guide > [Configuration](https://docs.conda.io/projects/conda/en/latest/user-guide/configuration/index.html)


Conda의 주요 기능이자 가장 큰 장점 
* Python packages 간의 dependency 관리 
* Python을 이용한 개발을 위한 가상환경 지원.

# OpenCV

Linux환경에서 python으로 openCV를 이용시 gtk문제로 인해 cv2.imshow를 사용하지 못하는 경우가 많다.
이를 막기 위해서는 `conda-forge`를 채널로 지정해서 opencv를 설치해야 한다.

### 1.Conda 및 root(base) environment의 기본 packages 업데이트


```bash
conda update conda
conda update --all
```


### 2.Create a new environment for DIP


```bash
conda create -n dip python=3.7 
```

### 3.Activate the environment


```bash
conda activate dip 
```

### 4.Install packages

필요한 package가 opencv, matplotlib, jupyterlab, scikit-image, seaborn, git 설치.

```bash
conda install -c conda-forge opencv matplotlib jupyterlab scikit-image seaborn git
```

### 5.Install libqt5x11extras5

opencv의 마우스 이벤트 등의 GUI 프로그램을 작성할 경우 다음과 같은 에러가 나면서 jupyter lab의 cell의 수행이 중단될 수 있음.

```bash
This application failed to start because it could not find or load the Qt platform plugin "xcb".

Reinstalling the application may fix this problem.
```

이 경우, `apt-get`으로 `libqt5x11extras5`를 설치해주면 해결됨.

```bash
sudo apt-get install libqt5x11extras5
```
