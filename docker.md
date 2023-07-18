

[docker 관련 내용]


* 도커에서 젠킨스 설치

- 이름은 jenkins2023
- 외부포트는 18080, 내부 포트는 8080

docker run -d --name jenkins2023 --restart=on-failure -p 18080:8080 -v /var/jenkins_home:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock -e TZ=Asia/Seoul -u root jenkins/jenkins

* 도커접속
docker exec -it jenkins2023 /bin/bash


