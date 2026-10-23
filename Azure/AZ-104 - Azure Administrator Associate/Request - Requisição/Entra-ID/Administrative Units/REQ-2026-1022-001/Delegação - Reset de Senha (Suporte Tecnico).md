
# 🎫 CHAMADO ADMINISTRATIVE UNITS — Reset de Senha ( Suporte Técnico)

* Número do chamado: REQ-2026-1022-001
* Categoria: Delegação | reset de senha | Suporte técnico
* Prioridade: Média
* Solicitante: Financeiro
* Equipe responsável: Suporte Técnico
* Status: 
    ```
    ☑ Em análise
    ☐ Em implementação
    ☐ Aguardando validação
    ☐ Concluído
    ```

# 1. 📌 Descrição.

* Criar uma Administrative Units para equipe do **Support** com foco na delegação controlada de operações relacionadas à "reset de senha da equipe" **Marketing**.

# 2. 📝 Atendimento | 📸 Evidências.

* Com perfil de *Global Administrator* no **Portal Azure** > Entra ID > Manage > *Administrative Units*.

    <img src="./img/01.png" width="700">

* Em *Administrative Units* > ADD .

    <img src="./img/02.png" width="700">

    * **Properties**:

        <img src="./img/03.png" width="650">

    * **Assign roles**: Selecionada a opção **Password Administrator**.

        <img src="./img/04.png" width="650">

        * Adicionados os usuários da equipe do suporte técnico.

            <img src="./img/05.png" width="600">

    * **Review + Create**

        <img src="./img/06.png" width="650">

* Administrative criada com sucesso.

    <img src="./img/07.png" width="700">

* Após acessar a unidade administrativa que foi criada, em *Manage > Groups > ADD*.  
    
    <img src="./img/08.png" width="700">

    * Selecionado o grupo onde fazem parte todos os usuários da equipe de MKT.

        <img src="./img/09.png" width="650">

    * Grupo adicionado com sucesso.

        <img src="./img/10.png" width="650">

    ```Text

       * Grupos de associação dinânica costumam demorar algumas horas para aplicar os privilégios.

    ```

# 3. 💻 Comandos / Scripts Utilizados

> Registrar somente os comandos relevantes para reprodução do procedimento.

```powershell

    Nenhum comando foi executado.

```
# 4. 🔎 Validação dos usuários

* Autenticando com o usuário *junior.uacher@cenpc.shop* da equipe do Suporte técnico para validar os procedimentos que foram realizados.

    <img src="./img/11.png" width="700">

* Em seguida **ENTRA ID > Gerenciar > Usuários** foi selecionado um colaborador da equipe de MKT para realizar a alteração da senha.

    <img src="./img/12.png" width="700">

* Após escolher a colaboradora, a opção para redefinir a senha estava disponivel.

    <img src="./img/13.png" width="700">

# 5. 📸 Evidências

```
📁 REQ-2026-1022-001
└── 📁 img
    ├── 📄 01.png
    ├── 📄 02.png
    ├── 📄 03.png
    ├── 📄 04.png
    ├── 📄 05.png
    ├── 📄 06.png
    ├── 📄 07.png
    ├── 📄 08.png
    ├── 📄 09.png
    ├── 📄 10.png
    ├── 📄 11.png
    ├── 📄 12.png
    └── 📄 13.png
```
    
# 6.🏁 Encerramento

* Status:

    ```
    ☐ Em análise
    ☐ Em implementação
    ☐ Aguardando validação
    ☑ Concluído
    ```

* Analista responsável: Fábio Silva

#