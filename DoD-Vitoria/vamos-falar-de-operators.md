# Vamos falar de Operadores?

Os operadores são extensões de software para Kubernetes que fazem uso de custom resources para gerenciar aplicações e seus componentes. Os operadores seguem os princípios da Kubernetes,como o control loop. (source: https://kubernetes.io/docs/concepts/extend-kubernetes/operator/)

Ao final dessa talk você vai aprender os conceitos para criar o seu próprio operator e deixar sua aplicação Statefulset no Autopilot.

# Como funciona Stateless Application com o control Loop?

Imagine que você criou um deployment com 5 réplicas, caso você deseje escale essas réplicas para 7, o processo responsável por checar se o estado deseja foi alcançandou não e que medidas devem ser tomas, chama-se control loop.

![k0s start][k0s-start]

# Como funciona Stateful Application sem Operators?

# Como funciona Stateful Application com Operators?

[k0s-start]:https://raw.githubusercontent.com/yuriolisa/devops-calls-content/main/k0s_start.png



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

- Estrutura do CRD.

- Estrutura do Controller.

- Abordagem do controller com o Kubernetes API Server.

- Exemplo MyApp ao Vivo.
