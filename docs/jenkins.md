#### Installing Ubuntu and Docker on AWS is out of scope here, maybe later..

```
$ docker run --restart unless-stopped --name jenkins -p 80:8080 -p 50000:50000 -v /home/ubuntu/jenkins_home:/var/jenkins_home jenkins/jenkins

Get admin-pwd from installed container:
$ docker exec -it jenkins bash

jenkins@67a2abc12337:/$ more /var/jenkins_home/secrets/initialAdminPassword
a3e3fefefef64546858001111efefefe4b6c91

Login to container as root if needed:
$ docker exec -it -u root jenkins bash
```

#### Upgrade Jenkins in Docker:
```
$ sudo docker exec -u 0 -it jenkin bash

root@12a2abd12345:/# cd /usr/share/jenkins
root@12a2abd12345:/# service jenkins stop
root@12a2abd12345:/# mv jenkins.war jenkins_backup.war
root@12a2abd12345:/# wget https://updates.jenkins.io/download/war/2.324/jenkins.war
root@12a2abd12345:/# service jenkins start

DONE!
Note: Use latest download-link for jenkins.war.
You can get link from Jenkins-GUI > New version notification.

```
