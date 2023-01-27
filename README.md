# jornadaDevOpsElite

## Deploy

### Conecção SSH

```bash
    ssh -i <ssh-file> root@ip
```

### Jenkins

```bash
# Deploy em Comandos
    curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee \
    /usr/share/keyrings/jenkins-keyring.asc > /dev/null
```

```bash
    echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
    https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
    /etc/apt/sources.list.d/jenkins.list > /dev/null
```

```bash
    sudo apt-get update
    sudo apt-get install fontconfig openjdk-11-jre
    sudo apt-get install jenkins
```

### Docker

```bash
    url -fsSl https://get.docker.com | sh
```

```bash
    usermod -aG docker jenkins
    systemctl restart jenkins
    systemctl status jenkins
```

### Kubectl

```bash
    sudo apt-get update
    sudo apt-get install -y ca-certificates curl
```

```bash
    sudo curl -fsSLo /etc/apt/keyrings/kubernetes-archive-keyring.gpg https://packages.cloud.google.com/apt/doc/apt-key.gpg
```

```bash
    echo "deb [signed-by=/etc/apt/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list
```

```bash
    sudo apt-get update
    sudo apt-get install -y kubectl
```
