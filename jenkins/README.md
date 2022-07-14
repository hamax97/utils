# Description

Local Jenkins that can launch Docker (in Docker.)

Build:

```bash
docker build -t local-jenkins:latest .
```

Run:

```bash
docker run -d --name jenkins \
    -v /var/run/docker.sock:/var/run/docker.sock -v jenkins_home:/var/jenkins_home \
    -p 8080:8080 -p 50000:50000 \
    local-jenkins
```

Update:

```bash
docker push hamax97/local-jenkins:latest
```

# Docs

- [Docker Jenkins](https://github.com/jenkinsci/docker/blob/master/README.md).