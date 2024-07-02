## CPU를 극단적으로 사용하는 애플리케이션 생성하기

### 프로그램과 프로세스의 차이
나의 초기 답변 : 프로세스란 프로그램이 실행되는 단위를 뜻하고, 프로그램은 CPU위에서 동작하는 하나의 작업을 뜻합니다.
- 프로그램 : 
  하드디스크에 저장되어있는 application을 뜻한다.
- 프로세스 : 
  하드디스크에 저장되어있는 애플리케이션을 실행하면 메모리에 올라가는데 이를 프로세스라고한다.
  이때 여러개의 프로세스가 메모리에 올라가있는데, 스케줄링에의해 선택된 프로세스가 CPU위에서 실행된다.
   
  CPU와 하드디스크의 속도차를 극복하고자 메모리에 올려서 사용한다.
  또, 메모리와 CPU사이에 캐시메모리를 두고 속도차를 극복한다.

### CPU Bound Application
- Hash연산을 많이 쓰는 애플리케이션   

1. CPU Bound Application 생성하기   
<img width="1309" alt="스크린샷 2024-07-02 오후 8 38 11" src="https://github.com/corrvax/cloud/assets/54795404/93027cb4-d028-4bb2-8380-ca029d903fae">
    getMD5Digest 메소드에서 Hash연산을 100000번 반복한다.   
  - 서버의 Port를 80으로 맞춘다.   
<img width="1124" alt="스크린샷 2024-07-02 오후 8 41 31" src="https://github.com/corrvax/cloud/assets/54795404/02e7a3d5-7708-450d-b456-4b672bbbb7cd">   
  - 현재 실행중인 포트 중단하기   
`netstat - lntp |grep [포트번호]`   
`Isof -i :포트번호`   
  <img width="807" alt="스크린샷 2024-07-02 오후 8 58 48" src="https://github.com/corrvax/cloud/assets/54795404/8855b0ed-e3b0-4586-961d-0de4a8f90484">
  - localhost/hash/123으로 접속 시 hash연산이 된 것을 확인할 수 있다.
<img width="575" alt="스크린샷 2024-07-02 오후 9 01 09" src="https://github.com/corrvax/cloud/assets/54795404/2dbf75b7-9c7c-41ea-89b9-011f899c1838">
  - deploy하여 jar파일로 추출한다.
<img width="1552" alt="스크린샷 2024-07-02 오후 9 26 15" src="https://github.com/corrvax/cloud/assets/54795404/1c26364e-c4f1-4a6a-8e1a-9e6265f1d103">

