# 🎫 CHAMADO -  

* Número do chamado: REQ-2026-1109-001
* Categoria: Cloud Computing | Azure | Governança de Recursos
* Serviço: Microsoft Entra ID
* Tipo de solicitação: Configuração e padronização de ambiente Cloud
* Prioridade: Média
* Solicitante: IT Infraestrutura.
* Equipe responsável: Suporte Técnico
* Status: 

    ```
    ☑ Em análise
    ☐ Em implementação
    ☐ Aguardando validação
    ☐ Concluído
    ```

# 1. 📌 Descrição.

* Solicito que coloque a TAG com o nome da instituição direto na subscription para que sejam herdadas pelos Grupos de recursos e recursos.

    * **Company Name** - *"Nome da Instituição"*: **CENPC**
    
    * **Workload** - *"Identificar a carga de trabalho"*: **Cloud Computing**   

# 2. 📝 Atendimento | 📸 Evidências.

* Customizando a Politica para herdar as TAGS da Subscription para os Resources Groups e os Recursos.

```JSON
{
    "displayName": "CENPC - Herdar uma marca da assinatura para RG e Recursos",
    "policyType": "Custom",
    "mode": "All",
    "description": "Inherits and replaces the specified tag and value from the subscription to resource groups.",
    "metadata": {
      "category": "Tags",
      "version": "1.0.1"
    },
    "parameters": {
      "tagName1": {
        "type": "String",
        "metadata": {
          "displayName": "First Tag Name",
          "description": "Informe o nome da TAG, Exemplo: 'Company Name'."
        }
      },
      "tagValue1": {
        "type": "String",
        "metadata": {
          "displayName": "First Tag Value",
          "description": "Valor da primeira TAG. Exemplo: CENPC"
        }
      },

    "tagName2": {
      "type": "String",
      "metadata": {
        "displayName": "Second Tag Name",
        "description": "Informe o nome da TAG, Exemplo: 'Workload - Identificar a carga de trabalho'"
      }
    },
      "tagValue2": {
        "type": "String",
        "metadata": {
          "displayName": "Second Tag Value",
          "description": "Valor da segunda TAG. Exemplo: Production"
        }
      }
    },
    "policyRule": {
      "if": {
        "allOf": [
          {
          "field": "[concat('tags[', parameters('tagName1'), ']')]",
          "notEquals": "[parameters('tagValue1')]"
          },
          {
          "field": "[concat('tags[', parameters('tagName2'), ']')]",
          "notEquals": "[parameters('tagValue2')]"
          }
        ]
      },
      "then": {
        "effect": "modify",
        "details": {
          "roleDefinitionIds": [
            "/providers/Microsoft.Authorization/roleDefinitions/b24988ac-6180-42a0-ab88-20f7382dd24c"
          ],
          "operations": [
            {
            "operation": "addOrReplace",
            "field": "[concat('tags[', parameters('tagName1'), ']')]",
            "value": "[parameters('tagValue1')]"
            },
          {
            "operation": "addOrReplace",
            "field": "[concat('tags[', parameters('tagName2'), ']')]",
            "value": "[parameters('tagValue2')]"
          }
          ]
        }
      }
    }
  }

```
* Customizando Policy para Herdar TAG dos Resources Groups para os recursos.

```JSON
    {
    "displayName": "CENPC - Herdar uma marca do grupo de recursos",
    "policyType": "Custom",
    "mode": "Indexed",
    "description": "Adds or replaces and update multiple tags from the resource group.",
    "metadata": {
        "category": "Tags"
    },
    "parameters": {
        "tagName1": {
        "type": "String",
        "metadata": {
            "displayName": "First Tag Name",
            "description": "Informe o nome da TAG, Exemplo: 'Ambiente'"
        }
        },
        "tagName2": {
        "type": "String",
        "metadata": {
            "displayName": "Second Tag Name",
            "description": "Informe o nome da TAG, Exemplo: 'Centro de Custo'"
        }
        },
        "tagName3": {
        "type": "String",
        "metadata": {
            "displayName": "Third Tag Name",
            "description": "Informe o nome da TAG, Exemplo: 'Departamento'"
        }
        },
        "tagName4": {
        "type": "String",
        "metadata": {
            "displayName": "Fourth Tag Name",
            "description": "Informe o nome da TAG, Exemplo: 'Owner do projeto'"
        }
        },
        "tagName5": {
        "type": "String",
        "metadata": {
            "displayName": "Fifth Tag Name",
            "description": "Informe o nome da TAG, Exemplo: 'Nome do Projeto'"
        }
        },
        "tagName6": {
        "type": "String",
        "metadata": {
            "displayName": "Sixth Tag Name",
            "description": "Informe o nome da TAG, Exemplo: 'Equipe'"
        }
        }    
    },
    "policyRule": {
        "if": {
        "anyOf": [
            {
            "field": "[concat('tags[', parameters('tagName1'), ']')]",
            "notEquals": "[resourceGroup().tags[parameters('tagName1')]]"
            },
            {
            "field": "[concat('tags[', parameters('tagName2'), ']')]",
            "notEquals": "[resourceGroup().tags[parameters('tagName2')]]"
            },
            {
            "field": "[concat('tags[', parameters('tagName3'), ']')]",
            "notEquals": "[resourceGroup().tags[parameters('tagName3')]]"
            },
            {
            "field": "[concat('tags[', parameters('tagName4'), ']')]",
            "notEquals": "[resourceGroup().tags[parameters('tagName4')]]"
            },
            {
            "field": "[concat('tags[', parameters('tagName5'), ']')]",
            "notEquals": "[resourceGroup().tags[parameters('tagName5')]]"
            },
            {
            "field": "[concat('tags[', parameters('tagName6'), ']')]",
            "notEquals": "[resourceGroup().tags[parameters('tagName6')]]"
            }        
        ]
        },
        "then": {
        "effect": "modify",
        "details": {
            "roleDefinitionIds": [
            "/providers/Microsoft.Authorization/roleDefinitions/4a9ae827-6dc8-4573-8ac7-8239d42aa03f"
            ],
            "operations": [
            {
                "operation": "addOrReplace",
                "field": "[concat('tags[', parameters('tagName1'), ']')]",
                "value": "[resourceGroup().tags[parameters('tagName1')]]"
            },
            {
                "operation": "addOrReplace",
                "field": "[concat('tags[', parameters('tagName2'), ']')]",
                "value": "[resourceGroup().tags[parameters('tagName2')]]"
            },
            {
                "operation": "addOrReplace",
                "field": "[concat('tags[', parameters('tagName3'), ']')]",
                "value": "[resourceGroup().tags[parameters('tagName3')]]"
            },
            {
                "operation": "addOrReplace",
                "field": "[concat('tags[', parameters('tagName4'), ']')]",
                "value": "[resourceGroup().tags[parameters('tagName4')]]"
            },
            {
                "operation": "addOrReplace",
                "field": "[concat('tags[', parameters('tagName5'), ']')]",
                "value": "[resourceGroup().tags[parameters('tagName5')]]"
            },
            {
                "operation": "addOrReplace",
                "field": "[concat('tags[', parameters('tagName6'), ']')]",
                "value": "[resourceGroup().tags[parameters('tagName6')]]"
            }          
            ]
        }
        }
    }
    }
```
* Na Subscription foram inseridas as TAGS solicitadas.

    <img src="./img/01.png" width="700">

* Nos resources groups e nos recursos, não existem TAGS aplicadas.

    * rg-ti-dev-hml

        <img src="./img/001.png" width="600">

    * stgcenpctidevhml0001

       <img src="./img/002png" width="600">

    * rg-ti-dev-prd

        <img src="./img/003png" width="600">

    * stgcenpctidevprd0001 

        <img src="./img/004png" width="600">


* Com perfil de Owner ou Contributor na subscriptyion, Portal Azure > *Pesquisar -> Policy* > Authoring > Definitions.

* Em seguida, procure por TAG e localize a "**TAG de herança para subscription - Inherit a tag from the subscription**".

* Clique nos "*3 pontos*" > duplication definition.

    <img src="./img/02.png" width="700">

    * Edite a TAG na guia **BASICS**.

        <img src="./img/03.png" width="600">
    
    * Ainda na guia BASICIS porem na área *Policy Rule*, remova o codigo DEFAULT.

        <img src="./img/04.png" width="600">

    * Após remover, cole o código que foi editado.

        <img src="./img/05.png" width="600">

    * Em *Role Definitions* selecione **Tag Contributor** e clique em **SALVAR**.

        <img src="./img/06.png" width="600">

* Ainda em Definitions, localize a TAG "*Inherit a tag from the resource group*" > Duplicate Definition.

    * Edite a TAG na guia **BASICS**.

        <img src="./img/07.png" width="600">

    * Ainda na guia BASICIS porem na área *Policy Rule*, remova o codigo DEFAULT.

        <img src="./img/08.png" width="600">

    * Após remover, cole o código que foi editado.

        <img src="./img/09.png" width="600">

    * Em *Role Definitions* selecione **Tag Contributor** e clique em **SALVAR**.

        <img src="./img/10.png" width="600">

* Com as TAGs criadas, clique em **Assignments** > clique em **Assign Policy**.

    <img src="./img/11.png" width="700">

    * Na guia **BASICS** > *BASIC* > *Policy definition* selecione a politica que foi customizada "Que é para Herdar as TAGs da Subscription".

        <img src="./img/12.png" width="600">

    * Tag adicionada, clique em Próximo.

        <img src="./img/13.png" width="600">
    
    * Na guia **PARAMETROS** informe as TAGS que deverão constar por padrão.

        <img src="./img/14.png" width="600">

    * Na guia Remediação, selecione a opção "**Create a remediation task**".

        <img src="./img/15.png" width="600">

    * Para finalizar, clique em **CREATE**.

        <img src="./img/16.png" width="600">

* Politica associada com sucesso.

    <img src="./img/17.png" width="700">

* Para policy nos resources Groups, os mesmos passos foram realizados. "clique em **Assignments** > clique em **Assign Policy**."

    <img src="./img/18.png" width="700">

* Politica associada com sucesso.

    <img src="./img/19.png" width="700">

* No Resource Group de HML foram inseridas as TAGS.

    <img src="./img/20.png" width="700">

    * Após atualizar a página, as TAGS herdadas da Subscription foram adicionadas o RG.

        <img src="./img/21.png" width="600">

* No Resource Group de PRD foram inseridas as TAGS.

    <img src="./img/22.png" width="700">

    * Após atualizar a página, as TAGS herdadas da Subscription foram adicionadas o RG.

        <img src="./img/23.png" width="600">


# 3. 💻 Comandos / Scripts Utilizados

> Registrar somente os comandos relevantes para reprodução do procedimento.

```PowerShell

    Nenhum comando foi execitado

```
# 4. 🔎 Validação dos usuários

* Conforme a solicitação foram criadas politicas para adicionar/herdar as TAGS automaticamente nos recursos tanto da Subscription como do Resource Group.

    * Storage Account de homologação.

        <img src="./img/24.png" width="600">

    * Storage Account de produção.

        <img src="./img/25.png" width="600">

# 5. 📸 Evidências

```
📁 REQ-2026-1109-001
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
    ├── 📄 13.png
    ├── 📄 14.png
    ├── 📄 15.png
    ├── 📄 16.png
    ├── 📄 17.png
    ├── 📄 18.png
    ├── 📄 19.png
    ├── 📄 20.png
    ├── 📄 21.png
    ├── 📄 22.png
    ├── 📄 23.png
    ├── 📄 24.png
    └── 📄 25.png
```
   
# 6.🏁 Encerramento

* **Motivo do encerramento:** Solicitação atendida e validada com sucesso.

* **Próxima ação:** Nenhuma ação pendente.

* Status:

    ```
    ☐ Em análise
    ☐ Em implementação
    ☐ Aguardando validação
    ☑ Concluído
    ```

* Analista responsável: Fabio Silva

#