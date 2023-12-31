## TLS/SSL

### ****SSL****

*암호화 기반 인터넷 보안 프로토콜*

원래 웹에서의 데이터는 가로채면 누구나 읽을 수 있는 일반 텍스트 형태로 전송 되었다. 이러한 문제때문에 인터넷 통신의 개인정보 보호, 인증, 데이터 무결성을 보장하기 위해 Netscape가 1995년 처음으로 SSL을 개발하였다.

- 전달되는 모든 데이터를 암호화하고 특정한 유형의 사이버 공격도 차단
- TLS(Transport Layer Security) 암호화의 전신

### ****TLS****

SSL의 업데이트 버전으로 SSL의 최종버전인 3.0과 TLS의 최초버전의 차이는 크지않으며, 이름이 바뀐것은 SSL을 개발한 Netscape가 업데이트에 참여하지 않게 되어 소유권 변경을 위해서 변경

- TLS는 SSL의 업데이트 버전이며 명칭만 다르다

## SSL/TLS의 작동 방식

SSL은 개인정보 보호를 제공하기 위해, 웹에서 전송되는 **데이터를 암호화**

→ 데이터를 가로채려해도 거의 **복호화가 불가능**

- SSL은 클라이언트와 서버간에 **핸드셰이크를 통해 인증**이 이루어진다. 또한 **데이터 무결성**을 위해 데이터에 디지털 서명을 하여 데이터가 의도적으로 도착하기 전에 조작된 여부를 확인한다.

## ****SSL/TLS 핸드셰이크****

handShake는 클라이언트와 서버간의 메세지 교환

- HTTPS 웹에 처음 커넥션할 때 진행
- 핸드셰이크의 단계는 클라이언트와 서버에서 지원하는 암호화 알고리즘, 키 교환 알고리즘에 따라 달라짐

### **RSA 키 교환 알고리즘**

1. 클라이언트 -> 서버 메세지 전송 - 이때 핸드셰이크가 시작된다. 이 메세지에는 TLS 버전, 암호화 알고리즘, 무작위 바이트 문자열이 포함된다.
2. 서버 -> 클라이언트 메세지 전송 - 클라이언트의 메세지에 응답으로 서버의 SSL인증서, 선택한 암호화 알고리즘, 서버에서 생성한 무작위 바이트 문자열을 포함한 메세지를 전송한다.
3. 인증 - 클라이언트가 서버의 SSL인증서를 인증 발행 기관에 검증한다.
4. 예비 마스터 암호 - 클라이언트는 무작위 바이트 문자열을 공개 키로 암호화된 premater secret 키를 서버로 전송한다.
5. 개인 키 사용 - 서버가 premaster secret 키를 개인 키를 통해 복호화한다. (개인 키로만 복호화 가능)
6. 세션 키 생성 - 클라이언트와 서버는 클라이언트가 생성한 무작위 키, 서버가 생성한 무작위 키, premaster secret 키를 통해 세션 키를 생성한다. 양쪽은 같은 키가 생성되어야 한다.
7. 클라이언트 완료 전송 - 클라이언트는 세션 키로 암호화된 완료 메세지를 전송한다.
8. 서버 완료 전송 - 서버도 세션 키로 암호화된 완료 메세지를 전송한다.
9. 핸드셰이크 완료 - 핸드셰이크가 완료되고, 세션 키를 이용해 통신을 진행한다.
