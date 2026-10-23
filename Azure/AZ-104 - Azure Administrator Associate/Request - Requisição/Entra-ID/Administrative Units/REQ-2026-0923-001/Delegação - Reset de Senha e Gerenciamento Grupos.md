# Microsoft Entra ID — Administrative Units

## Objetivo

Implementação de **Administrative Units (AUs)** no Microsoft Entra ID para estabelecer um modelo de **administração delegada e segmentada**, permitindo que usuários específicos executem tarefas administrativas sobre as equipes de **Marketing (MKT)** e **Development (DEV)** sem necessidade de acesso administrativo amplo ao diretório.

A estrutura foi planejada considerando os princípios de **Least Privilege**, **segregação de responsabilidades** e **redução do escopo administrativo**, proporcionando maior controle sobre as operações realizadas pelos responsáveis de cada equipe.

---

## 1. Administrative Unit — Delegação para Reset de Senha

### Responsável: Junior Uacher

Foi criada uma **Administrative Unit dedicada ao gerenciamento de identidades das equipes DEV e MKT**, com foco na delegação controlada de operações relacionadas à recuperação de acesso.

### Implementação

* Criação da Administrative Unit destinada ao escopo das equipes **DEV** e **MKT**.
* Inclusão dos usuários pertencentes às equipes na Administrative Unit.
* Designação do usuário **Junior Uacher** como responsável pela execução das operações administrativas delegadas.
* Configuração da delegação necessária para permitir o **reset de senha dos usuários pertencentes ao escopo da Administrative Unit**.
* Restrição do escopo administrativo aos usuários previamente associados à unidade, evitando concessão de privilégios administrativos abrangentes no tenant.

### Validação

Foi realizado um teste operacional de **reset de senha** utilizando usuários pertencentes à Administrative Unit.

**Resultado:** operação executada com sucesso, confirmando o funcionamento da delegação administrativa e o correto isolamento do escopo de gerenciamento.

---

## 2. Administrative Unit — Gerenciamento de Associação a Grupos

### Responsável: Jose Silva

Foi criada uma segunda **Administrative Unit**, destinada à delegação controlada das operações de gerenciamento de grupos utilizados pelas equipes **DEV** e **MKT**.

### Implementação

* Criação da Administrative Unit destinada ao gerenciamento das equipes **DEV** e **MKT**.
* Inclusão dos grupos relacionados às equipes na estrutura de gerenciamento.
* Designação do usuário **Jose Silva** como responsável pelas operações administrativas delegadas.
* Configuração das permissões necessárias para gerenciamento das associações de usuários aos grupos dentro do escopo definido.
* Criação de um usuário convidado (**Guest**) para validação do processo de onboarding da equipe DEV:

  * `michaelkyle.b2c@hotmail.com`
* Inclusão do usuário convidado no fluxo de gerenciamento da equipe **DEV**.

### Validação

Foi realizado um teste de associação do usuário:

**Cloud TI Dev | Michael R. Kyle**

ao grupo:

**gp_ti_cloud_dev_hml**

**Resultado:** inclusão realizada com sucesso, validando o modelo de administração delegada e o controle de escopo aplicado à Administrative Unit.

---

## Arquitetura de Delegação

| Administrative Unit                | Escopo           | Responsável   | Operação                    |
| ---------------------------------- | ---------------- | ------------- | --------------------------- |
| AU — DEV & MKT Password Management | Usuários DEV/MKT | Junior Uacher | Reset de senha              |
| AU — DEV & MKT Group Management    | Grupos DEV/MKT   | Jose Silva    | Gerenciamento de associação |

## Resultado

A implementação das Administrative Units estabeleceu um modelo de **administração descentralizada e baseada em escopo**, permitindo delegar tarefas operacionais específicas sem conceder privilégios administrativos globais.

A solução proporciona:

* **Least Privilege:** redução dos privilégios concedidos aos operadores.
* **Delegated Administration:** distribuição controlada das responsabilidades administrativas.
* **Segregação de responsabilidades:** separação entre gerenciamento de credenciais e gerenciamento de grupos.
* **Escopo administrativo controlado:** operações limitadas aos objetos associados às respectivas Administrative Units.
* **Maior segurança operacional:** redução da exposição decorrente do uso de contas com privilégios elevados.
* **Governança:** estrutura mais organizada para administração das equipes DEV e MKT.
* **Validação operacional:** testes realizados com sucesso para comprovar o funcionamento das delegações implementadas.

### Tecnologias

* Microsoft Entra ID
* Administrative Units
* Role-Based Access Control (RBAC)
* Delegated Administration
* Least Privilege
* Identity & Access Management (IAM)
* Microsoft Entra ID Groups
* Guest Users
