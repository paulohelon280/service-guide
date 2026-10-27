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

A primeira solicitação real de recuperação foi aceita em **26/10/2026 às
21:14**, America/Sao_Paulo (`2026-10-27T00:14:31Z`). Houve novo aceite após a
transferência da organização, para as duas contas existentes autorizadas.
O log Auth confirmou `/recover` com HTTP 200. Aceite pelo serviço não equivale
a entrega comprovada na caixa de entrada.

**Atualização de 27/10/2026:** o responsável mostrou uma captura do teste
simples, sem links, recebido na caixa de entrada do Gmail do titular e
enviado por essa mesma conta. Isso comprova a entrega do teste SMTP direto.
O recebimento do e-mail **“Redefina sua senha — Service Guide”**, gerado pelo
Supabase Auth, ainda precisa de confirmação própria.

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

Nenhum deploy, migration ou troca de plano foi executado nesta etapa.
A organização Supabase foi transferida em operação separada, após confirmação
humana, e conferida no painel e na API. O site continua no Cloudflare e no
mesmo projeto Supabase. A troca do SMTP, por si só, não transfere o banco.

## Pendências da entrega

- Confirmar recebimento do e-mail de recuperação do Auth; o teste simples
  do SMTP já foi confirmado pela captura do responsável.
- Entregar o pacote privado e suas chaves separadas ao novo responsável.
- Exercitar os fluxos reais do titular antes do aceite operacional.

Recibos técnicos locais, sem senhas, permanecem em `.wrangler/` e não são
publicados com credenciais. A conferência do banco encontrou 43 tabelas
públicas com RLS, 15 migrações, três contas Auth e catálogo de empresas vazio.
O recibo atual é `evidencias/entrega-titular-2026-10-27.json`; o recibo SMTP
de 26/10 registra o primeiro ensaio e seu estado naquele momento.
