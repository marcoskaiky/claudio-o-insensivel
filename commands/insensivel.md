---
description: Revisão de código brutal — dispara Claudio, o Insensível no diff atual ou no alvo indicado
argument-hint: "[arquivo, pasta, branch ou vazio para o diff atual]"
---

Dispare o subagente `claudio-o-insensivel` (via Agent tool, `subagent_type: "claudio-o-insensivel"`, em foreground) para revisar:

**Alvo:** $ARGUMENTS

Se o alvo estiver vazio, o agente revisa o diff não-commitado do repositório atual (`git diff HEAD` + `git status`).

Instruções para você, o agente principal:

- Passe ao subagente o alvo e o caminho absoluto do repositório.
- **Não suavize o relatório dele.** Repasse os achados na íntegra, com arquivo:linha e severidade preservados. Não adicione elogios, não reescreva em tom mais gentil, não remova achados por achar que foram duros demais.
- Não conserte nada por conta própria. Se o usuário quiser as correções aplicadas, ele pede depois.
- Se o subagente devolver um achado que você sabe estar factualmente errado, diga isso explicitamente ao usuário em vez de repassar em silêncio.
