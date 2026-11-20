# MDD â€” Mestre de DireÃ§Ã£o DinÃ¢mica

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


Skill para [Claude Code](https://claude.com/claude-code) que transforma **qualquer assunto** em um pacote completo de direÃ§Ã£o de vÃ­deo dinÃ¢mico, pronto pra gerar em Seedance, Kling, Runway, Veo, Luma ou similares.

Em vez de devolver "uma pessoa usando X", a skill dirige uma **cena com movimento, intenÃ§Ã£o e continuidade**: cÃ¢mera que muda por motivo, aÃ§Ã£o que progride e um fechamento forte.

## O que ela gera

Para qualquer assunto, sempre na mesma ordem:

| Bloco | ConteÃºdo |
| --- | --- |
| **01 CartÃ£o do projeto** | tÃ­tulo, linha meta, prioridade, micro brief |
| **02 Pacote de cena** | premissa, resumo, local, elementos, estado inicial/final, cadeia de aÃ§Ã£o |
| **03 Bloqueios de estilo** | o que nÃ£o muda: estilo, cÃ¢mera, efeitos, continuidade, negativo |
| **04 Storyboard** | 8/12/16 painÃ©is â€” cÃ¢mera, aÃ§Ã£o, continuidade, efeito, intenÃ§Ã£o emocional |
| **05 Faixa do diretor** | beat, cÃ¢mera, aÃ§Ã£o, ritmo, escalaÃ§Ã£o, estado, estilo |
| **06 Prompt final de vÃ­deo** | prompt limpo pra colar na ferramenta de geraÃ§Ã£o |
| **07 Prompt negativo** | tudo que a IA deve evitar |

## A fÃ³rmula central

> **Assunto â†’ conflito visual â†’ progressÃ£o â†’ virada â†’ impacto suspenso.**

Sem conflito visual, o vÃ­deo fica parado. A skill encontra o conflito antes de montar o storyboard (produto: problema vs soluÃ§Ã£o; imÃ³vel: espaÃ§o comum vs experiÃªncia desejada; IA: tela vazia vs revelaÃ§Ã£o; etc.).

E a regra de ouro de cada tomada:

> **CÃ¢mera + aÃ§Ã£o + continuidade + emoÃ§Ã£o + efeito permitido.**

## O conceito: como o padrÃ£o Ã© construÃ­do

O MDD nÃ£o Ã© sÃ³ um template â€” Ã© um **sistema reaproveitÃ¡vel** pensado em 3 nÃ­veis crescentes de sofisticaÃ§Ã£o:

1. **Template fixo** â€” a estrutura nunca muda. A IA sempre preenche os mesmos blocos 01â€“07. Ã‰ o ponto de partida e garante consistÃªncia.
2. **Biblioteca de estilos e tomadas** â€” a IA escolhe cÃ¢mera, ritmo e efeitos conforme o assunto, puxando da biblioteca de tomadas e dos presets. Deixa de ser engessado e passa a se adaptar.
3. **Treinamento por exemplos** â€” vocÃª mostra 5, 10, 20 pacotes nesse formato e a IA aprende o seu gosto especÃ­fico.

O segredo Ã© nÃ£o "treinar" no sentido tÃ©cnico logo de cara: primeiro vocÃª cria o **formato mestre** e manda a IA sempre preencher esse formato. O refinamento vem depois.

### Como "treinar" a IA para o seu gosto

TrÃªs caminhos, do mais simples ao mais avanÃ§ado:

- **Por conversa** â€” peÃ§a o pacote e vÃ¡ corrigindo em linguagem natural: *"ficou bom, mas quero mais cÃ¢mera e menos texto"*, *"agora em 12 tomadas"*, *"agora versÃ£o 9:16"*. Com 5â€“10 exemplos a IA jÃ¡ segue melhor seu padrÃ£o.
- **Por biblioteca de presets** â€” categorias prontas (aÃ§Ã£o, produto premium, tech/IA, imobiliÃ¡rio, evento, histÃ³ria emocional) que a IA escolhe conforme o assunto. Veja `skill/references/presets.md`.
- **Por gerador de prompts prÃ³prio** â€” campos fixos (assunto, pÃºblico, formato, duraÃ§Ã£o, estilo, chamada, emoÃ§Ã£o, CTA, ferramenta) que sempre produzem a mesma saÃ­da: storyboard + prompt de imagem + prompt de vÃ­deo + prompt negativo + checklist.

**Esta skill jÃ¡ Ã© a realizaÃ§Ã£o desses 3 nÃ­veis:** o `SKILL.md` Ã© o template mestre + gerador; `references/biblioteca-tomadas.md` e `references/presets.md` sÃ£o a biblioteca de estilos; e a pasta `exemplos/` Ã© onde o treinamento por exemplos se acumula.

## Como usar

Com a skill instalada, basta pedir em linguagem natural:

```
direÃ§Ã£o dinÃ¢mica sobre IA no cinema
```
```
monta um pacote de vÃ­deo dinÃ¢mico pra esse produto, versÃ£o 9:16, 15s
```
```
transforma em 12 tomadas e usa o preset de imobiliÃ¡rio
```

A skill nÃ£o trava com perguntas: se faltar formato, duraÃ§Ã£o ou estilo, ela assume a opÃ§Ã£o mais forte pro conflito visual e declara a suposiÃ§Ã£o. A **chamada principal fica fora do prompt de vÃ­deo** (vai na ediÃ§Ã£o), pra evitar que a IA renderize texto torto.

## Estrutura

```
skill/
â”œâ”€â”€ SKILL.md                    # fluxo, fÃ³rmula de ouro, template 01â€“07, checklist de qualidade
â””â”€â”€ references/
    â”œâ”€â”€ biblioteca-tomadas.md   # tomadas de cÃ¢mera (push-in, crash zoom, orbitâ€¦) + sequÃªncias por assunto
    â””â”€â”€ presets.md              # 6 presets de estilo + guia de conflito visual por domÃ­nio
exemplos/                       # pacotes gerados (treinamento por exemplos)
â”œâ”€â”€ ia-no-cinema.md
â””â”€â”€ hormozi-12-dicas.md
```

### Presets disponÃ­veis

AÃ§Ã£o/esporte Â· Produto premium Â· Tecnologia/IA Â· ImobiliÃ¡rio Â· Evento Â· HistÃ³ria emocional.

## InstalaÃ§Ã£o

Copie a pasta `skill/` para o diretÃ³rio de skills do Claude Code, com o nome da skill:

```bash
cp -r skill ~/.claude/skills/mestre-direcao-dinamica
```

A skill passa a ser acionada automaticamente quando vocÃª pedir "direÃ§Ã£o dinÃ¢mica", "vÃ­deo dinÃ¢mico sobre X", "storyboard + prompt de vÃ­deo", "pacote de vÃ­deo" ou der um assunto pra virar vÃ­deo cinematogrÃ¡fico.

## LicenÃ§a

MIT.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>