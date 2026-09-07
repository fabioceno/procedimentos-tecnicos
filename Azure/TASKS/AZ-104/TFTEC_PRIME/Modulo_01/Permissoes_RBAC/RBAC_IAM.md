# Azure RBAC / IAM — Controle de Acesso por Resource Group

## Objetivo

Implementação de **controle de acesso baseado em funções (RBAC)** no Microsoft Azure, utilizando o **IAM (Identity and Access Management)** para definir permissões específicas para grupos de usuários em diferentes **Resource Groups**.

O objetivo foi aplicar o princípio de **controle de acesso por função**, garantindo que cada equipe tenha as permissões necessárias para administrar seus respectivos recursos, mantendo uma estrutura organizada entre os ambientes de **Homologação (HML)** e **Produção (PRD)**.

### Permissão utilizada

* **Role:** Contributor
* **Escopo:** Resource Group
* **Identidade:** Grupos de segurança do Microsoft Entra ID
* **Gerenciamento:** Azure RBAC / IAM

A função **Contributor** permite gerenciar os recursos dentro do Resource Group, sem conceder permissões para alterar as atribuições de acesso do próprio ambiente.

---

## Subscription — CENPC HML

Ambiente destinado a **Homologação**, utilizado para testes, validações e desenvolvimento.

| Resource Group      | Grupo do Entra ID     | Função      |
| ------------------- | --------------------- | ----------- |
| `rg-cloud-ti-dev`   | `gp_ti_cloud_dev_hml` | Contributor |
| `rg-cloud-ti-infra` | `gp_ti_cloud_infra`   | Contributor |
| `rg-cloud-mkt`      | `gp_mkt_cloud_hml`    | Contributor |

### Estrutura de acesso

**TI — Desenvolvimento**

* Resource Group: `rg-cloud-ti-dev`
* Grupo: `gp_ti_cloud_dev_hml`
* Permissão: **Contributor**

**TI — Infraestrutura**

* Resource Group: `rg-cloud-ti-infra`
* Grupo: `gp_ti_cloud_infra`
* Permissão: **Contributor**

**Marketing**

* Resource Group: `rg-cloud-mkt`
* Grupo: `gp_mkt_cloud_hml`
* Permissão: **Contributor**

---

## Subscription — CENPC PRD

Ambiente destinado à **Produção**, contendo os recursos utilizados pelos serviços em operação.

| Resource Group      | Grupo do Entra ID       | Função      |
| ------------------- | ----------------------- | ----------- |
| `rg-cloud-ti-dev`   | `gp_ti_cloud_dev_prd`   | Contributor |
| `rg-cloud-ti-infra` | `gp_ti_cloud_infra_prd` | Contributor |
| `rg-cloud-mkt`      | `gp_mkt_cloud_prd`      | Contributor |

### Estrutura de acesso

**TI — Desenvolvimento**

* Resource Group: `rg-cloud-ti-dev`
* Grupo: `gp_ti_cloud_dev_prd`
* Permissão: **Contributor**

**TI — Infraestrutura**

* Resource Group: `rg-cloud-ti-infra`
* Grupo: `gp_ti_cloud_infra_prd`
* Permissão: **Contributor**

**Marketing**

* Resource Group: `rg-cloud-mkt`
* Grupo: `gp_mkt_cloud_prd`
* Permissão: **Contributor**

---

## Modelo de organização

A estrutura foi criada separando os acessos por:

**Subscription → Resource Group → Grupo do Entra ID → Role RBAC**

Essa abordagem facilita a administração das permissões e permite manter uma separação clara entre os ambientes de **Homologação** e **Produção**.

### Benefícios da implementação

* 🔐 Controle de acesso baseado em funções (RBAC)
* 👥 Gerenciamento de permissões por grupos
* 🏢 Separação entre ambientes HML e PRD
* 📦 Permissões aplicadas diretamente no escopo dos Resource Groups
* 📋 Maior organização e facilidade de auditoria
* 🔄 Facilidade para inclusão ou remoção de usuários através dos grupos
* 🛡️ Aplicação do princípio de menor privilégio dentro do escopo definido

## Tecnologias e conceitos

* Microsoft Azure
* Microsoft Entra ID
* Azure RBAC
* IAM (Identity and Access Management)
* Resource Groups
* Role-Based Access Control
* Access Management
* Controle de acesso por grupos
* Gestão de ambientes HML e PRD
