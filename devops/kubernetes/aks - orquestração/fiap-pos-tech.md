# AULA 1: Introdução ao Kubernetes

# AULA 2: Implantação do Azure AKS

Quais problemas o AKS resolve?
- Escalabilidade
- Gerenciamento de containers
- Foco do time de desenvolvimento: Times não olham para infraestrutura.

O que é AKS?
- É um serviço de 

Quais os benefícios chaves do AKS?

Quais os componentes do AKS? Pelo que o AKS é composto?
- Control Panel: Gerencia os cluster.
- Clusters
- Noz: Máquinas virtuais, onde os containers sao executados.
- Pods: 

Resumo:

- Instalação Azure CLI
- Criação de um grupo de recurso no Azure sem padrão.
- Criação básica de um AKS sem padrão.

Implantação do Azure AKS

Azure CLI

- Ferramenta instalada na máquina para começar a implementação do AKS no azure.
- az --version -> comando para verificar se a instalação foi realiaza corretamente
- az login

Criação do Cluster no AKS

- Existem duas opções para criar recursos dentro do Azure, via portal ou via prompts do azure cli.

Permissão ao criar o serviço AKS

Azure

- Azure CLI
- Grupo de recurso: O que é um Grupo de Recurso?
  É uma organização lógica que o Azure fornece para facilitar o gerenciamento, monitoramento, pagamento e controle de acesso dos seus recursos.

# Aula 3: Trabalhando com AKS parte prática

Resumo:

- Conectar com Cloud Shell via bash.
- Upload do arquivo .ymal.
- Executar Apply do arquivgo .ymal dentro do Cloud Shell.
- Testou requisição para o serviço/endpoint público.
- Aumento de replicas para os pods.

Após criação do cluster, o próximo passo é se conectar no cluster.

Para se conectar no cluste, faça o seguinte:

- Suba o arquivo deployment.ymal via Upload Files
- Execute o comando kubeclt apply -f deployment.ymal
- Execute o comando kubectl get services para verificar se o servico foi criado corretamente.
- Execute o comando kubectl get pods para verificar os Pods que estao up

Cloud Shell

- Ferramenta utilizada para acessar a linha de comando do Azure pelo navegador.
- Ferramenta utilizada para se conectar ao cluster AKS.
- Acessar o promp e executar comandos.

Observação:

- Alteração arquivos .YMAL: Sempre que alterar o arquivo .ymal, é necessário dar o apply
- Distribuição de Carga: O próprio Kubernetes sabe distribuir as requisições para nao deixar alguma replica sendo mais utilizada do que outra.

Parte 2

Reverter um deployment

- Execute o comando kubectl deployments para obter todos os deployments realizados no cluster
- Execute o comando kubectl delete deployments <SERVICE-NAME>
- Execute o comando kubectl delete services <SERVICE-NAME>

Dúvidas da aula:

- Como escolher o modo de autenticação ao criar um cluster AKS?
- Eu nao entendi o porque de matar os pods e o servico continuar de pé.
- Ao remover os deployments e os services, ainda sim será cobrado algo na assinatura?
- Como dar acesso a mais pessoais a um cluster?

# Aula 4: CI/CD com AKS

Parte 1: Entendendo CI/CD e suas vantagens

Entendendo Continuous Integration(CI)

- Repositório no github compartilhado pelo time que sofre constantes alterações.

Observações da Aula:

- Antes do CI, era necessário o build ser gerado na máquina do desenvolvedor e abrir uma comunicacao SSH com o servidor para enviar o pacote.

Entendendo o Continouous Deployments

Parte 2: Por que foi escolhido Github Actions?

Resumo:

- Explicação dos recursos do Github Actions
- Vantagens de utilizar Github Actions

Workflows:

Triggers:

- Assim que acontecer isso no meu repositório, faça isso.

Segurança
Gratuito
Integração com Docker

Parte 3

- Criação do arquivo kube-config com as credenciais do AKS.
- Execute o comando az aks get-credentials --resource-group <NAME_RESOURCE_GROUP> --name <NAME_CLUSTER_AKS> --file kubeconfig.ymal
- Explicação da necessidade de criar Secrets
- Criação de Secrets no github
- Criação do arquivo .YMAL de CI/CD

Criar arquivo de configuração do GitHub Actions
Criar arquivo com as configurações com as credenciais do AKS

Resumo

- Criação de Secrets no Github

Dúvida da aula

- Como segregar secrets por ambiente DEV, HOMOLOG e PRD?

Dúvida:

Github da aula:
JoaoAntonioMarques/FiapAKS
