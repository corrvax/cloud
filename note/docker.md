##Docker

### Docker 설치방법
1. 도커를 설치한다.   
`sudo yum install docker`   
<img width="1299" alt="스크린샷 2024-06-27 오후 9 24 53" src="https://github.com/corrvax/cloud/assets/54795404/8cb67b7f-c278-4996-a200-246f1bef6b7f">

2. 도커를 실행시킨다.   
`sodo systemctl start docker`   
`docker run -d -p 80:80 docker/getting-started`   
1024번 이하 포트들은 wellknown포트로 이 포트들을 열땐 관리자 권한이 필요함으로 sudo로 명령어를 실행한다.
`sudo docker run -d -p 80:80 docker/getting-started`   
<img width="2038" alt="스크린샷 2024-06-27 오후 9 31 52" src="https://github.com/corrvax/cloud/assets/54795404/f3a6fa07-6bfd-4fa1-87ba-e193926f95cc">

3. VM인스턴스의 외부 IP로 접속하면 VM에 설치한 도커에 접속이되고있음을 확인할 수 있다.   
<img width="2208" alt="스크린샷 2024-06-27 오후 9 35 50" src="https://github.com/corrvax/cloud/assets/54795404/aec0196b-064a-4d86-b133-0134d00029ac">
--> 상단에 접속 url을 확인하면 외부IP로 접속했음을 확인할 수 있다.
<img width="2203" alt="스크린샷 2024-06-27 오후 9 36 45" src="https://github.com/corrvax/cloud/assets/54795404/6a819d95-bab5-425a-995d-1ef2dcbef0e3">
