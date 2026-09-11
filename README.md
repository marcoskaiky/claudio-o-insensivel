# Claudio, o Insensível

Revisor de código para Claude Code que não é seu amigo.

Aponta toda falha com `arquivo:linha`, o mecanismo exato do defeito e o que fazer para
resolver. Sem elogios, sem "no geral está bom", sem sanduíche de feedback. O veredito
padrão é **REPROVADO** e o melhor resultado possível é "APROVADO COM RESSALVAS".

Ele **não corrige nada** — não tem ferramenta de escrita, e isso é proposital. Diz o que
fazer com precisão suficiente para não haver desculpa. Consertar é com você.

## Instalação

```
/plugin marketplace add SEU-USUARIO/claudio-o-insensivel
/plugin install claudio-o-insensivel@claudio
```

Reinicie o Claude Code depois de instalar.

## Uso

```
/insensivel                 # revisa o diff não-commitado
/insensivel src/auth.ts     # revisa um arquivo ou pasta
/insensivel minha-branch    # revisa uma branch
```

Também atende chamado pelo nome: "manda o Claudio olhar isso".

## Instalação manual (sem plugin)

Copie os dois arquivos para o seu config global:

```
agents/claudio-o-insensivel.md  ->  ~/.claude/agents/
commands/insensivel.md          ->  ~/.claude/commands/
```

## Calibragem

A intensidade mora em dois lugares de `agents/claudio-o-insensivel.md`: a seção
**Personalidade** e a lista de **frases banidas**. Para amaciar, encurte a lista de
banidas — não amoleça a personalidade, senão ele vira revisor genérico de novo.

A regra que não se mexe é a **regra zero**: toda crítica tem que ser verificável. Um
revisor hostil que inventa bug perde a única coisa que o torna útil.
