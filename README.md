# Service Guide

Descoberta de empresas, produtos e serviços locais em Cacoal, Rondônia.

- [Site publicado](https://service-guide.helon280.workers.dev/)
- [Painel administrativo](https://service-guide.helon280.workers.dev/admin)
- [Instalação PWA no Android e iPhone](https://service-guide.helon280.workers.dev/instalar)
- [Repositório oficial do titular](https://github.com/paulohelon280/service-guide)

TanStack Start, React, TypeScript e Cloudflare Workers; banco, autenticação e
controle de acesso no Supabase. O modelo antigo de marketplace foi aposentado.

## Trabalhar no projeto

Leia [documentos/AGENTS.md](documentos/AGENTS.md) antes de alterar o código.
Use Node.js 24 ou superior. Copie `.env.example` para `.env.local` e preencha
as variáveis do projeto; mantenha senhas e tokens fora do Git.

```bash
npm ci
npm run dev
```

Um ambiente com as credenciais reais acessa o backend real. Os laboratórios
isolados e os comandos de validação estão documentados no guia do projeto.
Deploy e migrações de produção exigem validação humana.

## Operação e entrega

- [Arquitetura e decisões](documentos/DECISIONS.md)
- [Configuração e segredos](documentos/ENVIRONMENT.md)
- [Publicação e recuperação](documentos/DEPLOYMENT.md)
- [Painel administrativo](documentos/ADMIN.md)
- [Estado das versões instaláveis](documentos/PUBLICACAO-PWA-2026-10-26.md)
- [Transferência ao titular](documentos/TRANSFERENCIA-HELON-2026-10-26.md)

A PWA está publicada. APK/AAB Android foram compilados e assinados, ainda sem
publicação na Play Store. O aplicativo da App Store não foi desenvolvido.
