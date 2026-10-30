# 🎫 CHAMADO DE ACESSO — LIBERAÇÃO NO RESOURCE GROUP HML

* Número do chamado: REQ-2026-1029-001
* Categoria: RBAC | RESOURCE GROUP | Permissões
* Prioridade: Média
* Solicitante: Development | Juca Uacher
* Equipe responsável: Suporte Técnico - IAM
* Status: 

    ```
    ☑ Em análise
    ☐ Em implementação
    ☐ Aguardando validação
    ☐ Concluído
    ```

# 1. 📌 Descrição.

* O colaborador Juca Uacher solicitou que fossem atribuida a função RBAC para os colaboradores:
    
    * Management Group CENPC:

        * **Contributor** para os colaboradores com **JobTitle** *Gerente* 
    
    * Subscription:
        
        * **Contributor** para os colaboradores com **JobTitle** *Analista Senior*

    * Resource Group DEV:
        
        * **Contributor** no Resource Group da equipe de DEV para os colaboradores com **JobTitle** *Analista Pleno*
 
# 2. 📝 Atendimento | 📸 Evidências.

* No portal Azure *Com perfil Owner* > Pesquisa *Management Group* > Origanization > Management Group > Tenant Root Group > CENPC.

    <img src="./img/01.png" width="700">

* Em seguida, **Access Control (IAM - RBAC)** *Liberando permissão de contributor para os gerentes da equipe Development.* > Add > ADD role assignment.

    <img src="./img/02.png" width="700">

    * Em **Role > Privileged Administrator Role** selecionado a opção **Contributor** > NEXT.

        <img src="./img/03.png" width="700">
    
    * Em **Members**, foi selecionado o grupo que pertence os usuários com **JobTitle=Gerente**.

        <img src="./img/04.png" width="700">

    * Em **Condições**, nenhuma condição foi adicionada.

        <img src="./img/05.png" width="700">

    * Em **Assignment Type** foi selecionada *ACTIVE* E **ASSIGNMENT DURATION** foi selecionado *Permanente*.

        <img src="./img/06.png" width="700">

    * Finalizando os procedimentos, clicando em **Review + Assign**.

        <img src="./img/07.png" width="700">

* Após concluir o procedimento anterior, em **Resource Management > Management Groups > CENPC** foi acessado o campo de **Subscription**.

    <img src="./img/08.png" width="700">

* Clicando no link da subscription para ter acesso ao recurso.

    <img src="./img/09.png" width="700">

* Na subscription > **Access Control (IAM) > ADD > Add role Assignemt**.

    <img src="./img/10.png" width="700">

    * Em **Role > Privileged Administrator Role** selecionado a opção **Contributor** > NEXT.

        <img src="./img/11.png" width="700">

    * Selecionado o grupo de colaboradores com o perfil **Analista Senior**.

        <img src="./img/12.png" width="700">

    * Em **Assignment Type** foi selecionada *ACTIVE* E **ASSIGNMENT DURATION** foi selecionado *Permanente*.

        <img src="./img/13.png" width="700">

    * Finalizando os procedimentos, clicando em **Review + Assign**.

        <img src="./img/14.png" width="700">

* Após concluir o procedimento anterior, em **Resource Management > Management Groups > CENPC** foi acessado o campo de **Resource Group** e selecionado o rg-dev-hml-01.

    <img src="./img/15.png" width="700">

    * Dentro do resource group, **Access Control (IAM - RBAC)** *Liberando permissão de contributor para os Analistas Pleno da equipe Development.* > Add > ADD role assignment.

        <img src="./img/16.png" width="700">
    
    *  Em **Role > Privileged Administrator Role** selecionado a opção **Contributor** > NEXT.

        <img src="./img/17.png" width="700">

    * Selecionado o grupo de colaboradores com o perfil **Analista Pleno**.

        <img src="./img/18.png" width="700">

    * Em **Assignment Type** foi selecionada *ACTIVE* E **ASSIGNMENT DURATION** foi selecionado *Permanente*.

        <img src="./img/19.png" width="700">
    
    * Finalizando os procedimentos, clicando em **Review + Assign**.

        <img src="./img/20.png" width="700">

# 3. 💻 Comandos / Scripts Utilizados

> Registrar somente os comandos relevantes para reprodução do procedimento.

```powershell

    Nenhum comando foi realizado.

```
# 4. 🔎 Validação dos usuários

* Como amostragem, foram realizados acessos com os perfis dos colaboradores:

    * Juca Uacher:

        * Consegue ter acesso a toda a estrutura do Management Group e Subscription, porem não consegue permitir acessos.

            <img src="./img/21.png" width="700">

    * Paulo Souza:

        * Consegue ter acesso a partir da subscription, é não consegue permitir acessos.

            <img src="./img/22.png" width="700">

        * Consegue visualizar outros Resource Groups criados.

            <img src="./img/22-1.png" width="700">

    * Felipe Nunes:

        * Não consegue visualizar as informações referente a subscription.

            <img src="./img/23.png" width="700">

        * Consegue visualizar somente o Resource Group que foi liberado.

            <img src="./img/23-1.png" width="700">
       

# 5.🏁 Encerramento

* Status:

    ```
    ☐ Em análise
    ☐ Em implementação
    ☐ Aguardando validação
    ☑ Concluído
    ```

* **Analista responsável:** Fabio Silva





