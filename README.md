# HelloWorldMaven
$ docker pull jenkins/jenkins
$ docker volume create --name jenkins-volume
$ echo "Volume check" >> /var/lib/docker/volumes/jenkins-volume/test.txt	
$ docker run -p 11000:8080 -p 50000:50000 -v jenkins-volume:/jenkins-volume jenkins/jenkins:latest
$ docker exec -it -u root e7a88722f8bb /bin/bash
$ cd /jenkins-volume/
$ ls | grep test
$ apt-get update -y && apt install maven -y
$ mvn -version
