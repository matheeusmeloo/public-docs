# Login

Plugins adicionais na versão 2 do gitbook não funcionam.

Nesta rota é possível realizar o login de acesso ao sistema.

**Rota**: *baseUrl/oauth*

**Corpo da requisição:**
```
{
  "grant_type": "password",
  "client_id": "app",
  "client_secret": "",
  "username": "user",
  "password": "sua_senha"
}
```

{% codetab Python %}
```python
print("Hello, world!")
```
{% endcodetab %}

## Cabeçalho

- Content-Type: application/json
- Origin: {{origin}}
