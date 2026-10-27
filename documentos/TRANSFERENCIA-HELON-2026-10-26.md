# Transferência do Service Guide ao titular

Estado atualizado em 27/10/2026. GitHub, Supabase e Cloudflare estão sob
controle do titular. Cada item abaixo tem validação independente; a entrega
dos arquivos privados e o aceite operacional continuam com status próprios.

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

## Supabase: transferência concluída e conferida

O projeto existente `taabjnmsaaltsiehywbw` foi transferido, após confirmação
humana no momento da operação, para `paulohelon280's Org`
(`rundjmvpowpppnozqtso`). O painel confirmou Helon como Owner e o responsável
técnico como Developer. A Management API confirmou a organização de destino
e o estado `ACTIVE_HEALTHY` novamente em 27/10/2026.

A operação nativa removeu o vínculo de armazenamento do Vercel Marketplace.
A aplicação publicada continua no Cloudflare Workers, no mesmo endereço.

Foi preservado o projeto atual, com banco, Auth, RLS e Storage. O projeto
antigo do titular não foi usado como substituto. A conferência posterior,
por conexão TLS validada e transação somente leitura, encontrou:

- 43 tabelas públicas, todas com RLS ativa; nenhuma tabela removida.
- 15 migrações e três contas Auth, com as mesmas contagens anteriores.
- Nenhuma redução nas contagens de registros das 43 tabelas.
- Um bucket Storage e nenhum objeto; catálogo de empresas já estava vazio.
- Onze verificações HTTP da PWA/site aprovadas, incluindo proteção de cache
  administrativo e associação Android.

O SMTP do titular foi aplicado em 26/10/2026. Autenticação Gmail com TLS e
solicitações reais de recuperação pelo Supabase Auth passaram. O titular
mostrou o teste simples recebido na caixa de entrada; o recebimento do
e-mail de recuperação do Auth ainda aguarda confirmação. CAPTCHA e
confirmação de e-mail continuam obrigatórios. Ver `SMTP-TITULAR-2026-10-26.md`.

Nenhum plano pago, exclusão de projeto, migração de schema ou novo deploy
foi executado nesta transferência. A URL do Supabase, as credenciais públicas
da aplicação e o domínio do site foram preservados. Recibo público atual:
`evidencias/entrega-titular-2026-10-27.json`.

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

- Titularidade de GitHub, organização Supabase e Cloudflare conferida.
- Teste simples do SMTP recebido; confirmar separadamente o recebimento do
  e-mail de recuperação do Supabase, com as proteções ativas.
- Validar login novo, recuperação, painel, cadastro/edição, logotipo, horários
  e desativação/reativação pelo fluxo real do titular.
- CI do novo repositório aprovado; conferir também a execução que registra
  esta atualização documental.
- Entregar os materiais privados e instruções de recuperação ao novo responsável.
- Somente após aceite, retirar acessos temporários específicos do Service Guide;
  preservar contas, tokens e automações que atendam outros projetos.

Fontes oficiais para a operação:

- https://docs.github.com/en/repositories/creating-and-managing-repositories/duplicating-a-repository
- https://supabase.com/docs/guides/platform/project-transfer
- https://supabase.com/kb/troubleshooting/error-target-organization-is-not-managed-by-vercel-marketplace-during-project-transfer
