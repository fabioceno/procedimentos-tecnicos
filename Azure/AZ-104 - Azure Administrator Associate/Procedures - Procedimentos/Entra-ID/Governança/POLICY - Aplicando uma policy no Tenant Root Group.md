# Azure Policy - Aplicando politicas no Tenant Root Group.


# 📌 Descrição.

* Por padrão, não é possivel selecionar o **Tenant Root Group** para que seja associada uma Policy no escopo dele.

    <img src="./img/policy - tenant root group/01.png" width="700">

        " Não é possivel selecionar a opção Tenant Root Group. "

# 🎯 Objetivo:

        Estabelecer um procedimento para habilitar e realizar a associação de Policies no escopo do Tenant Root Group do Azure, considerando que, por padrão, esse escopo não está disponível para seleção direta durante a atribuição de políticas.
        
        O procedimento visa orientar os administradores na configuração das permissões necessárias e na aplicação centralizada de políticas de governança, garantindo a padronização, a conformidade e o controle dos recursos em todas as Management Groups e Subscriptions vinculadas ao tenant.

---

# 📝 Procedimentos | 📸 Evidências | 💻 Comandos | 🛠️ Scripts .

1) No Microsoft Entra ID > Manage > Propriedades > Access management for Azure resources, a opção "*User (user@outlook.com.br) can manage access to all Azure subscriptions and management groups in this tenant.*" está desabilitada.

    <img src="./img/policy - tenant root group/02.png" width="700">

    * **Habilite a opção** e **SALVE** as alterações.

    <img src="./img/policy - tenant root group/03.png" width="600">

2) Em seguida, procure por **Management Group**. 

    <img src="./img/policy - tenant root group/04.png" width="700">
    
3) Em **Organization** > **Management Groups, clique no link do Tenant Root Group.

    <img src="./img/policy - tenant root group/05.png" width="700">

    * Clique em **Access Control List - IAM | RBAC** > Role Assignment.

        <img src="./img/policy - tenant root group/06.png" width="600">

    * Para gerenciar o Tenant Root Group é necessário ter a permissão de **Owner**.

        <img src="./img/policy - tenant root group/07.png" width="600">
 
    * Para alterar as permissões para o usuário, clique em **ADD** > ADD Role Assignmemt.

        <img src="./img/policy - tenant root group/08.png" width="600">

        * Na guia **ROLE** > Privileged administrator roles > selecione *Owner* e clique em **Próximo**.

            <img src="./img/policy - tenant root group/09.png" width="550">

        * Em seguida na guia **MEMBERS** selecione o usuário que ira administrar o Tenant.

            <img src="./img/policy - tenant root group/10.png" width="550">
        
        * Na guia **Condicional** selecione a opção de mais privilégios e clique em **Próximo**.

            <img src="./img/policy - tenant root group/11.png" width="550">

        * Na guia **Assignment type** selecione *Active* e clique em **Review + Assign** para concluir as alterações.

            <img src="./img/policy - tenant root group/12.png" width="550">

        * Aguarde a concluir as alterações.

            <img src="./img/policy - tenant root group/13.png" width="550">
        
        * Alterações realizadas com sucesso.

            <img src="./img/policy - tenant root group/14.png" width="550">
    
4) Retornando para **políticas - policy** após as aterações, agora é possivel selecionar o **Tenant Root Group** para associar a politica.

    <img src="./img/policy - tenant root group/15.png" width="700">

# ✅ Resultado

* Após as alterações, é possível associar políticas ao Tenant Root Group ao escopo.

    <img src="./img/policy - tenant root group/16.png" width="700">

```
* Status: ☐ Em análise | ☐ Em implementação | ☐ Aguardando validação | ☑ Concluído

```
* Analista responsável: Fabio Silva

#