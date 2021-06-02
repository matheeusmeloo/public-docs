# Códigos de Erro



**Mensagens de erro**

Quando uma requisição de API falha, a Zoop retornará um código de resposta HTTP 4xx ou 5xx que identifica genericamente a falha, bem como uma resposta JSON que fornece informações mais específicas sobre o erro \(ou os erros\) que causou a falha.

A resposta conterá:

* O status e o status\_code.
* O tipo e a categoria que você pode usar para programar as respostas aos erros.
* Uma mensagem legível para humanos que explica por que o erro ocorreu.
* Os valores possíveis para o parâmetro de tipo estão listados abaixo:

| Status Code | Tipo | Categoria | Descrição | Código de erro Bandeira |
| :--- | :--- | :--- | :--- | :--- |
| 500 | processing\_error | server\_api\_error | Ocorreu um erro de processamento na Zoop. Se você receber esta mensagem, entre em contato com api@pagzoop.com |  |
| 409 | invalid\_request\_error | duplicate\_taxpayer\_id | Customer with this taxpayer\_id already exists. |  |
| 408 | invalid\_request\_error | service\_request\_timeout | Credit card process is temporarily unavailable at the specified location. |  |
| 404 | invalid\_request\_error | endpoint\_not\_found | The requested URL was not found on the server |  |
| 401 | invalid\_request\_error | authentication\_failed | The API Key provided has expired or has been deleted. |  |
| 401 | invalid\_request\_error | expired\_security\_key | This API call cannot be made with a publishable API key. |  |
| 401 | invalid\_request\_error | invalid\_key\_for\_api\_call | The minimum amount is $0.50 \(or equivalent in country currency\). The amount must be a positive integer in cents representing how much to charge, e.g 1260 for $12.60. |  |
| 400 | invalid\_request\_error | transaction\_amount\_error | The minimum amount is $0.50 \(or equivalent in country currency\). The amount must be a positive integer in cents representing how much to charge, e.g 1260 for $12.60. |  |
| 400 | invalid\_request\_error | transfer\_amount\_error | The minimum transfer amount is $1.00 \(or equivalent in country currency\). The amount must be a positive integer in cents representing how much to charge, e.g 1260 for $12.60. |  |
| 400 | invalid\_request\_error | missing\_required\_param | Missing required parameter\(s\). Please verify request parameters. |  |
| 400 | invalid\_request\_error | unsupported\_payment\_type | Invalid request: unsupported payment type. |  |
| 400 | invalid\_request\_error | invalid\_payment\_information | Invalid payment information. Please verify request parameters. |  |
| 400 | invalid\_request\_error | invalid\_parameter | Invalid parameter\(s\). Your parameter value is incorrect. Please verify request parameters. |  |
| 402 | file\_upload | file\_size\_too\_large |  |  |
| 402 | invalid\_request\_error | insufficient\_escrow\_funds\_error | Requested transfer exceeds remaining settled funds in escrow. |  |
| 402 | invalid\_request\_error | capture\_transaction\_error | The capture request failed. Transaction could not be captured. |  |
| 402 | invalid\_request\_error | no\_action\_taken | No action taken. Unable to back out prior transaction |  |
| 402 | invalid\_request\_error | seller\_authorization\_refused | Seller has not been authorized to charge credit cards. Complete activation to start processing payments. |  |
| 402 | invalid\_request\_error | void\_transaction\_error | The void request failed. Transaction could not be voided. |  |
| 402 | card\_error | invalid\_expiry\_month | Invalid expiry month value. Please verify request parameters. |  |
| 402 | card\_error | invalid\_expiry\_year | Invalid expiry year value. Please verify request parameters. |  |
| 402 | card\_error | card\_customer\_not\_associated | Transaction denied. No active card. |  |
| 402 | card\_error | insufficient\_funds\_error | Requested credit exceeds remaining settled funds. | 51 |
| 402 | card\_error | expired\_card\_error | The credit card has expired. | 33 |
| 402 | card\_error | invalid\_card\_number | The card number is not a valid credit card number. | 15 |
| 402 | card\_error | invalid\_pin\_code | Transaction denied. Invalid PIN code. | 55 |
| 402 | card\_error | authorization\_refused | Transação ilegal | 58 |

