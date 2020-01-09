---
title:  "[Etc] Git에서 사용자 확인 및 변경."
date:   2020-01-08 20:33:59
author: dsaint31
categories: Etc
use_math: false
tags: Git
---

# git의 현재 user정보 확인. 
@(Computer)

### user의 ID확인.

```bash
git config user.name
```

### user의 email확인.

```bash
git config user.email
```

### 전체 git의 설정 내용 확인.

```bash
git config --list
```

### user 설정하기

```bash
git config user.name new_id
```
* 위의 command에서 `new_id`를 새로 설정할 id로 변경하여 입력하면 됨.

전역으로 설정하는 경우에는 다음과 같음.

```bash
git config --global user.name new_id
```

### user 삭제하기.

```bash
git config --unset user.name
```

전역으로 설정된 이름 삭제는 다음과 같음.

```bash
git config --unset --global user.name
```

> email의 설정 삭제도 `user.email`을 사용한다는 차이점만 존재함.
>
> `git config --unset --global user.email`

