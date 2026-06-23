# Bruno Messias

> Desenvolvedor Sênior. Construo produtos full-stack, geralmente do tipo que precisa conversar com banco de dados, autenticação decente, deploy que não cai na sexta e código que o próximo dev entende sem precisar me ligar.

**Tech Lead na Rybená** (acessibilidade web em Libras) e, nos horários vagos, mantenho uns projetos próprios que ainda não explodiram.

<p>
  <a href="https://github.com/brunosmessias?tab=repositories"><img alt="GitHub repos" src="https://img.shields.io/badge/GitHub-brunosmessias-181717?logo=github&logoColor=white"></a>
  <a href="https://brunosmessias.github.io/"><img alt="Site" src="https://img.shields.io/badge/Site-brunosmessias.github.io-2563eb"></a>
</p>

---

## 🔧 Stack com a qual eu trabalho todo dia

<p>
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white&logoWidth=20">
  <img alt="Next.js" src="https://img.shields.io/badge/Next.js-000000?logo=next.js&logoColor=white">
  <img alt="React" src="https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=06121F">
  <img alt="Node.js" src="https://img.shields.io/badge/Node.js-22-339933?logo=node.js&logoColor=white">
  <img alt="Bun" src="https://img.shields.io/badge/Bun-000000?logo=bun&logoColor=white">
  <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-15-4169E1?logo=postgresql&logoColor=white">
  <img alt="Drizzle" src="https://img.shields.io/badge/Drizzle-C5F74F?logo=drizzle&logoColor=000000">
  <img alt="tRPC" src="https://img.shields.io/badge/tRPC-v11-398CCB?logo=trpc&logoColor=white">
  <img alt="Better Auth" src="https://img.shields.io/badge/Better_Auth-000000?logoColor=white">
  <img alt="Tailwind" src="https://img.shields.io/badge/Tailwind-v4-38B2AC?logo=tailwindcss&logoColor=white">
  <img alt="shadcn/ui" src="https://img.shields.io/badge/shadcn/ui-000000?logoColor=white">
  <img alt="Rust" src="https://img.shields.io/badge/Rust-stable-000000?logo=rust&logoColor=E07C16">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.11+-3776AB?logo=python&logoColor=FFD43B">
  <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white">
</p>

<details>
<summary><b>Mais coisas que eu pego da prateleira</b></summary>

<br>

- **Front:** Astro 6, React 19 Server Components, TanStack Query/Table/Form, HeroUI v2, Zod
- **Back:** Hono, Express, tRPC v11, Drizzle, Prisma (de vez em quando), Redis, BullMQ
- **Auth/RBAC:** Better Auth, NextAuth, RBAC customizado por módulo/perfil
- **Pagamentos:** Stripe, Asaas (PIX/boleto)
- **Mensageria/Comunicação:** Resend, react-email, WhatsApp Business API, uazapiGO, SSE/WebSockets
- **Storage:** S3, Cloudflare R2, MinIO
- **Busca/IA:** FAISS, sentence-transformers, spaCy, OpenAI-compatible APIs
- **Outros:** Playwright (e2e), Vitest, Bun test, Bun runtime, pnpm/bun/npm
- **Mobile / Cross:** React Native (básico), PWA

</details>

---

## 🏢 Trabalho atual — Rybená

Plataforma brasileira de **acessibilidade web em Libras** (tradução de texto/áudio para língua de sinais, voice synthesis, ferramentas de inclusão). Site em produção: [rybena.com.br](https://rybena.com.br).

Sou um dos engenheiros do time. Atuo em vários produtos ao mesmo tempo — aqui vai o que tem no meu radar:

- **Site institucional & funil de vendas** (`site-astro`) — Astro 6 SSR + Cloudflare Pages. SEO, JSON-LD, modal de trial em 4 passos, checkout via Stripe.
- **Comercial — back-end** (`comercial-api`) — gestão de clientes, domínios, licenças, agentes. Onde mora a maior parte da regra de negócio de cobrança e trial.
- **Comercial — front-end** (`comercial-gestao`) — dashboard admin (HeroUI v2 + TanStack Query) rodando em Cloudflare Pages via OpenNext.
- **Serviço semântico de sinais** (`semantic-service`) — Python + FastAPI + FAISS. Resolve texto em candidatos de sinal com ranking híbrido (lexical + semântico). Roda em cluster Kubernetes.
- **Núcleo de Libras** (`core-librasgo`, `core-servertts`) — engine de tradução e síntese de voz.
- **Players e plugins** — players HTML/Unity3D, plugins Moodle/WordPress/PDF.js, dicionário de sinais.
- **CDN, blog, cron-manager** — a infra de suporte que ninguém vê mas todo mundo precisa.

### O que eu faço na Rybená

- Mantenho o **cluster Kubernetes** (manifests em `semantic-service/k8s/base/`) e os pipelines do **Jenkins**.
- Defino padrões de **RBAC**, modelagem de dados e boundaries de domínio entre os serviços.
- Reviso PR, oriento decisões técnicas e ajudo o time a sair do "funciona" pro "funciona e dá pra manter".
- Trabalho próximo do comercial pra traduzir "como o cliente quer pagar" em schema e fluxo de checkout.

---

## 🚀 Projetos pessoais (com material real)

> Alguns em produção, alguns em fase de dar orgulho. Sem invented metrics — só o que está no código ou no disco.

### [`commitai`](https://github.com/brunosmessias/commitai) — Rust · público

CLI em Rust que gera mensagens de commit com **qualquer provedor de IA compatível com OpenAI** (OpenAI, OpenRouter, Groq, DeepSeek, Ollama local, etc.). Integra direto com [lazygit](https://github.com/jesseduffield/lazygit) — você escolhe a mensagem num menu dentro do TUI.

- Binário estático de ~3 MB, sem runtime, sem Node, sem Python.
- `install.sh` detecta SO/arch, baixa do GitHub Releases, instala em `~/.local/bin`.
- **Funciona com qualquer modelo** — não trava o usuário no OpenAI.
- Prompt templates editáveis, `commitai config` com menu interativo, primeira execução com wizard e teste de conexão.
- Keys em `~/.config/commitai/config.toml`, nunca saem da máquina.

Eu uso todo dia. Foi escrito pra preencher uma lacuna real do [`chhoumann/bunnai`](https://github.com/chhoumann/bunnai) (mesma ideia, Rust mais antigo, travado no OpenAI).

### `senhorimoveis` (privado) — Next.js 15

Plataforma full-stack de **gestão imobiliária com whitelabel**, multi-tenant, CRM, contratos, portal de locatário/proprietário e **WhatsApp via uazapiGO v2 com SSE em tempo real**.

- Next.js 15 (App Router) + tRPC v11 + Drizzle + PostgreSQL + Better Auth
- **Whitelabel por env vars** (nome, cores, logo, contato, jurídico) — cada publisher vira um "site" próprio
- SSE singleton por publisher (`/api/sse/[publisherId]`) com heartbeat de 30s pra não cair
- Webhooks WhatsApp `/api/whatsapp/webhook/[...slug]/`
- Uploads via **presigned URL direto pro S3** (R2/MinIO compat), nunca no app
- Moeda **sempre em centavos** (integer) — `convertToCents("1.450,00")` → `145000`
- Middleware com 300+ linhas de auth + RBAC granular por módulo

### `nossa-grana` (público) — Next.js 16

App de **finanças pessoais para famílias brasileiras** (pt-BR). Modelo family-scoped: tudo pertence a uma família, com roles OWNER/ADMIN/MEMBER e `assertFamilyMember()` antes de qualquer leitura.

- Next.js 16 (App Router, RSC) + React 19 + tRPC v11 + Drizzle + better-auth (Google + Email OTP)
- **Zod compartilhado client/server** via `src/shared/schemas/` — uma validação só, pro front e pro back
- TanStack Form + Tailwind v4 (CSS-first, sem `tailwind.config`) + shadcn/ui (`base-nova` em cima de `@base-ui/react`)
- **Audit log** de toda mutação: actor, entity, before/after JSON, requestId
- Moeda em centavos, IDs UUID, Drizzle migrations versionadas
- Regras de negócio com TLC spec-driven — sem `any`, 500 linhas/arquivo, ESLint como gate
- **v2 em draft** reescrito do zero com arquitetura auditável e guia oficial de novos projetos (vai substituir a v1)

### `agroanalise` (privado) — Next.js 16

Sistema de **gestão de análises agronômicas** com dashboard, upload de fotos georreferenciadas (Leaflet + clusters), geração de PDF (`@react-pdf/renderer`), QR code de compartilhamento, e PWA instalável.

- T3 stack (Next + tRPC + Drizzle) + Better Auth (admin plugin + access control)
- Upload processado server-side com **Sharp**: WebP automático, max 2048px, thumbnails 300px
- Storage proxy `/api/storage/[...path]` servindo do MinIO
- Reset de senha nativo do Better Auth (token 1h, `revokeSessionsOnPasswordReset`), email via Resend
- Estados de tela obrigatórios: loading, vazio, erro, sem permissão — para tudo

### `contador-online` (no cliente, contribuo) — Next.js 15

Plataforma SaaS B2B2C que conecta **contadores** com **clientes** para consultorias por vídeo. Repo: [contadoronline/web-contador-online-nextjs](https://github.com/contadoronline/web-contador-online-nextjs).

- Next.js 15 + tRPC v11 + Drizzle + PostgreSQL (schema `contadoronline`) + Better Auth
- HeroUI v2 + Tailwind + Framer Motion + React Leaflet (mapas de contadores)
- **Asaas** (PIX/boleto) + **Agora.io** (tokens de vídeo) + WhatsApp API (Meta) + S3/MinIO
- 100–500ms de delay artificial em dev pra simular latência de produção
- Deploy com `docker-compose -f docker-compose.prod.yml` na VPS

---

## 🛠️ Infra & DevOps

Coisa que eu opero direto, não só "li o README":

- **Kubernetes** — manifests em `~/Rybená/semantic-service/k8s/base/`. Faço o básico bem: Deployments, Services, ConfigMaps, HPA, namespace isolation.
- **Jenkins** — pipelines de CI/CD da Rybená. Build → test → push GHCR → deploy no cluster.
- **Dokploy** — CI/CD dos projetos pessoais e clientes. Mais simples que o cluster K8s, suficiente pra 90% das coisas.
- **Docker / Docker Compose** — multi-stage builds, `bun imob`/`bun dev`/`bun prod` com compose separados.
- **Cloudflare Pages** — `site-astro` e `comercial-gestao` rodam em SSR via `@astrojs/cloudflare` e `opennextjs-cloudflare` respectivamente. Wrangler + `_headers`/`_redirects` na munheca.
- **GHCR** (GitHub Container Registry) — imagens privadas para deploy.
- **VPS** — Dokploy self-hosted, Postgres, MinIO. Onde rodam o contador-online, senhorimoveis, agroanalise e o pessoal.
- **Postgres** em produção — Drizzle migrations rodando, `bun db:push` proibido em prod, `bun db:studio` pra investigar.

---

## 🧠 Como eu penso engenharia

Não é título de LinkedIn, é o que aparece no PR:

- **Arquitetura primeiro, código depois.** Antes de sair criando tabela, defino o domínio — quem é o ator, qual o lifecycle do recurso, onde mora a regra de negócio (service, não router). Uso **TLC spec-driven** como ritual: spec → design → tasks → execute. Toda decisão vira `.specs/` antes de virar commit.
- **Boundaries explícitos.** `shared/` não importa de `server/`. Procedures de leitura têm `.output(schema)`. Procedures que recebem `id` fazem ownership check. RBAC por módulo/perfil/função, não por URL.
- **Validação no boundary, confiança dentro.** Zod único no `shared/schemas/`, reusado pelo TanStack Form no front e pelo procedure no back. `notNull` no DB **não é validação** — é constraint de integridade.
- **Tipos como ferramenta de design, não como decoração.** `z.infer<typeof schema>`, `RouterInputs/Outputs`, sem `any` sem motivo grave, `noUncheckedIndexedAccess` ligado. Prefiro o compilador reclamando agora a runtime reclamando em produção.
- **Performance por default em três lugares:** (1) **paginação server-side** desde o dia 1 (transactions, listagens, dashboards) — nunca `findMany()` no caminho quente; (2) **queries N+1 eliminadas na modelagem** — Drizzle relations + `with:` explícito; (3) **render de listas grandes** com TanStack Virtual quando passa de algumas centenas de linhas. E quando precisa de mais, **SSE/streaming** em vez de polling (WhatsApp, real-time).
- **Segurança como hábito, não checklist.** Cookie `httpOnly` + `sameSite`, secrets via `@t3-oss/env-nextjs` + Zod (sem `process.env` solto), headers no Cloudflare (`_headers`), validação de origem em webhooks, RBAC verificado **no procedure**, não na UI. Mensagens de erro do tRPC nunca vazam pro cliente — mapeio por `code`.
- **UX que dev percebe.** Estados de tela obrigatórios: loading, vazio, erro, sem permissão. Skeleton no carregamento, ilustração + CTA no vazio, retry no erro. Acessibilidade não é feature: `<Label htmlFor>`, `role="alert"`, `focus-visible:ring`, touch target 44x44, contraste, e pluralização PT-BR que não vira "izaçãoes".
- **Erro legível pra humano, não pra console.** `toast.error` em pt-BR com a mensagem do Zod, `AlertDialog` pra delete destrutivo, `disabled={mutation.isPending}` no submit. Nunca `window.confirm`.
- **Datas e moeda sem armadilha.** UTC no banco, conversão local na UI, `toLocaleDateString("en-CA")` pra evitar off-by-one em BRT. Centavos como `integer` sempre — converter na borda.
- **CI verde ou não foi feito.** Typecheck, lint filtrado pros arquivos da feature, testes unit + e2e (Playwright/Vitest) onde a regra de negócio pede. `bun check` antes do `git push`.
- **Documentação que envelhece bem.** `AGENTS.md` em todo repo descrevendo stack, comandos, padrões, gotchas. Toda mudança em regra de negócio ou padrão visual atualiza o doc na mesma PR. Prefiro 1 nota boa por sessão do que 12 espalhadas.

---

## 📚 Engineering Playbook (pessoal)

Tenho um repositório interno (`~/Pessoal/engineering-playbook/`) com princípios, arquitetura, UX, coding standards, testing, git e field notes sobre agentes. Funciona como o "código de conduta" técnico que eu aplico em qualquer projeto novo. Se você for mexer num repo meu, vale a leitura do `AGENTS.md` — ele te economiza uma tarde.

---

## 📫 Onde me achar

- **GitHub:** [@brunosmessias](https://github.com/brunosmessias) — você já está aqui
- **Email:** [brunodsm10@gmail.com](mailto:brunodsm10@gmail.com)
- **Org Rybená:** [Rybena](https://github.com/Rybena) (repos privados)
- **Commit que eu uso todo dia:** [`brunosmessias/commitai`](https://github.com/brunosmessias/commitai)

Se a conversa for sobre Next.js, tRPC, Drizzle, acessibilidade em Libras, infra K8s/Dokploy, ou Rust — provavelmente vale meu tempo. Se for pra debater tabs vs spaces, eu uso **2 spaces, semicolons, single quotes, sem trailing comma** e morro nessa hill.
