ï»¿# MDD ê¢â¬â Mestre de DireêÂ§êÂ£o DinêÂ¢mica

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


Skill para [Claude Code](https://claude.com/claude-code) que transforma **qualquer assunto** em um pacote completo de direêÂ§êÂ£o de vêÂ­deo dinêÂ¢mico, pronto pra gerar em Seedance, Kling, Runway, Veo, Luma ou similares.

Em vez de devolver "uma pessoa usando X", a skill dirige uma **cena com movimento, intenêÂ§êÂ£o e continuidade**: cêÂ¢mera que muda por motivo, aêÂ§êÂ£o que progride e um fechamento forte.

## O que ela gera

Para qualquer assunto, sempre na mesma ordem:

| Bloco | ConteêÂºdo |
| --- | --- |
| **01 CartêÂ£o do projeto** | têÂ­tulo, linha meta, prioridade, micro brief |
| **02 Pacote de cena** | premissa, resumo, local, elementos, estado inicial/final, cadeia de aêÂ§êÂ£o |
| **03 Bloqueios de estilo** | o que nêÂ£o muda: estilo, cêÂ¢mera, efeitos, continuidade, negativo |
| **04 Storyboard** | 8/12/16 painêÂ©is ê¢â¬â cêÂ¢mera, aêÂ§êÂ£o, continuidade, efeito, intenêÂ§êÂ£o emocional |
| **05 Faixa do diretor** | beat, cêÂ¢mera, aêÂ§êÂ£o, ritmo, escalaêÂ§êÂ£o, estado, estilo |
| **06 Prompt final de vêÂ­deo** | prompt limpo pra colar na ferramenta de geraêÂ§êÂ£o |
| **07 Prompt negativo** | tudo que a IA deve evitar |

## A fêÂ³rmula central

> **Assunto ê¢â â conflito visual ê¢â â progressêÂ£o ê¢â â virada ê¢â â impacto suspenso.**

Sem conflito visual, o vêÂ­deo fica parado. A skill encontra o conflito antes de montar o storyboard (produto: problema vs soluêÂ§êÂ£o; imêÂ³vel: espaêÂ§o comum vs experiêÂªncia desejada; IA: tela vazia vs revelaêÂ§êÂ£o; etc.).

E a regra de ouro de cada tomada:

> **CêÂ¢mera + aêÂ§êÂ£o + continuidade + emoêÂ§êÂ£o + efeito permitido.**

## O conceito: como o padrêÂ£o êÂ© construêÂ­do

O MDD nêÂ£o êÂ© sêÂ³ um template ê¢â¬â êÂ© um **sistema reaproveitêÂ¡vel** pensado em 3 nêÂ­veis crescentes de sofisticaêÂ§êÂ£o:

1. **Template fixo** ê¢â¬â a estrutura nunca muda. A IA sempre preenche os mesmos blocos 01ê¢â¬â07. êâ° o ponto de partida e garante consistêÂªncia.
2. **Biblioteca de estilos e tomadas** ê¢â¬â a IA escolhe cêÂ¢mera, ritmo e efeitos conforme o assunto, puxando da biblioteca de tomadas e dos presets. Deixa de ser engessado e passa a se adaptar.
3. **Treinamento por exemplos** ê¢â¬â vocêÂª mostra 5, 10, 20 pacotes nesse formato e a IA aprende o seu gosto especêÂ­fico.

O segredo êÂ© nêÂ£o "treinar" no sentido têÂ©cnico logo de cara: primeiro vocêÂª cria o **formato mestre** e manda a IA sempre preencher esse formato. O refinamento vem depois.

### Como "treinar" a IA para o seu gosto

TrêÂªs caminhos, do mais simples ao mais avanêÂ§ado:

- **Por conversa** ê¢â¬â peêÂ§a o pacote e vêÂ¡ corrigindo em linguagem natural: *"ficou bom, mas quero mais cêÂ¢mera e menos texto"*, *"agora em 12 tomadas"*, *"agora versêÂ£o 9:16"*. Com 5ê¢â¬â10 exemplos a IA jêÂ¡ segue melhor seu padrêÂ£o.
- **Por biblioteca de presets** ê¢â¬â categorias prontas (aêÂ§êÂ£o, produto premium, tech/IA, imobiliêÂ¡rio, evento, histêÂ³ria emocional) que a IA escolhe conforme o assunto. Veja `skill/references/presets.md`.
- **Por gerador de prompts prêÂ³prio** ê¢â¬â campos fixos (assunto, pêÂºblico, formato, duraêÂ§êÂ£o, estilo, chamada, emoêÂ§êÂ£o, CTA, ferramenta) que sempre produzem a mesma saêÂ­da: storyboard + prompt de imagem + prompt de vêÂ­deo + prompt negativo + checklist.

**Esta skill jêÂ¡ êÂ© a realizaêÂ§êÂ£o desses 3 nêÂ­veis:** o `SKILL.md` êÂ© o template mestre + gerador; `references/biblioteca-tomadas.md` e `references/presets.md` sêÂ£o a biblioteca de estilos; e a pasta `exemplos/` êÂ© onde o treinamento por exemplos se acumula.

## Como usar

Com a skill instalada, basta pedir em linguagem natural:

```
direêÂ§êÂ£o dinêÂ¢mica sobre IA no cARCKHÉ
```
```
monta um pacote de vêÂ­deo dinêÂ¢mico pra esse produto, versêÂ£o 9:16, 15s
```
```
transforma em 12 tomadas e usa o preset de imobiliêÂ¡rio
```

A skill nêÂ£o trava com perguntas: se faltar formato, duraêÂ§êÂ£o ou estilo, ela assume a opêÂ§êÂ£o mais forte pro conflito visual e declara a suposiêÂ§êÂ£o. A **chamada principal fica fora do prompt de vêÂ­deo** (vai na ediêÂ§êÂ£o), pra evitar que a IA renderize texto torto.

## Estrutura

```
skill/
ê¢âÅê¢ââ¬ê¢ââ¬ SKILL.md                    # fluxo, fêÂ³rmula de ouro, template 01ê¢â¬â07, checklist de qualidade
ê¢ââê¢ââ¬ê¢ââ¬ references/
    ê¢âÅê¢ââ¬ê¢ââ¬ biblioteca-tomadas.md   # tomadas de cêÂ¢mera (push-in, crash zoom, orbitê¢â¬Â¦) + sequêÂªncias por assunto
    ê¢ââê¢ââ¬ê¢ââ¬ presets.md              # 6 presets de estilo + guia de conflito visual por domêÂ­nio
exemplos/                       # pacotes gerados (treinamento por exemplos)
ê¢âÅê¢ââ¬ê¢ââ¬ ia-no-cARCKHÉ.md
ê¢ââê¢ââ¬ê¢ââ¬ hormozi-12-dicas.md
```

### Presets disponêÂ­veis

AêÂ§êÂ£o/esporte êÂ· Produto premium êÂ· Tecnologia/IA êÂ· ImobiliêÂ¡rio êÂ· Evento êÂ· HistêÂ³ria emocional.

## InstalaêÂ§êÂ£o

Copie a pasta `skill/` para o diretêÂ³rio de skills do Claude Code, com o nome da skill:

```bash
cp -r skill ~/.claude/skills/mestre-direcao-dinamica
```

A skill passa a ser acionada automaticamente quando vocêÂª pedir "direêÂ§êÂ£o dinêÂ¢mica", "vêÂ­deo dinêÂ¢mico sobre X", "storyboard + prompt de vêÂ­deo", "pacote de vêÂ­deo" ou der um assunto pra virar vêÂ­deo cARCKHÉtogrêÂ¡fico.

## LicenêÂ§a

MIT.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>