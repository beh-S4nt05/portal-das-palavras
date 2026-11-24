# Contratos entre backend e frontend — especificação preliminar

**Fase:** desenho público, ainda revisável. A definição executável OpenAPI e os DTOs Kotlin/Python serão introduzidos em fase técnica independente, com testes de conformidade.

## Convenções
- Base sugerida: `/v1` sobre **HTTPS**, JSON UTF-8.
- Autorização Bearer para operações associadas a identidade verificada, sujeita ao fluxo de autenticação definitivo.
- `Idempotency-Key` nas operações sujeitas a repetição de rede ou que movimentam créditos.
- O cliente **não informa saldo final, preço efetivo nem conta recebedora**; esses valores são determinados e validados no backend.
- Erros retornam códigos estáveis e mensagens localizáveis. O cliente não exibe exceções ou mensagens não traduzidas de terceiros.

## Contratos propostos
| Método | Caminho | Resposta/efeito | Consome créditos? |
| --- | --- | --- | --- |
| POST | `/v1/daily/refresh` | Inspiração diária do usuário, idempotente por dia | Não |
| GET | `/v1/wallet` | Saldo validado no servidor | Não |
| GET | `/v1/wallet/transactions` | Histórico paginado de movimentações | Não |
| POST | `/v1/generations/extra` | Inicia geração, identificador e estado | Após sucesso |
| GET | `/v1/generations/{id}` | Estado PENDING/SUCCEEDED/FAILED e resultado quando válido | Não duplica |
| GET | `/v1/purchases/packages` | Pacotes e preços oficiais, sempre fornecidos pelo servidor | Não |
| POST | `/v1/purchases/verify` | Valida compra confirmada pelo provedor antes de conceder créditos | Crédito concedido uma vez |

Valores monetários são transmitidos em **centavos inteiros** (BRL), nunca como float. Estados financeiros exigem transações e rastreabilidade.

## Exemplo de erro sem saldo
```json
{
  "code": "INSUFFICIENT_CREDITS",
  "message": "Você não possui créditos suficientes.",
  "request_id": "exemplo"
}
```
O Android associa `INSUFFICIENT_CREDITS` à abertura do modal contextual de pacotes. Erro do provedor, timeout e resposta rejeitada não geram débito.

## Operações sem HTTP obrigatório
Leitura bíblica offline, índice de hinários e letras liberadas, CRUD de favoritos e anotações são resolvidos localmente. Persistência local **não** concede saldo financeiro oficial.

## Versionamento
Para cada mudança de campo, enum ou regra, criar atualização coordenada do contrato, modelos de frontend/backend, testes e documentação. Mudanças incompatíveis exigem versão de API ou migração controlada.
