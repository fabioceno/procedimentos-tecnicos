# Controle de Acesso aos Resource Groups

Estrutura de permissões baseada em **Microsoft Entra ID** e **Azure RBAC**, utilizando grupos de segurança para controlar o acesso aos Resource Groups.

O nível de permissão definido para os grupos abaixo é **Contributor**, permitindo aos usuários gerenciar os recursos existentes dentro dos respectivos Resource Groups, sem conceder permissões para gerenciar acessos e atribuições de funções (RBAC).

## Estrutura de Acesso

| Resource Group          | Grupo de Acesso         | Ambiente                      | Permissão       |
| ----------------------- | ----------------------- | ----------------------------- | --------------- |
| `rg-ti-cloud-dev-hml`   | `gp_ti_cloud_dev_hml`   | Desenvolvimento / Homologação | **Contributor** |
| `rg-ti-cloud-dev-prd`   | `gp_ti_cloud_dev_prd`   | Desenvolvimento / Produção    | **Contributor** |
| `rg-ti-cloud-infra-hml` | `gp_ti_cloud_infra_hml` | Infraestrutura / Homologação  | **Contributor** |
| `rg-ti-cloud-infra-prd` | `gp_ti_cloud_infra_prd` | Infraestrutura / Produção     | **Contributor** |
| `rg-ti-cloud-mkt-hml`   | `gp_mkt_cloud_hml`      | Marketing / Homologação       | **Contributor** |
| `rg-ti-cloud-mkt-prd`   | `gp_mkt_cloud_prd`      | Marketing / Produção          | **Contributor** |

## Detalhamento

### 1. Desenvolvimento – Homologação

**Resource Group:** `rg-ti-cloud-dev-hml`
**Grupo:** `gp_ti_cloud_dev_hml`
**Função:** `Contributor`

Grupo destinado aos usuários responsáveis pelo gerenciamento dos recursos da área de **Desenvolvimento** no ambiente de **Homologação**.

---

### 2. Desenvolvimento – Produção

**Resource Group:** `rg-ti-cloud-dev-prd`
**Grupo:** `gp_ti_cloud_dev_prd`
**Função:** `Contributor`

Grupo destinado aos usuários responsáveis pelo gerenciamento dos recursos da área de **Desenvolvimento** no ambiente de **Produção**.

---

### 3. Infraestrutura – Homologação

**Resource Group:** `rg-ti-cloud-infra-hml`
**Grupo:** `gp_ti_cloud_infra_hml`
**Função:** `Contributor`

Grupo destinado à equipe responsável pelo gerenciamento dos recursos de **Infraestrutura** no ambiente de **Homologação**.

---

### 4. Infraestrutura – Produção

**Resource Group:** `rg-ti-cloud-infra-prd`
**Grupo:** `gp_ti_cloud_infra_prd`
**Função:** `Contributor`

Grupo destinado à equipe responsável pelo gerenciamento dos recursos de **Infraestrutura** no ambiente de **Produção**.

---

### 5. Marketing – Homologação

**Resource Group:** `rg-ti-cloud-mkt-hml`
**Grupo:** `gp_mkt_cloud_hml`
**Função:** `Contributor`

Grupo destinado aos usuários responsáveis pelo gerenciamento dos recursos utilizados pela área de **Marketing** no ambiente de **Homologação**.

---

### 6. Marketing – Produção

**Resource Group:** `rg-ti-cloud-mkt-prd`
**Grupo:** `gp_mkt_cloud_prd`
**Função:** `Contributor`

Grupo destinado aos usuários responsáveis pelo gerenciamento dos recursos utilizados pela área de **Marketing** no ambiente de **Produção**.

## Modelo de Governança

A estrutura segue uma abordagem de **Role-Based Access Control (RBAC)**, utilizando grupos do Microsoft Entra ID para facilitar a administração das permissões.

**Usuário → Grupo Entra ID → Resource Group → Azure RBAC → Contributor**

Essa abordagem permite:

* Centralizar o gerenciamento de acessos;
* Evitar atribuições individuais sempre que possível;
* Separar os acessos por área e ambiente;
* Facilitar auditorias e revisões de permissões;
* Simplificar a entrada e saída de usuários das equipes;
* Aplicar o princípio de segregação de ambientes;
* Manter maior organização e governança dos recursos Azure.

> **Observação:** A função **Contributor** permite criar, alterar e excluir recursos dentro do escopo atribuído, mas não permite gerenciar atribuições de acesso no Azure RBAC.

