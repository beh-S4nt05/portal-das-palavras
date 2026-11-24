# UI/UX — diretrizes públicas

## Identidade
Nome oficial: **Portal das Palavras**. Paleta proposta com verde-petróleo (`#24545E`), verde-sálvia (`#526E62`), dourado discreto (`#916118`), fundo papel (`#F7F5EF`), superfície (`#FFFEFA`) e texto (`#1B2B2F`). Tema inicial **claro**; o usuário poderá selecionar tema escuro ou automático depois.

A marca, splash e ícone próprios continuam sujeitos à aprovação visual definitiva. Não publicar previews de trabalho.

## Tipografia e medidas
Roboto para interface; conteúdo de leitura inicial aproximadamente 18sp, ajustável. Escalas de espaçamento de 4, 8, 12, 16, 24, 32 e 48dp. Cantos de componentes entre 8 e 24dp conforme função. Alvos de toque com pelo menos 48dp, evitando cortes em fontes ampliadas.

## Layout adaptativo
Usar `WindowSizeClass` e espaço **real da janela**, não nomes de aparelhos: compacta abaixo de 600dp; média de 600 a 839dp; expandida a partir de 840dp; larguras de 1200 e 1600dp como ajustes adicionais quando fizer sentido. Em geral, celular usa navegação inferior; tablet pode usar navegação lateral. Não assumir orientação ou altura fixa.

## Fluxos e pontos de atenção
- Seis telas conceituais: Início, Bíblia, Hinários, Leitura, Favoritos, Anotações. Leitura é destino contextual, não precisa ocupar uma sexta posição permanente na barra.
- Lista de livros bíblicos: nomes apenas, sem contagens laterais.
- Após selecionar livro, ocultar lista de livros e abrir capítulos; depois versículos; após escolha, iniciar leitura contínua.
- Separadores de novos capítulos/livros simples e discretos.
- Hinos: apenas consulta de número/título/letra e créditos, sem reflexões na ficha.
- Créditos: posição discreta abaixo dos ícones de sair/mais opções; abrir modal de compra somente se solicitar geração extra sem saldo.
- O ícone de saída não pressupõe autenticação já implementada.

## pt-BR obrigatório
Interface, conteúdo editorial, mensagens de IA, conselhos externos, datas, erros, títulos de ações e descrições TalkBack serão em pt-BR. Traduzir ou trocar mensagens externas em outros idiomas antes da exibição. Não exibir erros técnicos crus.

## Estados mínimos e testes
Normal, carregando, vazio, offline, erro recuperável e retorno de operação. Validar tamanhos de janela de 320, 360, 393, 412, 600 e 840dp, fonte ampliada, TalkBack, rotação, contraste e ausência de sobreposição.
