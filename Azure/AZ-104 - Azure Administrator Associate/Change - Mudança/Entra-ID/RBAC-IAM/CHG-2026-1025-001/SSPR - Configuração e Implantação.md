
# 🎫 CHAMADO DE ACESSO — SITE P@ssw0rd! 

* Número do chamado: CHG-2026-1025-001.
* Categoria: Cloud Computing | Gestão de Identidades.
* Serviço: Microsoft Entra ID.
* Tipo de solicitação: Mudança | Implantação.
* Prioridade: Média.
* Solicitante: Gerência de Development.
* Equipe responsável: Cloud | Identity and Access Management (IAM).
* Status: 
    ```
    ☑ Em análise
    ☐ Em implementação
    ☐ Aguardando validação
    ☐ Concluído
    ```

# 1. 📌 Descrição.
```
    A equipe de Development solicita a implantação do recurso Self-Service Password Reset (SSPR) no Microsoft Entra ID, permitindo que seus colaboradores de nivel (Analista Senior) redefinam suas próprias senhas ou desbloqueiem o acesso, quando aplicável, sem a necessidade de abrir chamados para a equipe de TI.

    A iniciativa tem como objetivo reduzir o volume de solicitações relacionadas a senhas, aumentar a autonomia dos usuários e melhorar a disponibilidade operacional da equipe de desenvolvimento. 
```
# 2. 📝 Atendimento | 📸 Evidências.

* Com o perfil de Global Admin clique Entra ID > Manage > Password reset.

    <img src="./img/01.png" width="700">

* Selecionado o grupo dos usuários que possuem **JobTitle** *Analista Senior*.

    <img src="./img/02.png" width="700">

* Em **Passoword reset > Properties** > Authentication Methods > **Auth Methods Policy**.

    <img src="./img/03.png" width="700">

* Em **Auth Methods** foram habilitados:

    * Microsoft Authenticator.
    * Email OTP.

        <img src="./img/04.png" width="700">

* Aos colaboradores do grupo, foi informado o link para o cadastro o modelo de autenticação que será usado.

    * Link do SSPR Setup **https://aka.ms/ssprsetup**.
```
    * Para colaboradores que já possuem um metodo cadastrado, o mesmo terá que incluir-lo manualmente.

```
* No portal será exibido a tela solicitando as credenciais de acesso.

    * <img src="./img/04-1.png" width="700">
    
    * Solicitando a senha de acesso.

        <img src="./img/04-2.png" width="700">

    * Após a autenticação, clique na opção *Adicionar método de entrada*

        <img src="./img/04-3.png" width="700">

    * Escolha o segundo metodo para autenticação.

        <img src="./img/04-4.png" width="700">

```
    * Para colaboradores que não possuem um metodo cadastrado, se autenticando pela primeira vez.

```
* Inicialmente, será disponibilizada a tela de autenticação padrão.

    <img src="./img/04-5.png" width="700">

* Em seguida, será solicitado para cadastrar metodo de autenticação.

    <img src="./img/04-6.png" width="700">

* Incialmente, será solicitado o cadastro do MS Authenticator.

    <img src="./img/04-7.png" width="700">

* Authenticator cadastrado com sucesso.

    <img src="./img/04-8.png" width="700">

* Em seguida, será soicitado o segundo metodo para autenticação para redefinição da senha.
*"Tem que ser um e-mail fora da organização".*

   <img src="./img/04-9.png" width="700">

* Será enviado um código para o e-mail cadastrado.

   <img src="./img/04-10.png" width="700">

* O cadastro foi realizado com sucesso.

   <img src="./img/04-11.png" width="700">

# 3. 💻 Comandos / Scripts Utilizados

> Registrar somente os comandos relevantes para reprodução do procedimento.

```
    Nenhum comando foi usando para essa tarefa.
```

# 4. 🔎 Validação dos usuários

* Aos colaboradores, foi informado o link da página para acesso ao SSPR **https://passwordreset.microsoftonline.com**

    <img src="./img/05.png" width="700">

* O colaborador **paulo.souza@cenpc.shop** acessou o link **https://passwordreset.microsoftonline.com/** para realizar o teste de SSPR.

    <img src="./img/06.png" width="700">

* Em seguida, os metodos de reset da senha foram exibidos.

    <img src="./img/07.png" width="700">

* Após validação com o autenticator, a tela de inserir uma nova senha foi habilitada com sucesso.

    <img src="./img/08.png" width="700">

    * Link para o SSPR Setup **https://aka.ms/ssprsetup** onde ficam as informações referente os metodos de autenticação que foram cadastrados.

        <img src="./img/08-1.png" width="700">

* Para usuários que **não** estão no grupo, a função do SSPR não fica habilitada.

    * Foi realizado o teste com colaborador de outra equipe com o JobTitle diferente.

        <img src="./img/09.png" width="700">
    
    * O sistema retorna que não é possivel realizar o procedimento.

        <img src="./img/10.png" width="700">

# 5. 📸 Evidências

```
📁 REQ-2026-1022-001
└── 📁 img
    ├── 📄 01.png
    ├── 📄 02.png
    ├── 📄 03.png
    ├── 📄 04.png
    │   ├── 📄 04-1.png
    │   ├── 📄 04-2.png
    │   ├── 📄 04-3.png
    │   ├── 📄 04-4.png
    │   ├── 📄 04-5.png
    │   ├── 📄 04-6.png
    │   ├── 📄 04-7.png
    │   ├── 📄 04-8.png
    │   ├── 📄 04-9.png
    │   ├── 📄 04-10.png
    │   ├── 📄 04-11.png
    ├── 📄 05.png
    ├── 📄 06.png
    ├── 📄 07.png
    ├── 📄 08.png
    │   └── 📄 08-1.png
    ├── 📄 09.png    
    └── 📄 10.png
```
  
# 6.🏁 Encerramento

**Motivo do encerramento:** Solicitação atendida e validada com sucesso.

**Próxima ação:** Nenhuma ação pendente.

* Status:

    ```
    ☐ Em análise
    ☐ Em implementação
    ☐ Aguardando validação
    ☑ Concluído
    ```

* Analista responsável: Fabio Silva

#