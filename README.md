# Portal das Palavras

Aplicativo Android de inspiração cristã, reflexões contextualizadas, leitura bíblica contínua, consulta a hinários, favoritos e anotações locais.

> **Estado: em desenvolvimento e revisão.** Esta branch contém exclusivamente especificações públicas. Não representa aplicativo concluído, backend implantado, pagamentos ativos nem aprovação final. A branch principal não recebe alterações sem revisão.

## Proposta central
O **mural de inspiração** é a função principal. Bíblia, hinários, leitura, favoritos e anotações oferecem consulta e organização. Toda a experiência visível será em português brasileiro (**pt-BR**), com início em tema claro e opção posterior de alterar o tema.

## Seis telas
1. **Início:** inspiração diária gratuita, temas, progressão de cartões bíblicos e três destaques editoriais de hinos.
2. **Bíblia:** seleção de livro, capítulo e versículo, seguida de leitura contínua.
3. **Hinários:** Harpa Cristã, Cantor Cristão e Hinário para o Culto Cristão.
4. **Leitura:** conteúdo bíblico contínuo e leitura individual autorizada dos hinos.
5. **Favoritos:** conteúdos marcados e acessíveis offline.
6. **Anotações:** textos privados, versões, exportação e salvamento automático local.

## Arquitetura prevista
- Android: **Kotlin**, **Jetpack Compose**, **Material 3**, **MVVM**, **Clean Architecture**, **Room/SQLite**, **Retrofit**, **Coroutines/Flow** e **Hilt**.
- Backend: **Python/FastAPI**, **OpenAPI**, **PostgreSQL** e integrações de IA/pagamento exclusivamente pelo servidor.
- Comunicação: **HTTPS/REST**, contratos versionados, autenticação quando necessária, idempotência e erros padronizados.
- Biblioteca e anotações offline permanecem utilizáveis sem backend.

## Ordem de desenvolvimento
**Documentação → Backend → Regras de negócio → Persistência e contratos → Integrações Gemini e SumUp → Frontend Android → Testes e revisão final.**

**Sem prévias publicadas:** capturas, protótipos HTML, pacotes ZIP, dados sensíveis, chaves, bancos preenchidos e letras sem licença não fazem parte deste repositório.

## Documentação
- [Visão funcional e critérios de produto](docs/01-ESCOPO-FUNCIONAL.md)
- [Arquitetura e responsabilidades](docs/02-ARQUITETURA.md)
- [Comunicação entre frontend e backend](docs/03-CONTRATOS-HTTP.md)
- [Regras de negócio e economia de créditos](docs/04-REGRAS-DE-NEGOCIO.md)
- [Persistência e conteúdo](docs/05-DADOS-E-LICENCAS.md)
- [Design, navegação e acessibilidade](docs/06-DESIGN-SYSTEM.md)
- [Segurança e proteção de publicação](docs/07-SEGURANCA-E-PUBLICACAO.md)
- [Sequência de commits, PRs e validação](docs/08-PLANO-DE-FASES.md)
- [Decisões vigentes e pontos abertos](docs/09-DECISOES-E-PENDENCIAS.md)

## Licença
O **código próprio do projeto** segue a licença existente no repositório. Conteúdos de terceiros (versões bíblicas, letras, traduções e materiais editoriais) possuem direitos próprios e **não são automaticamente licenciados pela licença do software**.
