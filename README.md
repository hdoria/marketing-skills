# marketing-skills

Plugin de marketing em **português** pra Claude Cowork e Claude Code.

**21 skills** que cobrem o ciclo completo: pesquisa de mercado, ideação afiada, escrita por canal, construção de páginas, edição anti-slop, conselho consultivo de modelos, distribuição multi-canal, e meta-skills pra criar suas próprias skills.

Curado por [Hugo Doria](https://github.com/hdoria) pra apoiar o workshop **Claude para Marketing** da [Vibe Makers](https://vibemakers.com.br).

---

## Sumário

- [O que vem com o plugin](#o-que-vem-com-o-plugin)
- [Estrutura do repositório](#estrutura-do-repositório)
- [Instalar (via marketplace · recomendado)](#instalar-via-marketplace--recomendado)
- [Instalação manual (alternativa)](#instalação-manual-alternativa)
- [Como usar uma skill](#como-usar-uma-skill)
- [Workflows do workshop](#workflows-do-workshop)
- [Tutorial completo do curso](#tutorial-completo-do-curso)
- [Catálogo das 21 skills](#catálogo-das-21-skills)
- [Premissas](#premissas)
- [Regras anti-slop herdadas](#regras-anti-slop-herdadas)
- [Contribuir / customizar](#contribuir--customizar)
- [Licença](#licença)

---

## O que vem com o plugin

| Família | Skills |
|---|---|
| Pesquisa e fundação | `entrevista-negocio`, `pesquisa-keywords`, `auditoria-seo` |
| Ideação e estratégia | `afiar-ideia`, `hooks-virais-x`, `arquitetar-oferta` |
| Escrita por canal | `post-longo-x`, `escrever-linkedin`, `escrever-newsletter`, `escrever-artigo`, `escrever-copy`, `sequencia-email` |
| Páginas e produtos | `landing-page`, `lead-magnet`, `design-frontend` |
| Edição e qualidade | `polir-texto`, `humanizar-texto`, `conselho-llm` |
| Distribuição | `reaproveitar-conteudo` |
| Meta (criar mais skills) | `criar-skill`, `entrevista-skill` |

Cada skill é um arquivo `SKILL.md` com frontmatter YAML (nome, descrição, gatilhos) e o playbook em markdown. A descrição é o que o Claude lê pra decidir quando ativar a skill automaticamente.

---

## Estrutura do repositório

O repo segue o padrão "marketplace com pasta `plugins/`" recomendado pela Anthropic — o que permite hospedar mais de um plugin no mesmo repositório no futuro (ex: `plugins/sales-skills`, `plugins/ops-skills`) sem reorganizar nada.

```text
marketing-skills/                       ← repo (= marketplace)
├── .claude-plugin/
│   └── marketplace.json                ← catálogo de plugins do repo
├── plugins/
│   └── marketing-skills/               ← o plugin em si
│       ├── .claude-plugin/
│       │   └── plugin.json             ← manifesto do plugin
│       └── skills/                     ← 21 pastas, uma por skill
│           ├── afiar-ideia/
│           │   └── SKILL.md
│           ├── post-longo-x/
│           │   └── SKILL.md
│           └── ...
├── README.md
└── LICENSE
```

O `marketplace.json` usa `metadata.pluginRoot: "./plugins"`, então o `source` de cada plugin pode ser apenas o nome da pasta (`"marketing-skills"`). Isso facilita adicionar novos plugins depois.

Quando você instala via marketplace no Cowork ou Code, o Claude resolve esses caminhos sozinho — você não precisa pensar nessa estrutura, só entender que o plugin "vive" em `plugins/marketing-skills/`.

---

## Instalar (via marketplace · recomendado)

É o mesmo caminho que o Ole Lehmann mostra no workshop original: você adiciona o repo como **marketplace** dentro do Claude e instala o plugin com um clique.

### Claude Cowork (app desktop)

1. Abra o Claude Desktop e troque pro modo **Cowork**.
2. **Customize → Personal plugins → Add plugin → Create plugin → Add marketplace**.
3. Cole a URL do repo: `https://github.com/hdoria/marketing-skills` e clique **Sync**.
4. Aparece a entrada **marketing-skills** em **Personal**. Clique **Install**.
5. Reinicie o Cowork (ou rode `/reload-plugins` se você estiver no Code).
6. **Validação**: peça ao Claude `"liste todas as skills que você tem disponíveis"`. Ele deve listar as 21.

### Claude Code (CLI/terminal)

```bash
/plugin marketplace add hdoria/marketing-skills
/plugin install marketing-skills@marketing-skills
/reload-plugins
```

Depois disso as skills ficam acessíveis com namespace: `/marketing-skills:afiar-ideia`, `/marketing-skills:post-longo-x`, etc.

---

## Instalação manual (alternativa)

Útil se você quer só clonar e usar localmente, sem passar pelo marketplace:

```bash
git clone https://github.com/hdoria/marketing-skills ~/.claude/plugins/marketing-skills
```

Reinicie o cliente. As skills aparecem em `list_skills` (o Claude resolve o `plugin.json` em `plugins/marketing-skills/.claude-plugin/` automaticamente).

Pra testar uma versão local apontando direto pra pasta do plugin:

```bash
claude --plugin-dir /caminho/pro/marketing-skills/plugins/marketing-skills
```

---

## Como usar uma skill

Você não precisa "carregar" a skill manualmente. O Claude detecta pelo gatilho da descrição. Três caminhos:

### 1. Mencionar pelo nome

```
Use a skill afiar-ideia pra trabalhar essa premissa: "automação com IA economiza tempo"
Público: founders de PME no Brasil
Formato: post longo no X
```

### 2. Descrever o que quer e deixar o Claude escolher

```
Tenho essa premissa boba sobre automação com IA. Me dá 5 ângulos mais afiados.
```

O Claude lê os gatilhos da `afiar-ideia` (`make this more interesting`, `find a surprising angle`, etc.) e ativa sozinha.

### 3. Pedir uma recomendação

```
Que skill eu deveria usar pra essa tarefa: transformar meu post de blog em conteúdo pra 4 canais?
```

Ele recomenda `reaproveitar-conteudo`.

---

## Workflows do workshop

A força do plugin tá nas **cadeias**. Skill por vez, mesmo chat. Você fica no comando e ajusta no caminho. Anti-padrão clássico: dump everything num único mega-prompt → resultado genérico, sem aprendizado.

### Fluxo 1 · Da ideia bruta ao post multi-canal (Exercício 4 do workshop)

```
ideia bruta
  → afiar-ideia            (5 ângulos, escolhe 1)
  → post-longo-x           (post pronto pro X)
  → humanizar-texto        (anti-slop opcional, se o post veio cru)
  → polir-texto            (10 passadas de edição)
  → reaproveitar-conteudo  (LinkedIn, Instagram, TikTok, YT Shorts)
```

**Passo a passo (no mesmo chat):**

```
1. Use a skill afiar-ideia. Material: "automação com IA economiza tempo das empresas".
   Público: founders de PME no Brasil. Formato: post longo no X.

2. Gostei do ângulo #3. Use post-longo-x pra escrever esse post.
   Estilo: cultural. Objetivo: autoridade.

3. Roda polir-texto. Formato: tweet. Agressividade: padrão.

4. Reaproveitar-conteudo: LinkedIn, Instagram, YouTube Shorts.
   ICP: founders de PME no Brasil.
```

### Fluxo 2 · Lançamento de produto

```
ideia de oferta
  → arquitetar-oferta   (promessa, mecanismo, prova, garantia, preço)
  → lead-magnet         (isca pra topo de funil)
  → landing-page        (página de venda)
  → sequencia-email     (nutrição até o pitch)
  → reaproveitar-conteudo (anúncios e posts pré-lançamento)
```

### Fluxo 3 · Conteúdo SEO

```
nicho
  → pesquisa-keywords   (clusters semânticos)
  → auditoria-seo       (estado atual do site)
  → escrever-artigo     (peça otimizada)
  → polir-texto         (polimento final)
  → reaproveitar-conteudo (LinkedIn, X, newsletter)
```

### Fluxo 4 · Pesquisa → landing pages

```
nicho + 2 concorrentes
  → pesquisa de dores (prompt do exercício 1, salva CSV em PESQUISAS/)
  → design-frontend + landing-page + humanizar-texto (em cadeia, batch de 2 LPs)
  → design.md (extraído de uma referência)
  → re-render de cada LP "on brand"
```

---

## Tutorial completo do curso

O plugin foi montado pra apoiar os 6 exercícios do workshop **Claude para Marketing**. Você pode usá-lo sozinho, mas pega o melhor se seguir o fluxo.

### 0. Pré-workshop · Construa o cérebro do Claude

Antes de rodar qualquer skill, configure o terreno:

1. **App desktop instalado** (não use `claude.com` — Cowork só funciona no app).
2. **Plano Pro ou Max** (Free não aguenta workshop).
3. **CLAUDE.md global preenchido** com quem você é, suas empresas, seu ICP base, sua voz e regras gerais. Vá em **Settings → Profile → Personal preferences** e cole. Sem isso, todas as skills entregam genérico.

Se ainda não tem CLAUDE.md, rode `entrevista-negocio` antes de qualquer outra skill. Ela faz 11 perguntas direcionadas e devolve o arquivo pronto pra colar.

### 1. Exercício 1 · Pesquisa de dores

Mapeia dores reais com evidência rastreável (Reclame Aqui, Reddit, reviews, X, fóruns). Saída: 20+ dores com citação, URL, data, plataforma, intensidade, frequência. Salvo como CSV em `PESQUISAS/`.

> **Skill principal:** prompt customizado do workshop (não vem como skill no plugin — é um one-shot direto no chat).
> **Suporte do plugin:** depois de rodar a pesquisa, use `afiar-ideia` pra transformar cada dor em ângulo de mensagem.

### 2. Exercício 2 · Duas landing pages com ângulos de dor diferentes

Encadeia `design-frontend` + `landing-page` + `humanizar-texto` numa única run, gerando 2 páginas com paletas, tipografias e energia diferentes. Cada uma ataca uma dor distinta da pesquisa.

```
Usando a pesquisa em PESQUISAS/, construa DUAS landing pages.
Ancore tudo no ICP, oferta e voz do CLAUDE.md.
Cada página foca em UM ângulo de dor diferente.
Devem ter paletas, design e vibe distintos.

Rode em 3 etapas usando essas skills:
1. Use design-frontend pra montar layout e visual de ambas.
2. Use landing-page pra escrever copy de alta conversão.
3. Use humanizar-texto pra limpar padrões de IA.

Salve ambas como HTML em landing-pages/.
```

### 3. Exercício 2.1 · Identidade visual on-brand

**Etapa 1 (extração):** crie um `design.md` extraindo a identidade visual de uma referência. Caminho rápido: [stitch.google.com](https://stitch.google.com) com prompt simples + URL/screenshots da home. Caminho completo: prompt 03 do workshop direto no Cowork (mais controle).

**Etapa 2 (reconstrução):** prompt 04 do workshop reaplicando 100% dos tokens do `design.md` numa das landings. Mapeamento explícito antes de codar (`headline 48px → token H1 40px`, `botão CTA #1A73E8 → primary-action #FF6B00`, etc.).

> **Suporte do plugin:** `design-frontend` pode reaplicar o `design.md` em qualquer página — é só passar o arquivo no contexto.

### 4. Exercício 3 · Construa sua skill

Use `criar-skill` pra construir uma skill nova do zero, ou `entrevista-skill` pra extrair seu workflow tácito (o que você faz toda semana mas nunca documentou). Hábito recomendado: terminou uma sessão longa que deu certo? Pede pro Claude transformar em skill. Não sai do workshop sem ter criado pelo menos uma.

### 5. Exercício 4 · Pipeline de conteúdo (5 skills em sequência)

O coração do workshop. Skill por vez, mesmo chat:

| Passo | Skill | O que faz |
|---|---|---|
| 1 | `afiar-ideia` | 5 ângulos contrarianos. Você escolhe 1. |
| 2 | `post-longo-x` | Post pronto pra publicar (500-3000 chars), 1 dos 9 padrões. |
| 3 | `humanizar-texto` | Anti-slop: 5 passadas removendo padrões de IA. |
| 4 | `polir-texto` | 10 passadas de edição (zoom in, headline scan, missão, fingerprint, corte final). |
| 5 | `reaproveitar-conteudo` | Variações nativas pra LinkedIn, Instagram, TikTok, YT Shorts. |

**Material de partida:** tweet, post LinkedIn ou rascunho que você gosta. Não começar do zero — você precisa de uma centelha real.

### 6. Exercício 5 · Connectors (MCPs)

Liga apps externos ao Cowork: Excalidraw, Gmail, Calendar, Notion, Asana, Apify. **Customize → Connectors → Browse Connectors**. Exemplo: pega seu post final, pede pro Claude transformar em fluxograma usando o connector do Excalidraw, e ele te entrega o `.excalidraw` pronto pra arrastar no `excalidraw.com`.

> **Suporte do plugin:** as skills do plugin não dependem de connectors. Connectors abrem novas combinações (ex: `auditoria-seo` num site específico via Apify).

### 7. Exercício 6 · Scheduled Tasks

Comando `/schedule` pra agendar tarefas recorrentes. Caso clássico: hook scraper diário às 9h, populando um `hooks-master.md` que você usa como swipe file quando vai escrever. Outros casos: daily briefing 7h (Gmail + Calendar), inbox triage a cada 4h, top posts semanais segunda 9h.

> **Caveat:** hoje (final 2025) scheduled task no Cowork só roda se o computador estiver ligado. Em Claude Code já existe `routines` que roda na nuvem.

### Próximos passos

3 ações concretas pra amanhã de manhã:

1. **Plugin instalado e validado** (já tá feito, parabéns).
2. **Um projeto vivo no disco** — escolha 1 cliente real, crie projeto no Cowork, preencha project instructions, rode o exercício 1.
3. **1 scheduled task no ar** — comece pelo hook scraper. Acorda amanhã com output pronto.

Não tente fazer os 6 exercícios de uma vez. Espalha por 1 semana. Cada exercício concluído de verdade vale mais que 6 pela metade.

---

## Catálogo das 21 skills

### Pesquisa e fundação

| Skill | O que faz |
|---|---|
| `entrevista-negocio` | Conduz entrevista de 11 perguntas extraindo voz, ICP, oferta, prova social, posicionamento. Devolve `CLAUDE.md` pronto pra colar em **Settings → Global Instructions**. |
| `pesquisa-keywords` | Expande seed keywords em 6 ângulos, organiza em clusters de tópico, devolve calendário de conteúdo escorado por oportunidade vs receita. Sem ferramenta paga. |
| `auditoria-seo` | Auditoria on-page (título, meta, H1, canonical, social cards, schema, alt text, links internos) usando só ferramentas nativas. Devolve relatório A-F com fixes priorizados P0-P3. |

### Ideação e estratégia

| Skill | O que faz |
|---|---|
| `afiar-ideia` | Pega ideia genérica, devolve 3-5 ângulos negando suposições do público. Murray Davis + 14 técnicas de novidade. Cada ângulo passa em 3 testes (surpresa, compartilhamento, "e daí"). |
| `hooks-virais-x` | 3-5 hooks pra X/LinkedIn, baseados em swipefile com 140+ padrões de criadores que batem 100k+ views (Greg Isenberg, Dan Koe, Nikita Bier, Karpathy, Pieter Levels, etc.). |
| `arquitetar-oferta` | Constrói oferta completa: shell de tiers, mapa Promessa/Caminho/Preço/Por que agora, arco protagonista, ritmo "90 dias de oferta". |

### Escrita por canal

| Skill | O que faz |
|---|---|
| `post-longo-x` | Post pronto pro X (500-3000 chars), 1 dos 9 padrões estruturais validados em posts com 100k+ views. Anti-slop interno como passada final. |
| `escrever-linkedin` | LinkedIn nativo (1200-1500 chars), tom profissional sem ficar robótico. Lê CLAUDE.md pra voz/ICP. |
| `escrever-newsletter` | Newsletter completa: hook, building blocks, momentum, CTA. Estrutura que o leitor encaminha. |
| `escrever-artigo` | Artigo longo pra X/blog: hook, passos numerados, copy-paste blocks, CTAs inline, hard closer. |
| `escrever-copy` | Direct response: VSL, sales page, anúncio, hero section, CTA. Schwartz + Ogilvy + Sugarman. Lê CLAUDE.md, roda anti-slop. |
| `sequencia-email` | Sequência completa (boas-vindas, nutrição, lançamento, reativação, onboarding). Subject + preview + timing + copy. |

### Páginas e produtos

| Skill | O que faz |
|---|---|
| `landing-page` | Sales page de alta conversão usando framework de 5 partes. Escreve em ordem estratégica (story primeiro, headline última). |
| `lead-magnet` | 3-5 conceitos de lead magnet (ângulo, formato, caminho pra oferta paga). Quando pedido, escreve o conteúdo dentro. |
| `design-frontend` | HTML/CSS/JS pra qualquer página, mobile-first, sem libs externas. Foge da estética genérica de IA (gradientes roxos, Inter, cards arredondados em fundo branco). |

### Edição e qualidade

| Skill | O que faz |
|---|---|
| `polir-texto` | 9 passadas sequenciais (zoom in, headline scan, cap de 3 ideias, sweep de confiança, teste da barra, missão, audiência, fingerprint, corte final) + anti-slop final. Até 30% menos gordura. |
| `humanizar-texto` | 5 passadas anti-slop (estrutura, frases, verbos, formatação, conteúdo). Remove palavras de hype, frases vazias, travessões mal usados, clichês de IA. |
| `conselho-llm` | "Conselho consultivo": 5 modelos analisam decisão independentemente, peer-review anônimo, síntese final. Pra textos/decisões de alto risco. |

### Distribuição

| Skill | O que faz |
|---|---|
| `reaproveitar-conteudo` | Pega 1 peça-fonte, devolve variantes nativas pra LinkedIn, X, Instagram, TikTok, YT Shorts. Não é cross-posting — é construído do zero pra cada plataforma. |

### Meta (criar mais skills)

| Skill | O que faz |
|---|---|
| `criar-skill` | Cria skills novas, edita existentes, mede performance com evals. Pra quando o padrão se repetiu 3+ vezes e vale codificar. |
| `entrevista-skill` | Entrevista pra extrair conhecimento tácito do seu workflow antes de virar skill. Output: SKILL.md production-ready. |

---

## Premissas

Todas as skills assumem que você tem um `CLAUDE.md` carregando voz, ICP e contexto de negócio. Sem isso, elas vão pedir os dados antes de continuar.

Se ainda não tem o arquivo, comece por `entrevista-negocio` que conduz a entrevista e devolve o `CLAUDE.md` pronto pra colar em **Settings → Profile → Personal preferences** (ou em **Project custom instructions** se for específico de um cliente).

**Hierarquia de contexto** (regra de ouro: global enxuto, project gordo):

```
1. Global instructions (CLAUDE.md global)
   └─ Settings → Profile → Personal preferences
   └─ ALTO nível: quem você é, negócios, ICP base

2. Project custom instructions
   └─ Por projeto: cliente, marca, tone of voice, regras

3. Files na pasta do projeto
   └─ Tudo que Claude cria fica como contexto pros próximos prompts
```

Não concentre tudo no global — confunde. 1 projeto por cliente.

---

## Regras anti-slop herdadas

Toda skill aplica a passada anti-slop como gate final. Lista de banidos:

- **Palavras de hype**: alavancar, sinergia, robusto, holístico, transformador, revolucionário, disruptivo, jornada, ecossistema, supercharge, leverage, level up, deep dive, unpack
- **Frases vazias**: "no mundo de hoje", "vamos explorar", "é importante notar", "imagine que…"
- **Construções clichê**: "não é X, é Y", "sem X. Sem Y. Apenas Z.", "se você é sério em relação a"
- **Travessão usado como vírgula** (zero tolerância)
- **Confete de emoji decorativo**
- **Estudos de caso fictícios** com nomes inventados (Sarah Chen, Marcus Johnson, etc.)
- **Regra de três** ("rápido, fácil, eficiente")
- **Ponto-e-vírgula**

Se seu texto precisa de uma dessas por motivo legítimo, edite manualmente depois da passada da skill.

---

## Contribuir / customizar

### Editar uma skill existente

```bash
cd ~/.claude/plugins/marketing-skills/plugins/marketing-skills/skills/<nome-da-skill>
# editar SKILL.md
/reload-plugins   # no Claude Code
```

> Caminho parece "duplicado" porque o repo é um **marketplace** (primeira pasta `marketing-skills`) que contém o **plugin** com mesmo nome (segunda pasta) — é o padrão oficial da Anthropic e te deixa adicionar outros plugins no mesmo repo depois.

Skills são editáveis sem medo — só quebram se outras skills as chamarem por nome (as desse plugin não chamam).

### Criar uma skill nova

Use a meta-skill:

```
Use criar-skill pra construir uma skill nova chamada "anuncio-meta" que
escreva anúncios pra Meta Ads no formato curto/médio/longo, lendo voz e
ICP do CLAUDE.md.
```

Ou se você ainda nem documentou seu workflow:

```
Use entrevista-skill. Quero codificar meu processo de auditar
landing pages de cliente antes de propor um redesign.
```

### Compartilhar suas mudanças

Faça fork desse repo, ajuste o `marketplace.json` e o `plugin.json` com seus dados, e use seu próprio fork como marketplace no Cowork. Cada pessoa do time aponta pra mesma URL e recebe atualizações ao rodar `/plugin marketplace update`.

---

## Recursos do workshop

- **Slides do workshop**: https://vibemakers.com.br/apresentacao-claudemarketing
- **Workbook completo (módulos + exercícios)**: https://vibemakers.com.br/claudemarketing
- **Workshop original do Ole Lehmann (referência)**: https://cute-tin-f85.notion.site/Claude-Cowork-Marketing-OS-34b4313995e281a5885cc35ebd4ab104
- **Doc oficial Anthropic sobre plugins**: https://docs.claude.com/en/docs/claude-code/plugins
- **Doc oficial sobre marketplaces**: https://docs.claude.com/en/docs/claude-code/plugin-marketplaces

---

## Licença

MIT. Veja [LICENSE](LICENSE). Copyright Hugo Doria.

Várias skills foram derivadas, traduzidas ou adaptadas do plugin original do [Ole Lehmann](https://github.com/olelehmann1337) — créditos a ele pelo trabalho de pesquisa e empacotamento original. Esta versão foca em PT-BR, contexto brasileiro, e integração com o curso da Vibe Makers.
