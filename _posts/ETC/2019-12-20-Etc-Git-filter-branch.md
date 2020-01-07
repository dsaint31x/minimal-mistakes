---
title:  "[Etc] Git에서 파일 완전삭제"
date:   2019-12-18 20:33:59
author: dsaint31
categories: Etc
use_math: false
tags: Rufus
---

# 파일의 모든 commit에서 영구적 삭제  
@(Computer)


## 언제
* 모든 커밋의 이메일 주소를 변경하거나 
* 어떤 파일(패스워드가 들어간 파일이나 쓸데없이 용량만 큰 파일들)을 삭제해야 하는 경우...

## `filter-branch` 
* history 전체에서 필요한 것들만 골라내는 도구.

### `--tree-filter` 옵션

`--tree-filter` option으로 모든 commit에서 특정 파일이나 디렉토리를 제거 가능함.

```bash
git filter-branch --tree-filter 'rm -rf test/trash/img` HEAD
```

* 위의 명령어는 git repository에서 test/trash/img 폴더를 모든 commit에서 제거함.


### `--prune-empty` 옵션

이후, 해당 디렉토리 및 파일들과 관련된 내용만으로 존재하던 비어있는 commit들도 제거해야 하기 때문에 `--prune-empty` 옵션을 사용해야 함.

```bash
git filter-branch --prune-empty -f HEAD
```

### 최종으로 push.

이후, 원격지에 push를 해주면 끝남.

```bash
git push origin master -f
```

## 기타

### 백업 제거하는 방법

`filter-branch`등을 사용할 때, 다음과 같은 에러가 나올때가 있음.

```bash
Cannot create a new backup.
A previous backup already exists in refs/original/
Force overwriting the backup with -f
```

이 경우, 다음의 명령어로 백업을 제거해야 함.

```bash
git update-ref -d refs/original/refs/heads/master
```

## References

* [Developer-Designer](http://developer-designer.blogspot.com/2019/09/master-push.html)
* [stack overflow](https://stackoverflow.com/questions/5324799/git-remove-commits-with-empty-changeset-using-filter-branch)
* [pro git](https://github.com/progit/progit/blob/master/ko/06-git-tools/01-chapter6.markdown)
