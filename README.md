<h1 align="center"> QUODE SRE BootCamp PROJETO FINAL - Squad3 </h1>

![Banner](https://user-images.githubusercontent.com/111643131/191636003-23204e01-bdc0-40ad-be32-206825b752ec.jpg)

## Definição dos Objetivos:

A criação de uma soluçao que que utiliza ferramentas e conceitos apresentados ao longo do bootcamp, ou similares, para aumento da confiabilidade de uma aplicação, focando em processo de deployment, automação, escalabilidade e observabilidade.

* INFRAESTRUTURA e REDE;
* APLICAÇÃO e DEPLOYMENT - Representação Gráfica do fluxo da aplicação;
* OBSERVABILIDADE;
* MELHORES PRÁTICAS;
* CONFIABILIDADE;

## INFRAESTRUTURA e REDE
### Infraestrutura Kubernetes

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

### Infraestrutura Docker

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

### Representação Gráfica do fluxo da aplicação:
```
XXX PENDENTE ADD IMAGEM
```

## OBSERVABILIDADE

- Prometheus: http://54.243.22.130:9090/targets
- Grafana: http://35.153.185.39:3000/

```
Golden Signals
- Latencia;
- Erros;
- Trafico;
- Saturação;
```

## MELHORES PRÁTICAS
- Definir e implementar uma estratégia de backup e restore;
- Monitoramento em todos os ativos do ambiente;

Definir alertas para monitorar as métricas da aplicação:
- como disponibilidade da aplicação e banco de dados; 
- disponibilidade da aplicação e tempo de resposta; 
- quantidade de requests com stauts code diferente de 200;

```
XXX
```

## CONFIABILIDADE
Ações para aumento da disponibilidade medida da aplicação e ativos.

```
1. Tolerancia a Falhas: uso de réplicas;
2. 
3. 
4.
5.
```

## PLANO DE CONTINUIDADE
Quais seriam os próximos passos para melhorar a infraestrutura da aplicação?

XXXXXXXXXXXXXXXXXXXXXXXXXXX

```
XXX
XXX
XXX
```

## Versioning
We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Autores
- Claudia Jugue [<p align="left"><img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></p>](https://www.linkedin.com/in/claudia-jugue/)  
- Fabiano Cesar Gaspar [<p align="left"><img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></p>](https://www.linkedin.com/in/thiago-felipe-de-andrade-932aab5/)
- Gabriel Mariusso [<p align="left"><img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></p>](https://www.linkedin.com/in/gabriel-mariusso/)
- Thiago Felipe de Andrade [<p align="left"><img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></p>](https://www.linkedin.com/in/thiago-felipe-de-andrade-932aab5/)
- Tânia Silva [<p align="left"><img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></p>](https://www.linkedin.com/in/taniass/)



