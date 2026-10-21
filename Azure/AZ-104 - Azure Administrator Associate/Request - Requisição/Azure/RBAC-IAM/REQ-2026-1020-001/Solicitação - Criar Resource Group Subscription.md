# CHAMADO DE ACESSO — Permissão para criar Resource Groups na Subscription

* Número do chamado: REQ-2026-1020-001
* Categoria: Permissão | RBAC | Resource Groups
* Prioridade: Média
* Solicitante: TI Development
* Equipe responsável: Suporte Técnico
* Status:

    ```
    ☑ Em análise
    ☐ Em implementação
    ☐ Aguardando validação
    ☐ Concluído
    ```
# 1. 📌 Descrição.

* Solicito que os colaboradores com o perfil de *Analista Sênior* e os *Gerentes* da equipe de **Development** possam ter permissão de criar Resources Groups na Subscription.

# 2. 📝 Atendimento | 📸 Evidências.

* Consultando os usuários que estão nos grupos de gerente e analista senior.

    * Gerente: 

        <img src="./img/01.png" width="700">

    * Analista Senior:

        <img src="./img/02.png" width="700">

* Portal Azure > Subscription > Access Control (IAM) > Add > Add role assignment.

* Em *Privileged Administrator Roles* selecionada permissão de *Contributor* > Next.

    <img src="./img/03.png" width="700">

* Em Members > *Members* > selecionado os grupos que foram solicitados no chamado.  

    <img src="./img/04.png" width="700">

* Colocada uma descrição por questões de auditoria.

    <img src="./img/05.png" width="700">

* Em **Assignment type** selecionado *Ativo* e **Assignment duration** selecionado *Permanente*.

    <img src="./img/06.png" width="700">

* Salvadas as alterações com sucesso.

# 3. 💻 Comandos / Scripts Utilizados

> Registrar somente os comandos relevantes para reprodução do procedimento.

* Nenhum comando foi realizado para este atendimento.

```powershell
# Exemplo
```

# 4. 🔎 Validação dos usuários

* Os usuários dos grupos autorizados realizam logon no portal do Azure.

    * Gerente - (juca.uacher@cenpc.shop):

        <img src="./img/07.png" width="700"> 

    * Analistas Sênior :
    
    - (beatriz.rocha@cenpc.shop).

        <img src="./img/08.png" width="700">
        
    - (paulo.souza@cenpc.shop).

        <img src="./img/09.png" width="700">

    
# 5.🏁 Encerramento

* *Solicitação atendida e validada com sucesso.*

* Próxima ação: *Nenhuma ação pendente.*

* Status: 

```text
    
    ☐ Em análise
    ☐ Em implementação
    ☐ Aguardando validação
    ☑ Concluído

```
* Analista responsável: Fabio Silva

#