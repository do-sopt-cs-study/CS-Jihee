# HTTP & HTTPS

: 웹 통신의 기초와 보안 버전의 차이

## HTTP란?

HTTP : (Hyper Text Transfer Protocol) 서버/클라이언트 모델을 따라 데이터를 주고 받기 위한 프로토콜

- HTTP는 인터넷에서 하이퍼텍스트를 교환하기 위한 통신 규약

### HTTPS의 구조

어플리케이션 레벨의 프로토콜로 TCP/IP 위에서 작동

- HTTP는 상태를 가지고 있지 않는 Stateless 프로토콜
- Method, Path, Version, Headers, Body 등으로 구성
![Untitled](https://github.com/do-sopt-cs-study/CS-Jihee/assets/68178395/605440e2-eaef-41df-9ec3-e2668d1abbf2)


## HTTPS

### HTTPS?

HyperText Transfer Protocol over Secure Socket Layer, HTTP over TLS, HTTP over SSL, HTTP Secure 등으로 불리는 HTTPS는 HTTP에 데이터 암호화가 추가된 프로토콜

- HTTPS는 HTTP와 다르게 443번 포트를 사용하며, 네트워크 상에서 중간에 제3자가 정보를 볼 수 없도록 암호화를 지원

### HTTPS의 등장

HTTP는 암호화 되지 않은 평문 데이터를 전송하는 프로토콜 → 보안에 취약함, 제 3자에게 개인정보 노출 위험

⇒ HTTPS 등장

## HTTPS

### HTTPS?

HyperText Transfer Protocol over Secure Socket Layer, HTTP over TLS, HTTP over SSL, HTTP Secure 등으로 불리는 HTTPS는 HTTP에 데이터 암호화가 추가된 프로토콜

- HTTPS는 HTTP와 다르게 443번 포트를 사용하며, 네트워크 상에서 중간에 제3자가 정보를 볼 수 없도록 암호화를 지원

### HTTPS의 등장

HTTP는 암호화 되지 않은 평문 데이터를 전송하는 프로토콜 → 보안에 취약함, 제 3자에게 개인정보 노출 위험

⇒ HTTPS 등장
