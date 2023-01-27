# Day 4

## Jenkins

### Resumo

**CI (Continuous Integration)** é um processo de desenvolvimento de software no qual as alterações frequentes no código-fonte são automaticamente compiladas e testadas. Isso permite que os erros sejam detectados e corrigidos rapidamente e garante que o código sempre esteja em um estado funcional.

**CD (Continuous Deployment)** é um processo de entrega de software automatizado que permite que as alterações no código-fonte sejam entregues ao usuário final sem interrupção. Isso inclui tarefas como a implantação automatizada em ambientes de produção, testes automatizados e monitoramento em tempo real.

**Jenkins** é uma ferramenta de automação de código aberto que permite a integração contínua e entrega contínua. Ele é escrito em Java e fornece vários plugins para automatizar tarefas relacionadas a CI / CD.

### Instalação

- Jenkins : https://www.jenkins.io/download/
- docker : `curl -fsSl https://get.docker.com | sh`
  - `usermod -aG docker jenkins`
  - `systemctl restart jenkins`
  - `systemctl status jenkins`
- kubectl: https://kubernetes.io/docs/tasks/tools/

**_Observação:_** o deploy está configurado na branch deploy.
