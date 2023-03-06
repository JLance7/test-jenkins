# To run docker in docker in jenkins 

## Get image
```
docker build -t <name> .
```
or
```
docker pull squabglob/jenkins-docker
```

---

## Run as container
```
docker run --name my-jenkins -d -p 8080:8080 -p 50000:50000 `
  -v jenkins_home:/var/jenkins_home --group-add 0 -v /var/run/docker.sock:/var/run/docker.sock `
  <image name>
```

## Add permission to docker.sock to jenkins user
```
cd /var/run
chown :jenkins docker.sock
chmod g+rwx docker.sock
```