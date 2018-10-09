Jenkins Pipeline with Docker Example
===

## Requirements

https://jenkins.io/doc/book/pipeline/docker/

## Jenkins

* add jenkins user to docker group
```
sudo usermod -a -G docker jenkins
```
* restart jenkins
```
sudo systemctl restart jenkins
```

## Docker
```
systemctl status docker
```

##

https://stackoverflow.com/questions/49214970/using-docker-image-of-maven-with-jenkins-could-not-create-local-repository