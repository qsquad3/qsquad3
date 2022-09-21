<h1 align="center"> SRE BootCamp PROJETO FINAL </h1>

![Imagem3](https://user-images.githubusercontent.com/111643131/191147873-c99b81ca-22a0-48ea-8bd1-c586ff2152d6.jpg)

## Definição dos Objetivos:

A criação de uma soluçao que que utiliza ferramentas e conceitos apresentados ao longo do bootcamp, ou similares, para aumento da confiabilidade de uma aplicação, focando em processo de deployment, automação, escalabilidade e observabilidade.

* INFRAESTRUTURA e REDE;
* APLICAÇÃO e DEPLOYMENT - Representação Gráfica do fluxo da aplicação;
* OBSERVABILIDADE;
* MELHORES PRÁTICAS;
* CONFIABILIDADE;

## INFRAESTRUTURA e REDE
## Infraestrutura Kubernetes

A estrutura compõe-se de 3 hosts, sendo 1 MASTER e 2 WORKERS.
A implantação da estrutura é feita via Terraform, configurando automaticamente o host MASTER e efetuando JOIN dos dois hosts WORKERS.
Nesta estrutura será armazenado a aplicação Python.

- ISTIO
- Kiali (precisa expor a porta 20001 no kubernetes)
- DataDog (Cloud Version)

![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white)
![Shell Script](https://img.shields.io/badge/shell_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)

## Infraestrutura Docker

A estrutura compõe-se de 1 host, sendo Docker Server.
Nesta estrutura estamos subindo as ferramentas de modo automatizado, sendo elas:
- Jenkins (ippublico-instancia-docker:8084)
- Grafana/Prometheus/Loki/Tempo (ippublico-instancia-docker:3000)
- Adminer (Adminstração PGSQL - Porta 8181)

![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Terraform](https://img.shields.io/badge/terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white)
![Shell Script](https://img.shields.io/badge/shell_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white)


## APLICAÇÃO e DEPLOYMENT

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

- O build da imagem da aplicação é feita via CICD GitHub Action após um push no repositório "final-project-application"
- Acesso aplicação (ippublico-instancia-kubernetes:8500)


## OBSERVABILIDADE

XXXXXXXXXXXXXXXXXXXXXXXXXXX

```
XXX
XXX
XXX
```

## MELHORES PRÁTICAS

XXXXXXXXXXXXXXXXXXXXXXXXXXX

```
XXX
XXX
XXX
```

## CONFIABILIDADE

XXXXXXXXXXXXXXXXXXXXXXXXXXX

```
XXX
XXX
XXX
```

### Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

### Autores
![Small](https://user-images.githubusercontent.com/111643131/191145275-c558c687-5e40-4033-9125-f919bce3ae2f.jpg)
- Claudia Jugue [<p align="left"><img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></p>](https://www.linkedin.com/in/claudia-jugue/)  - Fabiano Cesar Gaspar [<p align="left"><img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></p>](https://www.linkedin.com/in/thiago-felipe-de-andrade-932aab5/)
- Gabriel Mariusso [<p align="left"><img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></p>](https://www.linkedin.com/in/gabriel-mariusso/)
- Thiago Felipe de Andrade [<p align="left"><img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></p>](https://www.linkedin.com/in/thiago-felipe-de-andrade-932aab5/)
- Tânia Silva [<p align="left"><img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></p>](https://www.linkedin.com/in/taniass/)

## Contributors

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

