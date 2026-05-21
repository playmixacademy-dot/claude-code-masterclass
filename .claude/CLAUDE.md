# Claude Code & Cursor Masterclass — Projeto de Slides

## O que é este projeto

Apresentação HTML standalone para aula ao vivo de 90 minutos via Zoom sobre Claude Code e Cursor, para alunos do Maker Pro 2.0 (videomakers, não-devs). A prática ao vivo constrói o site da PLAYMIX (produtora audiovisual).

## Link de produção

https://claude-code-masterclass-tan.vercel.app

## Repositório

https://github.com/playmixacademy-dot/claude-code-masterclass

## Estrutura

```
index.html          — arquivo único com toda a apresentação (CSS + HTML + JS)
img/                — imagens usadas nos slides
  claude-code-in-terminal.png  — screenshot do Claude Code (site oficial Anthropic)
  cursor-hero.png              — screenshot do Cursor (site oficial)
  github-repo.png              — print real do repo no GitHub
  vercel-logo.svg              — logo SVG oficial
  supabase-logo.svg            — logo SVG oficial
  github-logo.svg              — logo SVG oficial
  cloudflare-logo.svg          — logo SVG oficial
  og.png                       — imagem Open Graph para compartilhamento
vercel.json         — headers de cache (criado pelo @devops)
```

## Estrutura dos slides (36 slides, 2 blocos)

### Bloco 1 — ENTENDER (slides 1-18)
1. Title (dark) — "Claude Code & Cursor"
2. Agenda — 2 blocos: Entender + Prática e Instalação
3. Section Break: ENTENDER
4. O que é uma LLM — Claude, GPT, Gemini (a família)
5. Claude, Cowork e Code — 3 produtos da Anthropic
6. Statement — "Você descreve. A IA constrói."
7. Claude Code — o que é (com imagem do terminal)
8. O que o Claude Code faz — capacidades para videomakers
9. Commit, Push e Deploy — como o código chega na internet
10. GitHub — o que é repositório (com print real)
11. CLAUDE.md e Memória — arquivo de regras + memória automática
12. Cursor — o que é, 3 níveis: Tab, Cmd+K, Modo autônomo (com imagem)
13. Claude Code + Cursor juntos — como funcionam combinados
14. LLM · Skill · Agente · Squad — 4 conceitos rápidos (analogia do cérebro/mãos)
15. AIOX Agents — @dev, @architect, @qa, @pm, @analyst, @devops
16. 16 Squads — grid completo com todas as squads operacionais
17. Tecnologias — HTML/CSS/JS, Next.js, React Native, Swift/Kotlin, Python, Flutter
18. Ecossistema — Vercel, Supabase, GitHub, Cloudflare (com logos SVG)

### Bloco 2 — PRÁTICA E INSTALAÇÃO (slides 19-33)
19. Section Break: PRÁTICA E INSTALAÇÃO
20. O projeto PLAYMIX — portfólio, orçamento, serviços
21. O prompt — prompt completo para Next.js com detalhes
22. Como pedir bem — Funciona vs Não funciona
23. MÃOS À OBRA (dark) — screenshare cue
24. Como ver seu site — npm run dev + localhost:3000
25. Publicar online — npx vercel
26. O que você vai precisar — Mac/Win, Claude Pro $20/mês, Node.js, Cursor
27. O que é um terminal — Mac: Cmd+Espaço, Windows: PowerShell
28. Como instalar Claude Code — curl (Mac) e irm (Windows)
29. O que acontece depois — login, cursor piscando, pronto
30. Primeiro uso — mkdir, cd, claude
31. Comandos principais — claude, claude -c, /help, exit
32. Instalando o Cursor — cursor.com, download, conta, Cmd+L
33. Dúvidas até aqui?

### Encerramento (slides 34-36)
34. Recap — 2 cards: Entendeu + Praticou e Instalou
35. Próximos passos
36. Closing (dark) — "Agora é com vocês."

## Decisões tomadas durante o desenvolvimento

### Visual
- Paleta: fundo branco (#FAFAFA) + laranja (#E8590C) como accent + degradê warm
- O usuário rejeitou 3 versões antes de aprovar (v1 dark puro, v2 gradiente roxo, v3 dark SOP)
- v4 (branco + laranja) foi aprovada e refinada
- Slides Title e Closing são dark (gradiente #1A1A1A → #57534E)
- Section breaks usam gradiente warm (creme → pêssego → laranja)
- Cards com borda e sombra sutil, fundo branco
- Ícones SVG inline (sem emojis genéricos)
- Logos SVG oficiais para Vercel, Supabase, GitHub, Cloudflare
- Imagens reais: Claude Code (site Anthropic), Cursor (site oficial), GitHub (print do repo)

### Conteúdo
- Público: videomakers que NUNCA programaram — linguagem 100% leiga
- Jargão técnico traduzido: deploy→publicar, commit→salvar versão, hero→tela inicial, footer→rodapé, mobile-first→funcione no celular, refatorar→melhorar o que já existe
- Analogia LLM/Skill/Agente/Squad aprovada pelo usuário: "LLM é o cérebro. Skill é dar um manual. Agente é quando ganha mãos. Squad é o time."
- Prompt Next.js detalhado com cores exatas, seções numeradas, dropdown no formulário
- Squads: todas as 16 mostradas sem marcar nenhuma como "em desenvolvimento"
- Preços confirmados: Claude Pro $20/mês (inclui Code+Cowork), Cursor Hobby gratuito
- Comandos de instalação verificados na doc oficial: curl (Mac), irm (Windows)
- Node.js NÃO é necessário pro instalador nativo do Claude Code (confirmado na doc)
- Node.js É necessário pro Next.js (adicionado nos pré-requisitos)
- "Conwork" é o nome correto → "Cowork" (confirmado no site Anthropic)
- Windsurf é da Cognition AI (não foi "comprada" — é a empresa criadora)

### Estrutura
- Começou com 4 blocos → reorganizado para 2 blocos por pedido do usuário
- Bloco 1: toda a teoria primeiro (entender)
- Bloco 2: prática ANTES da instalação (impressionar primeiro, ensinar depois)
- Informações "internas" removidas dos slides (tempo, Zoom, quantidade de minutos)
- Agenda e Recap espelham os 2 blocos

### Revisões realizadas
1. @content-architect — revisou textos, jargão, sequência
2. @analyst (Alex) — pesquisa factual: Cowork confirmado, preços, Windsurf/Cognition AI
3. @qa-inspector (Quinn) — 2 rodadas: erros factuais, acentos, footers, killer items
4. @ux-design-expert (Uma) — 30 problemas de clareza para leigos, todos corrigidos
5. Acentos — script automatizado verificou 100+ padrões, verificação final = 0 erros
6. Comandos técnicos — 15 comandos validados contra doc oficial
7. Segurança — review completo: sem scripts externos, sem tokens, sem eval

### Problemas resolvidos
- Formatação: conteúdo saía do viewport → centralização vertical com justify-content:center
- Watermark sobrepondo texto → movido pro canto, opacidade reduzida
- Tipografia grande demais → clamp() reduzido para telas menores
- Footer numbers errados → renumerados por script
- WhatsApp OG cache → renomeado imagem, adicionado timestamp, vercel.json com headers curtos
- Screenshot da área de trabalho no slide terminal → substituído por terminal CSS

## Stack técnica

- HTML standalone (sem framework, sem build)
- CSS com custom properties (var(--...)) seguindo SOP-SLIDES-003
- Tipografia responsiva com clamp()
- Animações CSS: fadeUp, fadeIn, scaleIn, growWidth, growHeight
- JavaScript vanilla para navegação (setas, espaço, clique, touch)
- Fontes: Inter (Google Fonts) + JetBrains Mono
- Deploy: Vercel (auto-deploy via GitHub)
- Imagens: PNG screenshots + SVG logos

## Squad que criou esta apresentação

Squad: slides-creator (instalado de /Users/marcelogiglio/Downloads/slides-creator → squads/slides-creator/)

Agentes envolvidos:
- @slide-chief — orquestrador do pipeline
- @content-architect — revisão de conteúdo
- @qa-inspector — auditoria de qualidade
- @ux-design-expert — análise de clareza para leigos
- @analyst — pesquisa factual
- @devops — deploy, git push, cache headers
- @dev — fixes técnicos
- @aiox-master — orquestração geral
