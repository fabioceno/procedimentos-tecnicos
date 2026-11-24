# Windows Ativação - Tirando marca D´água do Wallpaper do Windows via GPO.

# 📌 Descrição.

* Procedimento para retirar a marca d´agua de ativação do Windows.

    <img src="./img/ativacao windows/01.png" width="700">

# 📝 Procedimentos | 📸 Evidências | 💻 Comandos | 🛠️ Scripts .

1. Na ferramenta *Group Policy Management* foi criada uma nova GPO.

    <img src="./img/ativacao windows/02.png" width="700">

2. Em seguida foi editada a politica **Computer Configuration > Preferences > Windows Settings > Registry > New > Regisrty Item**.

    <img src="./img/ativacao windows/03.png" width="700">

    * **Action**: Replace
    * **Hive**: HKEY_LOCAL_MACHINE
    * **Key Path**: SOFTWARE\Microsoft\Windows NT\CurrentVersion\Windows
    * **Value name | Default**: displaynotret
    * **Value Type** Qword
    * **Value Data**: 0

        <img src="./img/ativacao windows/04.png" width="600">
    
    * Verificado que a policy foi criada.

        <img src="./img/ativacao windows/05.png" width="600">

3. A GPO foi associada a OU computer.

    <img src="./img/ativacao windows/06.png" width="700">

4. Executado o comando abaixo para atualização das GPO´S.

    ```Powershell

        gpupdate /force

    ```
5. Foi realizado o procedimento de reiniciar o computador cliente.

    <img src="./img/ativacao windows/07.png" width="700">

# ✅ Resultado

* Após reiniciar o computador cliente, a GPO foi aplicada com sucesso onde a marca d´agua foi retirada do Wallpaper. 

    <img src="./img/ativacao windows/08.png" width="700">



#