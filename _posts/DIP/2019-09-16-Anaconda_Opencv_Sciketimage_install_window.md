---
title:  "[Anaconda] OpenCV, Scikit image 설치하기 (Windows10)"
last_modified_at:   2019-09-16
author: dsaint31
categories: 
  - DIP
  - Python
use_math: true
tags: 
  - anaconda
  - windows
---

# [Anaconda]
# Anaconda


The open-source Anaconda Distribution is the easiest way to perform Python/R data science and machine learning on Linux, Windows, and Mac OS X. With over 11 million users worldwide, it is the industry standard for developing, testing, and training on a single machine, enabling individual data scientists to:


* Quickly download 1,500+ Python/R data science packages
* Manage libraries, dependencies, and environments with Conda
* Develop and train machine learning and deep learning models with scikit-learn, TensorFlow, and Theano
* Analyze data with scalability and performance with Dask, NumPy, pandas, and Numba
* Visualize results with Matplotlib, Bokeh, Datashader, and Holoviews


* References
  * [Anaconda](https://www.anaconda.com)
  * [Anaconda Cloud](https://anaconda.org/)
    * [Documentation](https://docs.anaconda.com/anaconda/)
    * [Anaconda Cheat Sheet](https://docs.anaconda.com/_downloads/9ee215ff15fde24bf01791d719084950/Anaconda-Starter-Guide.pdf)
  * [Conda](https://docs.conda.io/projects/conda/en/latest/index.html)
    * [Conda Cheat Sheet](https://docs.conda.io/projects/conda/en/latest/_downloads/1f5ecf5a87b1c1a8aaf5a7ab8a7a0ff7/conda-cheatsheet.pdf)
    * Docs > User guide > [Configuration](https://docs.conda.io/projects/conda/en/latest/user-guide/configuration/index.html)


Anaconda의 주요 기능이자 가장 큰 장점 
* Python packages 간의 dependency 관리 
* Python을 이용한 개발을 위한 가상환경 지원.

> 뿐만 아니라, NVIDIA GPU를 기반으로 TensorFlow를 사용하기 위해서는 NVIDIA CUDA 관련 도구(CUDA Toolkit, cuDNN 등)가 필요하지만, Anaconda를 통해서 `tensorflow-gpu`를 설치할 경우 필요한 추가도구의 설치와 환경설정을 자동으로 해준다. TensorFlow가 권장하는 Docker는 Linux에서 최적화가 되어 있으므로, Windows 사용자로서는 Anaconda가 최선의 선택이라고 생각한다.


## Install Anaconda


* Version: Anaconda 2019.07 (Conda 4.7.10)


※ Anaconda Prompt를 실행하기 전에 속성에 들어가서 `시작 위치`를 본인의 workspace로 설정하면, Anaconda를 켤 때마다 매번 이동해야 하는 번거로움을 덜 수 있다.


### 1.Anaconda 설치 [(Installing on Windows)](https://docs.anaconda.com/anaconda/install/windows/)
* [Anaconda 다운로드](https://www.anaconda.com/distribution/#download-section)에서 OS 및 버전(Python, 32-Bit or 64-Bit 등)을 잘 확인하고 다운로드한 후 설치


### 2.Conda 및 root(base) environment의 기본 packages 업데이트


```bash
conda update conda
conda update --all
```


### 3.Create a new environment for DIP

필요한 package가 opencv, matplotlib, scikit-image 정도임.
opencv를 제외하고는 anaconda에서 설치가 되므로 opencv만 지정해준다.

```bash
conda create -n dip python=3.7 anaconda opencv
```


### 4.Activate the environment


```bash
conda activate dip 
```


### 5.Install git 

`git`을 설치.
환경 생성시 설치해도 되지만 여기선 따로 설치를 해봄.

```bash
#conda install opencv scikit-image matplotlib
conda install git
```
