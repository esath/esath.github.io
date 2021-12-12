#### Installing Ubuntu and Docker on AWS is out of scope here, maybe later..

```
$ docker run --restart unless-stopped --name jenkins -p 80:8080 -p 50000:50000 -v /home/ubuntu/jenkins_home:/var/jenkins_home jenkins/jenkins

Get admin-pwd from installed container:
$ docker exec -it jenkins bash

jenkins@67a2abc12337:/$ more /var/jenkins_home/secrets/initialAdminPassword
a3e3fefefef64546858001111efefefe4b6c91

Login to container as root if needed:
$ docker exec -it -u root jenkins2 bash
```
