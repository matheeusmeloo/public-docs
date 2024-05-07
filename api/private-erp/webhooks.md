---
description: Notificação de eventos através de webhooks.
---

# Webhooks

Webhooks também conhecidos como HTTP Callbacks são uma forma de se registrar para receber informações úteis em uma URL específica de sua escolha.

Quando ocorre uma alteração no estado de um recurso dentro da plataforma GO, por exemplo, uma transação é criada, um evento é gerado por essa ocorrência e enviado para o webhooks cadastrado.

Para utilizar a notificação de eventos por webhooks você precisa: enviar um e-mail para suporte@gestao-online.com solicitando que seja configurado a URL que você deseja receber as notificações.

O sistema sempre enviará uma request POST com o corpo em JSON com o formato a seguir (de cada evento), sugerimos que na URL tenha algum token de validação de segurança (via query string) e/ou que seja validado por IP de origem.

## Eventos
### Compra realizada
É disparado quando uma compra é realizada

**Payload**

```json
{
    "event_id": "ORDER_CREATED",
    "data": {
	 "id": "100",
   	 "code": "0000593098",
   	 "utmId": "01407b89-b25d-4cac-a576-014158bb17a5",
   	 "date": {
   		 "date": "2021-03-02 21:02:53.000000",
   		 "timezone_type": 3,
   		 "timezone": "UTC"
   	 },
   	 "status": 1,
   	 "user": {
   		 "id": 2,
   		 "document": "123421341234",
   		 "name": "teste",
   		 "email": "teste@teste.com",
   		 "phone": null,
   		 "cellphone": "123423434"
   	 }
    }
}
```

### Compra cancelada
É disparado quando uma compra é cancelada

**Payload**

```json
{
    "event_id": "ORDER_CANCEL",
    "data": {
	 "id": "100",
   	 "code": "0000593098",
   	 "utmId": "01407b89-b25d-4cac-a576-014158bb17a5",
   	 "date": {
   		 "date": "2021-03-02 21:02:53.000000",
   		 "timezone_type": 3,
   		 "timezone": "UTC"
   	 },
   	 "status": 1,
   	 "user": {
   		 "id": 2,
   		 "document": "123421341234",
   		 "name": "teste",
   		 "email": "teste@teste.com",
   		 "phone": null,
   		 "cellphone": "123423434"
   	 }
    }
}
```

### Alteração de status de nota fiscal
É disparado quando acontece uma alteração do status da nota fiscal

**Payload**

```json
{
    "event_id": "TAX_INVOICE_CHANGE_STATUS",
    "data": {
	 "id": "100",
   	 "code": "0000593098",
   	 "utmId": "01407b89-b25d-4cac-a576-014158bb17a5",
   	 "date": {
   		 "date": "2021-03-02 21:02:53.000000",
   		 "timezone_type": 3,
   		 "timezone": "UTC"
   	 },
   	 "status": 1,
   	 "user": {
   		 "id": 2,
   		 "document": "123421341234",
   		 "name": "teste",
   		 "email": "teste@teste.com",
   		 "phone": null,
   		 "cellphone": "123423434"
   	 }
    }
}
```

### Baixa de pagamento financeiro
É disparado quando acontece a baixa do pagamento no financeiro

**Payload**

```json
{
    "event_id": "FINANCIAL_PAYMENT_DISCHARGE",
    "data": {
	 "id": "100",
   	 "code": "0000593098",
   	 "utmId": "01407b89-b25d-4cac-a576-014158bb17a5",
   	 "date": {
   		 "date": "2021-03-02 21:02:53.000000",
   		 "timezone_type": 3,
   		 "timezone": "UTC"
   	 },
   	 "status": 1,
   	 "user": {
   		 "id": 2,
   		 "document": "123421341234",
   		 "name": "teste",
   		 "email": "teste@teste.com",
   		 "phone": null,
   		 "cellphone": "123423434"
   	 }
    }
}
```

### Alteração de status pagamento financeiro
É disparado quando acontece uma alteração na situação do financeiro

**Payload**

```json
{
    "event_id": "FINANCIAL_PAYMENT_STATUS",
    "data": {
	 "id": "100",
   	 "code": "0000593098",
   	 "utmId": "01407b89-b25d-4cac-a576-014158bb17a5",
   	 "date": {
   		 "date": "2021-03-02 21:02:53.000000",
   		 "timezone_type": 3,
   		 "timezone": "UTC"
   	 },
   	 "status": 1,
   	 "user": {
   		 "id": 2,
   		 "document": "123421341234",
   		 "name": "teste",
   		 "email": "teste@teste.com",
   		 "phone": null,
   		 "cellphone": "123423434"
   	 }
    }
}

{
    "event_id": "FINANCIAL_PAYMENT_DISCHARGE",
    "data": {
	 "id": "100",
   	 "code": "0000593098",
   	 "utmId": "01407b89-b25d-4cac-a576-014158bb17a5",
   	 "date": {
   		 "date": "2021-03-02 21:02:53.000000",
   		 "timezone_type": 3,
   		 "timezone": "UTC"
   	 },
   	 "status": 1,
   	 "user": {
   		 "id": 2,
   		 "document": "123421341234",
   		 "name": "teste",
   		 "email": "teste@teste.com",
   		 "phone": null,
   		 "cellphone": "123423434"
   	 }
    }
}

```

### Alteração de status de entrega
É disparado quando acontece uma alteração na situação de entrega de uma venda

**Payload**

```json
{
    "event_id": "ORDER_DELIVERY_CHANGE_STATUS",
    "data": {
	 "id": "100",
   	 "code": "0000593098",
   	 "utmId": "01407b89-b25d-4cac-a576-014158bb17a5",
   	 "date": {
   		 "date": "2021-03-02 21:02:53.000000",
   		 "timezone_type": 3,
   		 "timezone": "UTC"
   	 },
   	 "status": 1,
   	 "user": {
   		 "id": 2,
   		 "document": "123421341234",
   		 "name": "teste",
   		 "email": "teste@teste.com",
   		 "phone": null,
   		 "cellphone": "123423434"
   	 }
    }
}
```