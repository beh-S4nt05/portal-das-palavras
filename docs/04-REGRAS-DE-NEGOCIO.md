# Regras de negócio — versão revisável

## Inspiração gratuita
Uma nova inspiração é oferecida quando o usuário retorna em um novo dia, sem custo. No mesmo dia o resultado é preservado. Sem internet, utiliza-se conteúdo editorial local previamente aprovado. Não exigir saldo para Bíblia, hinos, favoritos ou anotações.

## Cartões e geração
- Catálogo editorial bíblico inicial: **7** itens, expansão gratuita para **14** e **21**.
- Três cartões editoriais de hinos ficam exclusivamente na Home, um por hinário.
- Geração adicional solicitada pelo usuário: **1 crédito por reflexão aprovada**, depois de esgotada a franquia aplicável.
- A IA pode produzir **reflexões**, não modificar textos bíblicos nem reproduzir letras cuja licença não tenha sido comprovada.
- Validar que o texto está em pt-BR e que referências bíblicas/temáticas são coerentes.
- Ao detectar falha, timeout ou reprovação, desfazer reserva sem cobrança. Retentativas idempotentes não cobram novamente.
- Respostas não homologadas não devem ser exibidas como se fossem conteúdo editorial validado.

## Créditos comerciais
| Pacote | Créditos | Preço fixo em reais | Total em centavos |
| --- | ---: | ---: | ---: |
| Essencial | 5 | R$ 4,50 | 450 |
| Intermediário | 15 | R$ 11,00 | 1100 |
| Ampliado | 30 | R$ 24,00 | 2400 |

Valor de **referência**: R$ 0,75 por crédito, **não aplicável automaticamente** à precificação dos pacotes. O pacote de 15 créditos é o de menor custo unitário; não prometer desconto progressivo no pacote de 30.

## Compra
SumUp Empresarial é a primeira integração planejada; PayPal é alternativa futura. Pagamento deve ser iniciado em checkout apropriado e confirmado pelo servidor antes de conceder créditos. O acesso à compra depende de regras da plataforma de distribuição, incluindo políticas Google Play quando aplicáveis.

O saldo aparece discretamente abaixo dos ícones superiores. Saldo zero + pedido de geração extra abre modal em pt-BR. Não criar aba principal de carteira.

## Identidade financeira
A compra de créditos demanda associação verificável a uma identidade e recuperação após reinstalação/troca de aparelho. O mecanismo exato será definido antes da produção. Não manter autoridade de saldo em SQLite.

## Anotações
Persistir localmente, registrar revisão ao salvar ao concluir edição ou mudar de tela; exportar dados sob ação explícita; preservar histórico e usar atualização transacional. Sem envio de textos pessoais à IA por padrão.
