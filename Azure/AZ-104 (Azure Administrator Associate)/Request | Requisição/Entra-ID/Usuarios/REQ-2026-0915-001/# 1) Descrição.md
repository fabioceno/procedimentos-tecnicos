# CHAMADO — CRIAÇÃO DE CONTAS DE USUÁRIOS

Área solicitante: Recursos Humanos (RH)
Área responsável: Cloud / Identity & Access Management (IAM)
Categoria: Gestão de Identidades e Acessos
Subcategoria: Criação de usuários
Prioridade: Média
Ambiente: Corporativo
Solicitante: Recursos Humanos
Tipo de solicitação: Admissão de novos colaboradores

1. Descrição da Solicitação

   O departamento de Recursos Humanos (RH) solicita à equipe de Cloud/IAM a criação de 08 novas contas de usuários no ambiente corporativo, destinadas a novos colaboradores das equipes de Marketing e Development.

   A solicitação faz parte do processo de admissão de novos colaboradores e tem como objetivo garantir que os usuários tenham suas identidades criadas no Microsoft Entra ID, permitindo posteriormente a atribuição das permissões, grupos, licenças e demais recursos necessários para execução de suas atividades.

   ### Quantidade solicitada

   | Departamento | Quantidade |
   | ------------ | ---------: |
   | Development  |          4 |
   | **Total**    |      **4** |

---

# 2. Equipe de Development

### Usuário 01

* **Nome:** Gabriel Souza Pereira
* **Cargo:** Desenvolvedor Júnior
* **Departamento:** Development
* **Gestor:** André Luiz Carvalho
* **Localidade:** Rio de Janeiro/RJ
* **Data de admissão:** 21/09/2026
* **Tipo de vínculo:** CLT
* **E-mail corporativo sugerido:** [gabriel.pereira@cenpc.shop](mailto:gabriel.pereira@cenpc.shop)
* **UPN:** [gabriel.pereira@cenpc.shop](mailto:gabriel.pereira@cenpc.shop)

### Usuário 02

* **Nome:** Felipe Rodrigues Nunes
* **Cargo:** Desenvolvedor Pleno
* **Departamento:** Development
* **Gestor:** André Luiz Carvalho
* **Localidade:** Rio de Janeiro/RJ
* **Data de admissão:** 21/09/2026
* **Tipo de vínculo:** CLT
* **E-mail corporativo sugerido:** [felipe.nunes@cenpc.shop](mailto:felipe.nunes@cenpc.shop)
* **UPN:** [felipe.nunes@cenpc.shop](mailto:felipe.nunes@cenpc.shop)

### Usuário 03

* **Nome:** Beatriz Martins Rocha
* **Cargo:** Desenvolvedora Sênior
* **Departamento:** Development
* **Gestor:** André Luiz Carvalho
* **Localidade:** São Paulo/SP
* **Data de admissão:** 21/09/2026
* **Tipo de vínculo:** CLT
* **E-mail corporativo sugerido:** [beatriz.rocha@cenpc.shop](mailto:beatriz.rocha@cenpc.shop)
* **UPN:** [beatriz.rocha@cenpc.shop](mailto:beatriz.rocha@cenpc.shop)

### Usuário 04

* **Nome:** Thiago Mendes Barbosa
* **Cargo:** Tech Lead
* **Departamento:** Development
* **Gestor:** André Luiz Carvalho
* **Localidade:** São Paulo/SP
* **Data de admissão:** 21/09/2026
* **Tipo de vínculo:** CLT
* **E-mail corporativo sugerido:** [thiago.barbosa@cenpc.shop](mailto:thiago.barbosa@cenpc.shop)
* **UPN:** [thiago.barbosa@cenpc.shop](mailto:thiago.barbosa@cenpc.shop)

---

# 3. Requisitos para a Equipe de Cloud/IAM

Solicitamos que, após a validação dos dados fornecidos pelo RH, sejam realizadas as seguintes atividades:

1. Criar as respectivas identidades dos 04 colaboradores no **Microsoft Entra ID**.
2. Configurar:

   * Nome completo: ;
   * Display Name: ;
   * User Principal Name (UPN): ;
   * Departamento: ;
   * Cargo (Job Title): ;
   * Localidade: ;
   * Gestor responsável: .

3. Garantir que os usuários sejam criados como **Member** no diretório corporativo.
4. Adicionar os usuários aos respectivos grupos corporativos conforme a matriz de acesso vigente.
5. Aplicar as licenças Microsoft 365/Azure conforme o perfil de cada colaborador e política de licenciamento da empresa.
6. Garantir que os usuários estejam sujeitos às políticas corporativas de autenticação e segurança, incluindo MFA e demais políticas de Conditional Access aplicáveis.
7. Não conceder permissões administrativas ou privilégios elevados sem solicitação e aprovação formal.
8. Registrar as ações realizadas no chamado para fins de auditoria.

---

# 4. Matriz Inicial de Alocação

| Usuário                 | Departamento | Cargo                        | Grupo sugerido        |
| ----------------------- | ------------ | ---------------------------- | --------------------- |
| Gabriel Souza Pereira   | Development  | Desenvolvedor Júnior         | `gp_ti_cloud_dev_hml` |
| Felipe Rodrigues Nunes  | Development  | Desenvolvedor Pleno          | `gp_ti_cloud_dev_hml` |
| Beatriz Martins Rocha   | Development  | Desenvolvedora Sênior        | `gp_ti_cloud_dev_hml` |
| Thiago Mendes Barbosa   | Development  | Tech Lead                    | `gp_ti_cloud_dev_hml` |

---

# 5. Critérios de Aceite

O chamado poderá ser considerado concluído após:

* [ ] As 08 contas serem criadas com sucesso.
* [ ] Os atributos dos usuários serem preenchidos conforme informações fornecidas pelo RH.
* [ ] Os usuários serem associados aos respectivos grupos.
* [ ] A equipe de Cloud/IAM registrar evidências da execução.
* [ ] O RH ser informado sobre a conclusão da solicitação.

---

## 6. Observação de Segurança

As credenciais iniciais dos usuários deverão ser geradas e disponibilizadas de acordo com o procedimento corporativo de segurança.

**Não registrar senhas, códigos MFA, tokens ou outros dados de autenticação diretamente neste chamado.**

---

* **Solicitante:** Recursos Humanos
* **Responsável pela execução:** Cloud / IAM
* **Status:** Aberto
* **Data da solicitação:** 15/09/2026

---
