---
title:  "[linux] curl"
last_modified_at:   2020-12-25
author: dsaint31
categories: 
  - linux
use_math: false
tags: 
  - linux 
---

* command line interface tool로 Http 요청을 보내고 응답을 받는 클라이언트.
* restful api 테스트용으로 사용가능함.
* 단, highlight 기능등이 없어서... 급하게 사용할 때에만 사용하는게 나음.

python이 설치된 경우에는 ***HTTPie*** 를 사용하는 게 나음.

# GET 메소드로 보내기.
```bash
curl -X GET <URL>
```
* 이 경우, HTTP 응답헤더가 보이지 않음.

# 보다 자세한 응답 보기
```bash
curl -Xi GET <URL>
```
* GET 요청에 대해 HTTP 응답헤더를 같이 보여줌.

# `-h` extra header 설정하기

```bash
curl -iX PUT -H ‘Content-Type: application/json’ -d ‘{“key”:”value”}’ <URL>
```
* `-d` post 데이터 설정.
	(HTTP)  Sends  the  specified  data  in  a POST request to the HTTP server, in the same way that a browser does when a user has  filled in an HTML form and presses the submit button. This will cause curl to pass the data to the  server  using  the  content-type  applica‐tion/x-www-form-urlencoded.
	



