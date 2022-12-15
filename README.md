# wf_integracoes
Componentes de Integraçao com ClickSign
# Autenticação

<aside>
🔐 Headers de acesso
****authorization key Ocp-Apim-Subscription-Key
****

</aside>

## Chamada de API

O serviço do clicksign pode ser acessado via API, sendo necessário que sejam enviadas as informações em formato de payload “JSON”, respeitando os formatos pré-estabelecidos pela documentação da API do clicksign. Segue abaixo o resumo das informações da chamada de API REST

### Método: POST

### URL

```json
https://apim.looplex.com/actions/v1/code/integracao_clicksign
```

### Headers

```json
authorization key Ocp-Apim-Subscription-Key
```

### Body

```json
{
        "signers": [
            {
                "email": signer.email,
                "phone_number": signer.phone_number,
                "auths": [ "email" ],
                "name": signer.name,
                "documentation": signer.documentation,
                "has_documentation": true,
                "selfie_enabled": false,
                "handwritten_enabled": false,
                "official_document_enabled": false,
                "liveness_enabled": false,
                "facial_biometrics_enabled": false  
            }
        ],
        "document": {
            "path": "/Contrato de Prestação de Serviços-123.pdf",
            "content_base64": "data:application/pdf;base64,JVBERi0xLjcNCiXi48/TDQo0IDAgb2JqDQo8PA0KL......",
            "deadline_at": "2022-10-25T14:30:59-03:00",
            "auto_close": true,
            "locale": "pt-BR",
            "sequence_enabled": false,
            "block_after_refusal": false
        }
    }
```

---

### Documentação da API da ClickSign

[Informações gerais](https://developers.clicksign.com/docs/informacoes-gerais)
