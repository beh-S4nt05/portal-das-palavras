# Dados, integridade e licenças

## Banco local — Room/SQLite
Entidades conceituais: livro, capítulo, versículo, hinário, hino, autor, atribuição autoral, conteúdo editorial, favorito, anotação e versão de anotação. Separar entidades e chaves para evitar repetição; aplicar índices, FKs, unicidade e migrações. Buscar normalização até **3FN** quando aplicável.

A operação de edição de anotação deve atualizar a nota e inserir uma versão de modo transacional, sem apagar revisões históricas. Implementar exportação, política de retenção, testes de restauração e proteção de dados privados.

## Banco remoto — PostgreSQL
Entidades conceituais: identidade, conta de créditos, movimentação, geração, cota diária, pedido de compra, comprovante do provedor e auditoria. Transações e idempotência garantem que uma compra seja concedida uma única vez e que uma geração só seja debitada após validação.

**Não publicar bases SQL preenchidas, backups, registros financeiros, chaves nem parametrizações operacionais de produção.** DDL público poderá ser revisado em fase apropriada, evitando detalhes internos sensíveis.

## Bíblia e hinários
A proposta prevê uma edição bíblica em português cuja redistribuição precisa ser comprovada antes de incluir todo o texto no APK. A leitura será contínua de um capítulo para o seguinte e entre livros, desde que o conteúdo esteja disponível localmente.

| Hinário | Índices a preservar | Observação |
| --- | ---: | --- |
| Harpa Cristã | 640 | Edição de referência selecionada pelo produto; conferir correspondência editorial |
| Cantor Cristão | 581 | Respeitar número e título de cada hino |
| Hinário para o Culto Cristão | 441 hinos | Numeração original até 613, excluindo 172 leituras bíblicas |

A ficha de cada hino deve ter número, título, letra integral **quando licenciada**, compositor/autor/tradutor/adaptador quando identificados e origem/edição dos créditos. Não confundir disponibilidade em site de letras com autorização de redistribuição. Créditos de autoria não substituem licença.

## Qualidade editorial
Fontes e versões verificáveis; nunca inventar letras, hinos, autoria ou trechos bíblicos para preencher lacunas. Catálogos completos de índices não implicam catálogo completo de letras.

## Exclusões desta publicação
Textos bíblicos completos, letras de hinários, dumps, arquivos JSON de origem externa e acervos não homologados ficarão fora da primeira etapa documental. Os materiais serão avaliados e licenciados separadamente.
