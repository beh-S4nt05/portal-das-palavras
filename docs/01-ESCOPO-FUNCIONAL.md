# Escopo funcional — versão de trabalho

## Objetivo
O Portal das Palavras oferece inspiração cristã contextualizada, leitura e organização pessoal. O mural de mensagens é o foco, não uma carteira digital, um serviço de streaming ou uma rede social.

## Módulos e comportamento
| Tela | Responsabilidades |
| --- | --- |
| Início | Mensagem do dia, cinco temas, cartões com referência, reflexão e pergunta, sorteio, expansão de catálogo, ação extra de IA e três destaques de hinos |
| Bíblia | Mostrar nomes dos 66 livros sem contagem lateral de capítulos; depois selecionar capítulo e versículo |
| Hinários | Buscar por nome, título e índice; consultar cada hino |
| Leitura | Rolagem contínua de capítulos e livros, com separador discreto exibindo livro e capítulo; hinos somente com atributos autorizados |
| Favoritos | CRUD local de conteúdo favoritado |
| Anotações | CRUD privado, salvamento ao concluir edição ou trocar de tela, histórico de revisões e exportação local |

### Conteúdo editorial
- Temas de reflexão: **Esperança, Gratidão, Coragem, Paz/Descanso e Perseverança**.
- Cartões bíblicos: expansão **7 → 14 → 21**; os conteúdos adicionais, após franquia gratuita, podem utilizar IA mediante créditos.
- **Exatamente três** cartões editoriais de hinos, restritos à página inicial; não incluir reflexões na tela de detalhes do hino.
- O detalhe de hino contém apenas **número, título, letra quando juridicamente permitida e créditos autorais identificados**. Sem áudio, partitura, player ou interpretação.
- Harpa Cristã: **640** números na edição de referência a validar; Cantor Cristão: **581**; HCC: **441 hinos** dentre 613 entradas numeradas — as 172 leituras bíblicas não são músicas.

### Renovação diária
- A inspiração do dia deve ser renovada na abertura/retorno em outro dia sem custo de créditos.
- Reabrir no mesmo dia não deve ocasionar nova geração nem cobrança.
- Offline ou indisponibilidade do provedor exige mensagem válida do acervo local e manutenção do acesso.
- A política de identificação da data e prevenção a abuso será definida no backend, sem comprometer a leitura offline.

### Privacidade e idioma
Toda interação e conteúdo apresentado devem estar em **pt-BR**; resultados externos em outros idiomas são traduzidos ou substituídos por conteúdo local antes de aparecer. Anotações ficam no dispositivo na V1, sem envio automático às LLMs.

### Fora de escopo da V1
Áudios, partituras, streaming, feed social, geração de letras por IA, publicação de conteúdo protegido sem autorização, modo web/iOS, cobrança direta dentro do dispositivo e sincronização remota padrão de anotações.

## Critérios mínimos
- Nenhuma tela bloqueia conteúdo local devido a falta de rede.
- A tela Leitura começa no versículo escolhido e avança sem intervenção, com marcadores de capítulo/livro.
- Texto e rótulos seguem pt-BR, inclusive erros, acessibilidade e preços.
- Nunca debitar crédito por atualização diária ou por falha de geração.
- Não divulgar hinos protegidos integralmente sem licença aplicável.
- UI e regras permanecem revisáveis até homologação final.
