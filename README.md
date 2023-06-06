# Repositório dedicado aos estudos sobre Terraform

### Inicialmente privado afim de preservar informações.

### Esse repositório também será utilizado para aprender a documentar de maneira mais eficiente.

#### O que é Terraform?
    -> Terraform é uma ferramenta de IaC (Infrastructure as Code / Estrutura como Código) que te permite criar, alterar e versionar recursos de nuvem e on-prem de maneira segura e eficiente.

    -> O Terraform consegue gerenciar componentes de baixo nível como cálculos, armazenamento e recursos de rede, como também consegue gerenciar componentes de alto nível como DNS e SaaS.

    -> A workflow do Terraform é consistente e capaz de promover e gerenciar toda a infraestrutura durante o ciclo de vida da mesma.

#### Como o Terraform funciona?
    -> O Terraform cria e gerencia recursos em plataformas de nuvem (AWS, Azure, GCP, etc.) e outros serviços através de sua API. Os providers (provedores) habilitam o Terraform para trabalhar com virtualização em qualquer plataforma/serviço que acesse sua API.

    -> Existem muitos providers criados pela empresa responsável pelo Terraform, a HashiCorp, como também tem outros providers criados pela comunidade de usuários do Terraform. Todos esses providers estão registrados no Terraform Registry, incluindo também a AWS, Azure, GCP, GitHub, Kubernetes, etc.

#### O core da workflow do Terraform
    -> O core do Terraform consiste em 3 estágios:

    1. Escrita: Você define os recursos, que podem estar em 1 ou mais provedores de nuvem ou serviços.

    2. Planejamento: O Terraform cria um plano de execução onde ele descreve a infraestrutura que será criada, atualiza e também destrói a infraestrutura existente juntamente com sua configuração.

    3. Aplicação: Quando a infraestrutura for aprovada, o Terraform perfoma o propósito da operação de maneira correta, respeitando qualquer dependência dos recursos utilizados.

#### Por que usar o Terraform?
###### Gerenciamento de qualquer Infraestrutura
        -> Encontrar provedores para várias plataformas e serviços que você usa/usou no Terraform Registry. Assim como você pode escrever seu próprio provedor. O Terraform realiza uma abordagem imutável na infraestrutura, reduzindo a complexidade de atualização ou modificação de serviços e da própria estrutura.

###### Acompanhamento da Infraestrutura
        -> O Terraform gera um plano e alguns prompts para que o usuário aprove antes de modificar a infraestrutura. Também é possível acompanhar a infraestrutura através do comando 'Terraform state file', que é um recurso muito confiável para seu ambiente. O Terraform usa o 'state file' para determinar as mudanças que devem ser feitas na infraestrutura que combinam com sua configuração.

###### Alterações automatizadas
        -> A configuração de arquivos Terraform são declarativas, elas descrevem o estado final da sua infraestrutura. Não é necessário escrever instruções 'step-by-step', ou passo a passo, para criar recursos (resources) porque o Terraform já lida com a lógica. O Terraform cria um gráfico para determinar as dependências de recursos e criar/modificar recursos que não possuem dependências, de maneira paralela. Esse paralelismo é mais eficiente.

###### Configurações padronizadas
        -> O Terraform suporta a reutilização de componentes já configurados, chamados de módulos, para definir coleções de configurações de infraestruturas, economizando tempo e promovendo as boas práticas. É possível também utilizar de módulos públicos do Terraform Registry ou ainda escrever o seu próprio.

###### Colaboração
        -> Assim que a configuração estiver pronta, o usuário pode realizar um commit usando um controle de versionamento, como Git ou Mercurial, e usar o Terraform Cloud para gerenciar as workflows de maneira eficiente entre os times. O Terraform Cloud performa de maneira consistente e confia´vel e promove um acesso seguro para compartilhar estado e dados sigilosos, além de controle de acesso baseado em cargos e um registro privado para compartilhamento tanto de módulos como de provedores.

        