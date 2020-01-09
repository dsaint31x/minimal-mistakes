---
title:  "[linux] 파일명 검색 및 파일 내부 문자열 검색.- fnid and grep"
last_modified_at:   2020-01-08
author: dsaint31
categories: 
  - linux
use_math: false
tags: 
  - linux 
---

# 파일명으로 해당 파일 위치 검색.

```bash
find [target_dir] -name [file_name]
```

* 정규표현식 사용가능함.

```bash
find ./ -name 'linux*'
```

# 특정 문자열을 가진 파일 위치 검색.

```bash
grep -r [target_str] [target_file or target_dir]
```

* 특정 디렉토리 밑의 모든 파일 검색시 `*` 사용.
* `-r` 옵션으로 타겟 디렉토리 밑의 서브 디렉토리까지 뒤짐.

```bash
grep -r 'dft' ./*
```

> `--include` 옵션 사용시, 특정 확장자로 제한 가능함.

