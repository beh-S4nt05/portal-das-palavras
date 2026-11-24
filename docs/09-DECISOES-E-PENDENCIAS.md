# Decisões consolidadas e pendências

**Todas as decisões podem ser revisadas antes da homologação.** Em caso de conflito, os requisitos mais recentes aprovados em conversa prevalecem sobre os documentos de protótipos anteriores.

| Código | Definição de trabalho |
| --- | --- |
| PROD-01 | Portal das Palavras, Android nativo, seis telas; mural de inspiração é o objetivo principal |
| L10N-01 | Experiência integralmente pt-BR |
| UI-01 | Verde-petróleo e sálvia; tema inicial claro; futuro seletor de temas |
| UI-02 | Bíblia: livros sem contagem lateral; livro → capítulo → versículo → leitura contínua |
| UI-03 | Créditos discretos no cabeçalho, modal contextual quando não houver saldo para geração extra |
| HINO-01 | Harpa 640, Cantor 581, HCC 441 hinos; letras e autoria condicionadas à revisão e direitos |
| CARD-01 | Cartões bíblicos 7 → 14 → 21; três editoriais de hinos somente na Home |
| NOTE-01 | Notas locais, autosalvamento em saída/conclusão, versionamento e exportação |
| IA-01 | Integração Gemini pelo backend e geração de reflexões em pt-BR; revisão editorial e cotas |
| IA-02 | Nova inspiração em outro dia sempre gratuita; extra custa 1 crédito após sucesso |
| PAY-01 | Pacotes fixos: 5 por R$ 4,50; 15 por R$ 11,00; 30 por R$ 24,00; referência unitária R$ 0,75 |
| PAY-02 | SumUp como primeiro meio pretendido; PayPal como alternativa futura |
| DATA-01 | Room/SQLite offline; PostgreSQL para recursos financeiros remotos |
| RELEASE-01 | Primeiro documentação, depois backend/domínio/contratos/dados/integrações e frontend por último; validação final antes de merge |

## Pendências sem confirmação
- Fonte bíblica redistribuível e termo de licenciamento do texto integral.
- Verificação individual dos autores, traduções, edições e licenças dos hinos.
- Estratégia final de autenticação e recuperação de créditos entre aparelhos.
- Cadastro e credenciais do Google AI Studio, cotas/modelo Gemini e qualidade editorial.
- Habilitação SumUp, modalidade de checkout, política de reembolso e condições Google Play.
- Versão mínima Android, infraestrutura de implantação, métricas e política de privacidade.
- Design final do logotipo, ícone e splash.
- Contratos OpenAPI executáveis e critérios de testes finais a serem implementados em fases próprias.

## Limitações conhecidas
Artefatos anteriores locais incluíam protótipos HTML, contratos de referência e catálogos de índices; isso não prova compilação Android, aprovação de letras, conexão ativa de IA ou pagamentos reais. Evitar afirmações de produção antes de evidências verificáveis.
