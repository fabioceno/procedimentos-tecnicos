# POWERSHELL - Verificando o status de uma porta de comunicação na rede.

# 1. 📌 Descrição.

* Procedimento para procurar portas de comunicações que estão abertas ou fechadas na rede via Powershell.

# 📝 Procedimentos | 📸 Evidências | 💻 Comandos / Scripts Utilizados.

1) Inicie o *Terminal* ou *Prompt Powershell* como **Administrador local**.

    <img src="./img/img-eth01.png" width="700">

2) Execute o comando *conforme a imagem no exemplo abaixo*.

    * Neste exemplo a porta de comunicação está aberta.

        ```powershell
        
            tnc google.com -port 80
        
        ```
        <img src="./img/img-sts01.png" width="700">    

    * Neste exemplo a porta de comunicação está fechada.

        ```powershell
        
            tnc google.com -port 3389
        
        ```
        <img src="./img/img-sts02.png" width="700">    

# 🏁 Encerramento

### Com os procedimentos realizados acima podemos diagnostticar se uma determinada porta de um site ou até mesmo de um servidor está aberta ou fechada na rede.

* **Atualizado em:** 17/10/2026

* **Autor:** Fabio Silva