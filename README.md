# Dockerize sshd [![lint](https://github.com/infraworks/docker-sshd/actions/workflows/lint.yml/badge.svg)](https://github.com/infraworks/docker-sshd/actions/workflows/lint.yml)

Container with sshd service

Add your pub key in authorized_keys file
```bash
cat ~/.ssh/id_ed25519 > authorized_keys
```

Build the image
```bash
docker build . --tag sshd
```

Launch the container in background
```bash
docker run -d -p 2222:22 --name sshd sshd
```

Connect in ssh to the container

```bash
ssh -i ~/.ssh/id_rsa guest@xxx.xxx.xxx.xxx -p 2222
```
