# Vamos falar de Operadores?

Os operadores são extensões de software para Kubernetes que fazem uso de custom resources para gerenciar aplicações e seus componentes. Os operadores seguem os princípios da Kubernetes,como o control loop. (source: https://kubernetes.io/docs/concepts/extend-kubernetes/operator/)

Ao final dessa talk você vai aprender os conceitos para criar o seu próprio operator e deixar sua aplicação Statefulset no Autopilot.

# Como funciona Stateless Application com o control Loop?

Imagine que você criou um deployment com 5 réplicas, caso você deseje escale essas réplicas para 7, o processo responsável por checar se o estado deseja foi alcançandou não e que medidas devem ser tomas, chama-se control loop.

![control loop](controlloop.png?raw=true "Control Loop")

# Como funciona Stateful Application sem Operators?

Podemos citar como exemplo algum banco de dados, como: MySQL ou Postgres que esteja sendo executado em um cluster Kubernetes. O pessoal de Ops ou DevOps, muito provavelmente irão se preocupar em operações como: Criação de Novos Clusters/DB, Backup, Restore, Escalabilidade, Persistência de Dados. Como são aplicações Stateful você deve persistir dados e atentar-se para que esses dados estejam disponíveis em todos os pods. Todo esse trabalho deveria ser feito manual ou iriam ser criados scripts para automatizar todas essas tasks. É aqui que entra o próximo tópico onde vemos a importância do Operator para aplicações Stateful.

# Como funciona Stateful Application com Operators?

Uma aplicação Statefulset baseada em um operator possui a mesma lógica do control loop customizada, assim como o CRD (Custom Resource Definition), o que vai entregar toda a lógica ao controller de como executar aquela tarefa.
  `````
  Por padrão temos Kind: Deployment, com o operator poderemos criar por exemplo: 
  
  Kind: MyApp.
  `````

# Como posso desenvolver um novo Operator?

Vou deixar aqui dois frameworks que vocês poderão utilizar para começar a dar os primeiros passos: 

- Operator-SDK.
- Kubebuilder.

# Operator SDK. 

![operator sdk](operator_logo_sdk_color.svg?raw=true "Operator SDK")


- O que são Operadores?
  - Definição.
  - Casos de Uso.

- Stateless Application.
  - Definição com imagem.

- Stateful Application sem Operator.
  - Definição com imagem e mostrando as dores.

- Stateful Application com Operator.
  - Definição com imagem e mostrando as soluções.

- Os 5 níveis de automação dos Operators.

- Bases de um operator: Helm, Ansible, Go.

- Operator SDK.

- OLM - Operator Lifecycle Manager

- Estrutura do CRD.

- Estrutura do Controller.

- Abordagem do controller com o Kubernetes API Server.

- Exemplo MyApp ao Vivo.
