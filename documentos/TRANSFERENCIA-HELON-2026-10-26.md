# Transferência do Service Guide ao titular

Estado medido em 26/10/2026. Cada item abaixo tem validação independente.
Esta documentação não declara concluída a transferência de todos os serviços.

## Código: copiado e conferido

O responsável solicitou que o projeto passe ao GitHub do titular:
**https://github.com/paulohelon280/service-guide**. O proprietário confirmado
pela API é `paulohelon280`.

Após liberação de escrita, o destino vazio recebeu, sem force-push, as seis
branches publicadas de `GarciaCarlos1985/service`. Os identificadores de todas
as branches foram comparados após o envio. A `main` de origem copiada é
`7527bbeea54d7f8eaf1df8d9a15cd5cc458d698b`; alterações posteriores de
documentação registram a nova titularidade do código.

Foram copiadas somente três variáveis públicas de Actions:
`VITE_SUPABASE_URL`, `VITE_SUPABASE_ANON_KEY` e `VITE_TURNSTILE_SITE_KEY`.
Tokens, senhas, `.env.local`, dados do banco e assinatura privada não foram
enviados ao GitHub.

O repositório de origem foi preservado. PRs, issues e execuções antigas de
Actions permanecem lá; um push Git não transfere esses metadados. Os workflows
copiados validam código/Android e não publicam automaticamente em produção.

## Supabase: destino validado, transferência pendente

O site publicado utiliza o projeto existente `taabjnmsaaltsiehywbw`.
A organização de destino foi conferida no painel: `paulohelon280's Org`,
com Helon como Owner e o responsável técnico como Developer.

A pré-validação do painel aceitou esse destino. O projeto atual é gerenciado
pelo Vercel Marketplace; a transferência remove o vínculo de armazenamento
da Vercel. A aplicação publicada usa Cloudflare Workers.

O caminho aprovado é transferir o projeto atual, preservando banco, Auth,
RLS e Storage. Não trocar apenas a URL pelo projeto antigo do titular:
isso seria outra migração e não transfere dados ou contas.

Antes da execução, substituir o SMTP pessoal do desenvolvedor pelo SMTP do
titular e testar a entrega. Depois da transferência, conferir propriedade,
referência do projeto, permissões, Auth, Storage e disponibilidade do site.
Nenhum plano pago, exclusão de projeto ou migração de schema foi executado
nesta preparação.

## Backup e assinatura: preparados localmente

Foi gerado um dump PostgreSQL criptografado com AES-256-GCM, usando conexão
TLS validada. A integridade criptográfica e a leitura do índice do arquivo
passaram, incluindo Auth, tabelas comerciais, RPCs, migrations e políticas.
Não foi realizado um ensaio de restauração em outro banco.

Código e histórico publicados também têm cópia local verificável.
O material de assinatura Android foi exportado para um formato privado e
portátil; a descriptografia e a senha recuperada foram conferidas com keytool,
preservando o certificado associado ao domínio. Entregar esses arquivos e
suas chaves por canal privado, separados do repositório público.

O arquivo DPAPI original depende do usuário Windows que o criou e não basta
para entregar a assinatura a outro profissional. Nenhuma credencial pessoal
de GitHub, Supabase ou Gmail deve ser repassada com o projeto.

## Hospedagem e automações

Cloudflare e Turnstile foram conferidos na conta do titular. O endereço público
continua `https://service-guide.helon280.workers.dev`. A transferência do código
não alterou o Worker nem executou deploy.

Na conferência do Service Guide, o banco não tinha `pg_cron` instalado, o Worker
não tinha cron configurado e os workflows do repositório não continham agendamento
de notícias ou keepalive. Nenhuma rotina externa foi desativada ou teve seus
tokens revogados. Um agendador externo não identificado não deve ser tratado
como comprovado ou removido durante o encerramento.

## Conferência de encerramento

- Comprovar que o titular controla GitHub, organização Supabase e Cloudflare.
- Testar o SMTP do titular, preservando confirmação de e-mail e CAPTCHA.
- Validar login novo, recuperação, painel, cadastro/edição, logotipo, horários
  e desativação/reativação pelo fluxo real do titular.
- Conferir o CI do novo repositório e registrar o resultado.
- Entregar os materiais privados e instruções de recuperação ao novo responsável.
- Somente após aceite, retirar acessos temporários específicos do Service Guide;
  preservar contas, tokens e automações que atendam outros projetos.

Fontes oficiais para a operação:

- https://docs.github.com/en/repositories/creating-and-managing-repositories/duplicating-a-repository
- https://supabase.com/docs/guides/platform/project-transfer
- https://supabase.com/kb/troubleshooting/error-target-organization-is-not-managed-by-vercel-marketplace-during-project-transfer
