---
description: >-
  Ao utilizar nossa API talvez você se depare com certas mensagens de erro,
  nesta seção vamos descrevê-las e oque pode estar causando o erro.
---

# Mensagens de Erro

## Acesso Negado - 403

Este retorno indica que algum parâmetro utilizado para identificar o usuário como um **token** está inválido.

```text
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Forbidden",
    "status": 403,
    "detail": "Forbidden (Invalid token)"
}
```

ID utilizado é inválido.

```text
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Forbidden",
    "status": 403,
    "detail": "Forbidden (indicator scope)"
}
```

### Requisição Inválida - 400

Este retorno indica que o corpo da requisição é inválido, algum parâmetro está incorreto ou faltando, a descrição, geralmente possui a descrição em inglês do motivo da recusa.

```text
{
    "type": "http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html",
    "title": "Bad Request",
    "status": 400,
    "detail": "Fail to start checkout, payment cannot executed when status = 'CONCLUIDO'"
}
```

### Acesso Negado - 401

Para impedir o acesso indevido dos usuários a certos recursos este retorno indica que o acesso a rota é negado pois os parâmetros fornecidos levam ao acesso de informações restritas.

