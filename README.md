<h1 align="center"> QUODE SRE BootCamp PROJETO FINAL - Squad3 </h1>

![Banner](https://user-images.githubusercontent.com/111643131/191636003-23204e01-bdc0-40ad-be32-206825b752ec.jpg)

## Definição dos Objetivos:

A criação de uma solução que que utiliza ferramentas e conceitos apresentados ao longo do Bootcamp, ou similares, para aumento da confiabilidade de uma aplicação, focando em processo de deployment, automação, escalabilidade e observabilidade.

* INFRAESTRUTURA e REDE;
* APLICAÇÃO e DEPLOYMENT - Representação Gráfica do fluxo da aplicação;
* OBSERVABILIDADE;
* MELHORES PRÁTICAS;
* CONFIABILIDADE.

## INFRAESTRUTURA e REDE
### Infraestrutura Kubernetes

A estrutura compõe-se de 3 hosts, sendo 1 MASTER e 2 WORKERS.
A implantação da estrutura é feita via Terraform, configurando automaticamente o host MASTER e efetuando JOIN dos dois hosts WORKERS.
Nesta estrutura será armazenado a aplicação Python.
![image](https://user-images.githubusercontent.com/111643131/191832991-9f42b1e3-4141-43d7-b3e3-e644494e2849.png)

A imagem docker da aplicação de PRODUÇÃO e DESENVOLVIMENTO foi armazenada no DockerHub

![image](https://user-images.githubusercontent.com/111643131/191832846-14479b87-e34f-4d14-b6f2-02e55571b137.png)


- ISTIO (sem aplicação)
- Kiali (precisa expor a porta 20001 no Kubernetes)
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
- Adminer (Adminstração PGSQL Produção - Porta 8181)
- Adminer (Adminstração PGSQL Desenvolvimento - Porta 8282)

![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Terraform](https://img.shields.io/badge/terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white)
![Shell Script](https://img.shields.io/badge/shell_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

![Jenkins](https://img.shields.io/badge/jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white)

## ARQUITETURA DA SOLUÇÃO

<img width="574" alt="arquitetura-solucao" src="https://user-images.githubusercontent.com/111643131/192026704-dd1186fd-1311-415f-b9fc-805d6405f330.png">

## APLICAÇÃO e DEPLOYMENT

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

- O build da imagem da aplicação é feita via CI/CD GitHub Action após um push no repositório "final-project-application".
- Acesso Aplicação Produção (ippublico-instancia-kubernetes:8500)
- Acesso Aplicação Desenvolvimento (ippublico-instancia-kubernetes:8501)

### Representação Gráfica do fluxo da aplicação:

![DrawApplicationQuode](https://user-images.githubusercontent.com/111643131/191882712-b75f3c1a-1ac1-4db2-9b1a-0ee8f338555d.png)

## OBSERVABILIDADE

- Prometheus
- Grafana

```
Golden Signals

- Latência;
- Erros;
- Tráfego;
- Saturação
```

## MELHORES PRÁTICAS
- Monitoramento em todos os ativos do ambiente;

Definição de alertas para monitorar as métricas da aplicação:
- disponibilidade da aplicação e banco de dados; 
- disponibilidade da aplicação e tempo de resposta; 
- quantidade de requests com status code diferente de 200;

```
Definição de agendamento de backup via "AWS Backup" usando Terraform;
```

## CONFIABILIDADE
Ações para aumento da disponibilidade medida da aplicação e ativos.

```
1. Implantação de um ciclo de desenvolvimento padronizado;
2. Tolerância a Falhas: uso de réplicas;
3. Teste de Engenharia do Caos;
4. Plano de Recuperação de Desastres;
5. Métricas: 
MTBF: tempo médio antes da falha;
MTTR: tempo médio para recuperação, para reparos, de resposta ou para a resolução;
MTTA: tempo médio para confirmação;
MTTF: tempo médio sem falhas;
```

## PLANO DE CONTINUIDADE
Quais serão os próximos passos para melhorar a infraestrutura da aplicação?

![FlowLife](https://user-images.githubusercontent.com/111643131/192025950-7eeb9807-0105-4ab0-aaa0-91ddbb34e193.JPG)

```
- Colocar o banco de dados na AWS RDS;
- Colocar a imagem da aplicação na Amazon ECR;
- Configuração de acesso via VPN.
```

## Autores
- Claudia Jugue [<p align="left"><img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></p>](https://www.linkedin.com/in/claudia-jugue/)  
- Fabiano Cesar Gaspar [<p align="left"><img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></p>](https://www.linkedin.com/in/fabiano-gaspar-12907924)
- Gabriel Mariusso [<p align="left"><img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></p>](https://www.linkedin.com/in/gabriel-mariusso/)
- Thiago Felipe de Andrade [<p align="left"><img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></p>](https://www.linkedin.com/in/thiago-felipe-de-andrade-932aab5/)
- Tânia Silva [<p align="left"><img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></p>](https://www.linkedin.com/in/taniass/)



