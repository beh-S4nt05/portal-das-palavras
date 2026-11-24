# Arquitetura — visão técnica pública

## Diretrizes
Aplicar orientação a objetos com composição, interfaces de repositório, SOLID, separação de responsabilidades, Clean Architecture e fluxo unidirecional de estado. Implementação modular e testável.

## Android
| Camada | Componentes | Dever |
| --- | --- | --- |
| Apresentação | Compose, Material 3, Navigation, ViewModel, StateFlow | Renderização, navegação e estados de carregamento, erro, vazio e offline |
| Domínio | Entidades, interfaces, casos de uso, validações | Regras independentes de Android e banco |
| Dados | Room, DAO, repositórios, Retrofit, mapeadores | Persistir dados locais, orquestrar chamadas HTTPS e cache |
| Injeção | Hilt | Fornecer dependências por contratos e escopos |

A Home usa inspiração diária e cartões; Bíblia e hinários leem índices e conteúdo permitido de uma base instalada; favoritos e anotações mantêm suas alterações localmente.

## Backend
| Módulo | Dever |
| --- | --- |
| API | Autenticar, validar dados, versionar contratos e responder erros padronizados |
| Geração | Produzir reflexões em pt-BR, validar referência, qualidade e limite de uso |
| Cota diária | Entregar renovação gratuita idempotente e alternativa de conteúdo |
| Créditos | Consultar saldo, reservar/debitar após sucesso e recuperar falhas sem duplicidade |
| Pagamentos | Criar ordem de checkout e confirmar estado do provedor antes de creditar |
| Persistência | Transações em PostgreSQL, integridade referencial e auditoria |
| Integrações | Gemini/Google AI Studio e SumUp via adaptadores substituíveis |

**A chave Gemini e as credenciais SumUp/PayPal não pertencem ao aplicativo Android.** Os serviços externos são chamados por um backend autenticado.

## Dependências e contratos
O domínio define interfaces. Implementações concretas dependem desses contratos. As mudanças de contrato afetam OpenAPI, cliente Retrofit, testes e eventual migração.

## Ambiente
Configuração por variáveis de ambiente e armazenamento seguro de segredos. Desenvolvimento e produção isolados, com provedores simulados em testes. Não presumir que a presença de templates implica serviço em funcionamento.

## Validação necessária
Compilação Gradle em Android SDK, migrações Room, testes unitários e de integração, testes HTTP de contrato, testes de concorrência de créditos, acessibilidade e regressão nas seis telas.
