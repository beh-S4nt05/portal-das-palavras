# Publicação progressiva — commits e PRs em revisão

**Regra principal:** commits temáticos e PRs em rascunho para inspeção. **Sem merge na main, deploy, cobrança real ou release antes da validação final explícita.** Não publicar previews nem acervos críticos.

| Ordem | Branch/PR sugerido | Tema | Critério de aceite |
| --- | --- | --- | --- |
| 01 | docs/01-escopo-arquitetura | Visão, escopo, arquitetura, segurança, regras em nível de especificação | Revisão humana do conteúdo público |
| 02 | feat/02-backend-base | Base executável FastAPI, configuração sem segredos, saúde e testes | Testes unitários e inicialização controlada |
| 03 | feat/03-regras-dominio | Casos de uso, interfaces POO e lógica de domínio independente de frameworks | Regras verificadas isoladamente |
| 04 | feat/04-persistencia | PostgreSQL, persistência transacional, migrações e testes | Consistência, rollback, idempotência |
| 05 | feat/05-contratos-http | OpenAPI executável, schemas, clientes e testes de contrato | Frontend/backend compatíveis por versão |
| 06 | feat/06-integracoes | Adaptadores Gemini e SumUp em modo de testes; gerenciamento de segredos externo | Nenhuma chamada real/cobrança em CI |
| 07 | feat/07-dados-locais | Base Room, acesso offline, notas e favoritos; conteúdo somente licenciado | Integridade, migrações e teste offline |
| 08 | feat/08-frontend | Compose, seis telas, navegação, temas e acessibilidade | Compilação e testes de UI Android |
| 09 | test/09-homologacao | Segurança, integração, regressão, critérios de distribuição | Validação final do proprietário |

### Convenção de commits
`docs:`, `build:`, `feat(api):`, `feat(domain):`, `feat(data):`, `feat(android):`, `test:`, `fix:`, `chore:`.

### Contratos
O contrato HTTP deve evoluir com casos de uso, backend e DTOs do Android. Mudanças incompatíveis exigem plano de versão. Publicar documentação de API sem dados reais, sem segredos e sem assumir disponibilidade de integrações.

### Avaliação
Cada PR traz motivação, arquivos alterados, testes executados, riscos, pendências e checklist de conteúdo privado. PRs abertos são propostas, não aprovação da funcionalidade.
