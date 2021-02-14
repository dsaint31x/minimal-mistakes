---
title:  “[linux] vim 에서 help사용하기”
last_modified_at:   2021-02-13
author: dsaint31
categories: 
  - linux
  - vim
use_math: false
tags: 
  - linux
  - vim 
---
[
# vim 에서 help사용하기.

```bash
:help [topic]
```
* 위의 명령어에서 `[topic]`부분에 궁금한 명령어, 또는 기능을 지정.

# `help`에사용되는 접두어.

|mode | prefix | example | desc. |
| --- | --- | --- | --- |
| normal mode | None | :help w | 오른쪽으로 단어로 이동. |
| input mode | i_ | :help i_CTRL-N | |
| command mode | : | :help :w | 저장하기. |
| special key on command mode | c_ | :help c_CTRL-B | \
| visual mode | v_ | :help v_u | |
| excutoin option | - | :help -r | |
| option | ' | :help 'tabstop' | |

 
# multi-key input이 필요한 명령어의 help를 보기 위한 입력.

`:help CTRL-W_n` 은 `CTRL`과 `W`를 동시에 누르고 `n`을 누른 경우의 도움말을 보여줌.
