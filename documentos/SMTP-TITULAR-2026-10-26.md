# SMTP do titular — 26/10/2026

## Resultado medido

O SMTP Gmail do titular foi configurado no projeto Supabase existente
`taabjnmsaaltsiehywbw`. A senha foi lida somente do arquivo local ignorado pelo
Git; não foi publicada no código, no Worker, no relatório ou na conversa.

Os testes da credencial atual passaram:

- Conexão SMTP com STARTTLS e validação de certificado.
- Autenticação na conta Gmail do titular com a senha de aplicativo fornecida.
- Atualização da configuração Auth pela Management API, preservando Site URL,
  retornos, política de senha e rotação de sessão.
- Solicitação real de recuperação pelo Supabase Auth para a conta existente
  do titular, aceita sem erro de envio.
- Recusa de uma solicitação pública sem CAPTCHA válido.
- Confirmação de e-mail e Turnstile preservados na configuração.

A solicitação real de recuperação foi aceita em **26/10/2026 às 21:14**,
America/Sao_Paulo (`2026-10-27T00:14:31Z`). O destinatário foi convidado a
confirmar o recebimento. Aceite pelo serviço não equivale a entrega comprovada
na caixa de entrada; esse último item segue pendente.

## Escopo do teste

A solicitação positiva usou um backend administrativo autorizado. A chave
administrativa foi obtida apenas em memória, conferida para o projeto e não
foi salva, exibida ou enviada ao navegador. O teste público sem prova válida
continuou recusado pelo CAPTCHA. Não houve criação de usuário ou alteração
de senha de acesso ao site. O link de recuperação enviado permanece privado.

A comparação literal entre a senha local e o campo protegido retornado pela
Management API não foi usada como comprovação do funcionamento. A evidência
positiva foi a autenticação SMTP e a solicitação real de recuperação aceita
pelo Auth, em conjunto com a configuração aplicada.

Nenhum deploy, migration, troca de plano ou transferência de organização foi
executado nesta etapa. O site continua no Cloudflare e no mesmo projeto
Supabase. A troca do SMTP não transfere a propriedade do banco.

## Pendências da entrega

- Confirmar recebimento do e-mail na caixa de entrada do titular.
- Retomar a sessão da conta proprietária de origem e executar a transferência
  para a organização do titular, com a confirmação exigida no painel.
- Validar a propriedade e os serviços após a transferência e atualizar o
  pacote privado antes da entrega final.

Recibos técnicos locais, sem senhas, permanecem em `.wrangler/` e não são
publicados com credenciais. A conferência do banco encontrou 43 tabelas
públicas com RLS, 15 migrações, três contas Auth e catálogo de empresas vazio.
