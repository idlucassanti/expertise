# DIA 1

Aplicação - PaaS - AppService
Dados - SQL Server - Azure SQL DB
Identidade e Seguraça - Key Vault, Managed Identity, ACR(imagem pronta)

# DIA 2: CLOUD NATIVE + DEVOPS + AI

Kubernetes / AKS
-> A imagem que colocamos no ACR finalmente ganha vida

# Terraform

-> Ferramenta utilizada para criar um processo de automatizar toda a nossa infraestrutura.

- Pertence a IBM
- Possui integração com Azure

Componentes do Terraform

Workflow do Terraform

Arquivos no Terraform

- Extensão .tf
- Arquivos sao conhecidos como Terraform Manifests

Sintaxe do Terraform


Dúvidas na parte de criação da máquina do AKS
- Professor, no contexto de escalabilidade, se meu cluster nao estiver aguentando, para escalar, basta o tipo da máquina? Como eu consigo calcular uma máquina para atender minha aplicação? Ex: quantidade de containers? quantidade de requisicao que bate em cada container? Como eu consigo metrificar isso para escolher o tipo da minha máquina do AKS?