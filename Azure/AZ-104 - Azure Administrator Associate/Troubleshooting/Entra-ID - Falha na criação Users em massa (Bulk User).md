# 🎫 Entra ID - Bulk User: "O envio da operação em massa falhou".

Após realizar o ulpload do arquivo *.CSV* para o Entra ID e enviar o arquivo para processamento de **Bulk User** | *Criação de usuários em massa*, o portal retorna o **falha** conforme a imagem no exemplo abaixo.

<img src="./img/bulk-user00.png" width="700">.

## 🛠️ Procedimentos Executados 🛠️

1. Abra o arquivo *.CSV* que foi criado.

    <img src="./img/bulk-user01.png" width="700">.

2. Substitua o sinal de pontuação "**;**" pela "**,**".

    <img src="./img/bulk-user02.png" width="700">.

3. Inclua a seguinte linha de texto:

    *version:v1.0,,,,,,,,,,,,,,,,*

    <img src="./img/bulk-user03.png" width="700">.

    e em seguida antes do nome "*Chiris Green*" coloque a palavra *Exemplo*.

    <img src="./img/bulk-user04.png" width="700">.

4. Caso o *TENANT Entra ID* esteja com o idioma em *Português* no momento que for salvar o arquivo, altere em **Codificação** de *ANSI* ...

    <img src="./img/bulk-user05.png" width="700">.

    ... para *UTF-8*.

    <img src="./img/bulk-user06.png" width="700">.

5. Realize o procedimento de Upload e processamento do arquivo novamente.

    <img src="./img/bulk-user07.png" width="700">.

## ✅ Resultado

Os usuários foram cadastrados com sucesso.

   <img src="./img/bulk-user08.png" width="700">.