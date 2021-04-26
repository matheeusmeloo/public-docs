# Registro de novos usuários

O registro de novos usuários é feito de forma convencional, seguindo padrões de segurança com a geração e armazenagem de HASHES apartir das senhas enviadas.

Por padrão cada domínio é criado com 1 usuário superadmin assim é possível adicionar novos usuários iniciando novos processos de registro.

OBS: **Utilizamos o CPF como padrão não oficial para o `username` de novos usuários registrados**

## Fluxo de registro

* Usuário superadmin padrão do sistema.
* O usuário padrão adiciona novos usuários.
* O usuário adicionado verifica seu email e confirma seu registro.
* Ao confirmar seu registro o usuário pode então criar sua senha.

