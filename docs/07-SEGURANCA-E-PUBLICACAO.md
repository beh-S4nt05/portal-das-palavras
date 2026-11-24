# Segurança, privacidade e política de publicação

Este repositório é **público**. Somente artefatos revisados para publicação podem ser adicionados.

## Nunca versionar
- Chaves e tokens de Gemini, SumUp, PayPal, assinaturas de webhook, contas de serviço, senhas ou arquivos de ambiente reais.
- Dados identificáveis de usuários, anotações, conteúdo privado e informações pessoais/financeiras.
- Dumps e bancos preenchidos, backups, relatórios internos de incidentes, segredos antifraude, prompts privados e recursos proprietários sensíveis.
- Pacotes ZIP, previews HTML, screenshots/capturas de trabalho e assets privados.
- Letras ou textos de terceiros sem permissão de republicação.

## Controles de arquitetura
- Chaves das LLMs e dos meios de pagamento somente no backend e em gerenciador de segredos.
- Validar autenticação e autorização no servidor; não confiar em saldo ou preço enviado pelo Android.
- Usar HTTPS, validação de payload e resposta, limites de uso, logging sem segredos e trilha de auditoria.
- Gerenciar operações financeiras com transação e idempotência; tratar webhooks como notificações a confirmar pelo provedor.
- Geração diária nunca debita saldo; falhas e retentativas não geram cobranças duplicadas.
- Anotações permanecem locais e não são compartilhadas com IA por padrão.
- Credenciais de teste e ambientes reais separados; pagamentos reais bloqueados até homologação.

## Licenciamento de conteúdo
A licença MIT existente cobre código próprio, não conteúdos de terceiros. Conferir individualmente versões e direitos de letras, traduções, edições e texto bíblico antes de qualquer distribuição.

## Antes de merge e release
Revisar diff completo e histórico, rodar detector de segredos, verificar licenças, validar contratos, executar testes e obter aprovação expressa do proprietário. Nenhuma PR desta fase deve ser mesclada automaticamente.

## Acesso e manutenção
Definir proteção de branch, regras de revisão e CI em fase posterior, sem presumir que estão configurados. Incidentes e falhas de segurança devem ser reportados por canal privado apropriado, sem divulgar credenciais.
