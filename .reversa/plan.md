# Plano de Exploração — skills

> Criado pelo Reversa em 2026-05-15
> Marque cada tarefa com ✅ quando concluída.
> Você pode editar este plano antes de iniciar: adicione, remova ou reordene tarefas conforme necessário.

---

## Fase 1: Reconhecimento 🔍

- [x] ✅ **Scout** — Mapeamento de estrutura de pastas e tecnologias
- [x] ✅ **Scout** — Análise de dependências e gerenciadores de pacotes
- [x] ✅ **Scout** — Identificação de entry points, CI/CD e configurações

## Decisão de organização das specs 🗂️

> Entre o Scout e o Arqueólogo, o Reversa pergunta como você quer organizar as specs (por módulo, caso de uso, endpoint, híbrida, por features ou customizada). A escolha fica persistida em `.reversa/config.toml` na seção `[specs]` e não será reperguntada em execuções futuras. Para reapresentar o menu, remova manualmente a seção.

## Fase 2: Escavação 🏗️

- [x] ✅ **Archaeologist** — Analysis of the `engineering` module (10 skills: diagnose, grill-with-docs, improve-codebase-architecture, prototype, setup-matt-pocock-skills, tdd, to-issues, to-prd, triage, zoom-out)
- [x] ✅ **Archaeologist** — Analysis of the `productivity` module (4 skills: caveman, grill-me, handoff, write-a-skill)
- [x] ✅ **Archaeologist** — Analysis of the `misc` module (4 skills: git-guardrails-claude-code, migrate-to-shoehorn, scaffold-exercises, setup-pre-commit)
- [x] ✅ **Archaeologist** — Analysis of the `in-progress` module (4 skills: review, writing-beats, writing-fragments, writing-shape)

## Fase 3: Interpretação 🧠

- [x] ✅ **Detetive** — Arqueologia Git e ADRs retroativos (15 ADRs gerados em `_reversa_sdd/adrs/`)
- [x] ✅ **Detetive** — Regras de negócio implícitas e máquinas de estado (`domain.md`, `state-machines.md`)
- [x] ✅ **Detetive** — Matriz de permissões (RBAC/ACL) (`permissions.md` — 4 actors, capability matrix)
- [x] ✅ **Arquiteto** — Diagramas C4 (c4-context.md, c4-containers.md, c4-components.md)
- [x] ✅ **Arquiteto** — ERD completo e integrações externas (erd-complete.md — 24 entidades)
- [x] ✅ **Arquiteto** — Spec Impact Matrix (traceability/spec-impact-matrix.md)

## Fase 4: Geração 📝

- [x] ✅ **Redator** — Specs SDD por componente (4 units × requirements + design + tasks + edge-cases + optional files)
- [x] ✅ **Redator** — OpenAPI (n/a — no HTTP API in this system)
- [x] ✅ **Redator** — User Stories (user-stories/engineering-workflows.md + writing-workflows.md)
- [x] ✅ **Redator** — Code/Spec Matrix (traceability/code-spec-matrix.md — ~85% coverage)

## Fase 5: Revisão ✅

- [x] ✅ **Revisor** — Revisão cruzada de specs (solo — Codex unavailable; 3 reclassifications)
- [x] ✅ **Revisor** — Resolução de lacunas com o usuário (11 gaps identified; questions.md + gaps.md generated)
- [x] ✅ **Revisor** — Relatório de confiança final (confidence-report.md — overall 73%)

---

## Agentes Independentes

> Execute estes agentes quando os recursos estiverem disponíveis — podem rodar em qualquer fase.

- [ ] **Visor** — Análise de interface via screenshots
- [ ] **Data Master** — Análise completa do banco de dados
- [ ] **Design System** — Extração de tokens de design
- [ ] **Tracer** — Análise dinâmica (requer sistema acessível)

---

## Próximo passo

Após o Time de Descoberta concluir e o `_reversa_sdd/` estar populado, você pode disparar um dos fluxos seguintes:

- `/reversa-migrate`: orquestrador do **Time de Migração** (Paradigm Advisor → Curator → Strategist → Designer → Screen Translator → Inspector). Gera as specs do sistema novo. Saída em `_reversa_sdd/migration/` e `_reversa_sdd/screens/`.
- `/reversa-reconstructor`: gera plano bottom-up para reimplementar o software a partir das specs do legado (uma tarefa por sessão).
