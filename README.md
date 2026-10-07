# 📦 Estudo Prático de HTML e CSS: Box Model & Flexbox

Projeto prático desenvolvido para demonstrar em profundidade a aplicação do **CSS Box Model** e propriedades avançadas de **CSS Flexbox**, com foco em estruturação semântica, estilização externa e responsividade moderna.

---

## 🚀 Tecnologias Utilizadas

- **HTML5**: Estruturação semântica de componentes (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`).
- **CSS3 (Vanilla)**:
  - Estilização externa via tag `<link rel="stylesheet" href="style.css">`.
  - Configuração granular de Box Model (*Content, Padding, Border, Margin*).
  - 20+ propriedades e declarações de Flexbox.
  - Design moderno com Glassmorphism, paleta escura (Dark Theme) e Media Queries responsivas.
- **Google Fonts**: Tipografia *Plus Jakarta Sans*.

---

## 📂 Estrutura de Arquivos

```text
estudo_html_css/
├── index.html        # Estrutura HTML contendo os 20 elementos semânticos
├── style.css         # Folha de estilos externa com Box Model e Flexbox
└── README.md         # Documentação completa do projeto
```

---

## 🎯 Requisitos Implementados

### 1. Inclusão Externa de CSS
O arquivo `style.css` é carregado de forma modular e desacoplada no `<head>` do `index.html`:
```html
<link rel="stylesheet" href="style.css">
```

---

### 2. Box Model nos 20 Elementos
Cada um dos 20 elementos (`#el-1` até `#el-20`) possui regras explícitas para as 4 camadas do CSS Box Model:

| ID | Elemento / Componente | Content (Dimensões/Tipo) | Padding | Border | Margin |
|---|---|---|---|---|---|
| `#el-1` | `header.app-header` | `width: 100%; min-height: 80px` | `18px 36px` | `2px solid border-color` (inferior) | `0 0 24px 0` |
| `#el-2` | `div.logo-box` | `width: auto; height: 48px` | `6px 14px` | `1px solid border-color` | `0 12px 0 0` |
| `#el-3` | `nav.main-nav` | `width: auto; min-height: 44px` | `4px 8px` | `1px solid rgba(255,255,255,0.05)` | `0` |
| `#el-4` | `a.nav-item (Início)` | `display: inline-block` | `8px 16px` | `1px solid transparent` | `0 4px` |
| `#el-5` | `a.nav-item (Elementos)` | `display: inline-block` | `8px 16px` | `1px solid transparent` | `0 4px` |
| `#el-6` | `a.nav-item (Métricas)` | `display: inline-block` | `8px 16px` | `1px solid transparent` | `0 4px` |
| `#el-7` | `a.nav-item-cta (Explorar)` | `display: inline-block` | `8px 20px` | `1px solid var(--primary)` | `0 0 0 8px` |
| `#el-8` | `div.hero-card` | `width: 100%; min-width: 320px` | `40px` | `1px solid border-color` | `0 0 16px 0` |
| `#el-9` | `span.badge` | `display: inline-flex` | `6px 14px` | `1px solid rgba(6,182,212,0.3)` | `0 0 8px 0` |
| `#el-10` | `h1.hero-title` | `width: 100%` | `4px 0 4px 12px` | `4px solid var(--primary)` (lateral) | `4px 0 12px 0` |
| `#el-11` | `p.hero-description` | `max-width: 680px` | `12px 16px` | `1px dashed rgba(255,255,255,0.1)` | `0 0 16px 0` |
| `#el-12` | `div.hero-actions` | `width: 100%` | `10px 0` | `1px solid rgba(255,255,255,0.05)` (topo) | `8px 0 0 0` |
| `#el-13` | `button.btn-primary` | `height: 46px` | `0 24px` | `1px solid var(--primary)` | `0 4px 0 0` |
| `#el-14` | `button.btn-outline` | `height: 46px` | `0 24px` | `1px solid border-color` | `0` |
| `#el-15` | `aside.hero-sidebar` | `width: 100%` | `24px` | `1px solid border-color` | `0` |
| `#el-16` | `div.status-widget` | `width: 100%` | `16px` | `1px solid rgba(16,185,129,0.3)` | `0 0 8px 0` |
| `#el-17` | `div.mini-card` | `width: 100%` | `16px` | `3px solid var(--accent)` (lateral) | `6px 0 0 0` |
| `#el-18` | `article.card-highlight` | `min-width: 260px; min-height: 220px` | `24px` | `2px solid var(--border-accent)` | `8px` |
| `#el-19` | `article.card-align-self` | `min-width: 260px; min-height: 220px` | `24px` | `1px solid border-color` | `8px` |
| `#el-20` | `article.card-order` | `min-width: 260px; min-height: 220px` | `24px` | `1px dashed var(--accent)` | `8px` |

---

### 3. Propriedades de Flexbox Utilizadas

O projeto aplica de forma prática mais de 20 declarações/propriedades de Flexbox:

1. `display: flex` — Ativação de contexto flex em múltiplos containers.
2. `display: inline-flex` — Contexto flex inline para botões, badges e logo.
3. `flex-direction: row` — Orientação horizontal padrão.
4. `flex-direction: column` — Orientação vertical para cartões e layout body/mobile.
5. `flex-wrap: wrap` — Quebra de linha responsiva dos elementos.
6. `flex-flow: row wrap` — Sintaxe abreviada para direção e quebra simultâneas.
7. `justify-content: space-between` — Distribuição com espaçamento uniforme nas extremidades.
8. `justify-content: flex-start` — Alinhamento no início do eixo principal.
9. `justify-content: flex-end` — Alinhamento no fim do eixo principal (menu).
10. `justify-content: center` — Centralização de conteúdo e botões.
11. `justify-content: space-around` — Espaçamento simétrico em torno dos itens da sidebar.
12. `justify-content: space-evenly` — Espaçamento estritamente igual entre os cartões da galeria.
13. `align-items: center` — Centralização no eixo transversal.
14. `align-items: flex-start` — Alinhamento ao topo no eixo transversal.
15. `align-items: stretch` — Esticamento uniforme dos cards e painéis laterais.
16. `align-content: space-between` — Distribuição entre múltiplas linhas flex.
17. `gap` — Espaçamento nativo e moderno entre flex items.
18. `column-gap` — Espaçamento exclusivo entre colunas flex.
19. `row-gap` — Espaçamento exclusivo entre linhas flex.
20. `flex-grow` — Fator de crescimento dinâmico de elementos (`flex-grow: 1` e `flex-grow: 2`).
21. `flex-shrink` — Controle de encolhimento para preservar dimensões mínimas (`flex-shrink: 0` e `flex-shrink: 1`).
22. `flex-basis` — Dimensão base inicial dos itens flex antes da distribuição de espaço.
23. `flex (shorthand)` — Combinação de `grow`, `shrink` e `basis` (ex: `flex: 2 1 600px`).
24. `align-self: flex-end` — Alinhamento transversal customizado individual no `#el-19`.
25. `align-self: center` — Alinhamento transversal customizado individual no `#el-20`.
26. `align-self: stretch` — Adaptação de largura total no breakpoint responsivo.
27. `order: -1` — Reordenação visual do `#el-20` sem modificar o HTML.

---

## 📱 Responsividade (Media Queries)

A página se adapta perfeitamente a telas menores (`max-width: 768px`):
- O cabeçalho reorganiza a logo e a navegação em coluna (`flex-direction: column`).
- Ações e botões expandem para preencher a largura disponível (`align-items: stretch` e `width: 100%`).
- As propriedades de alinhamento individual (`align-self`) são reajustadas para preenchimento fluído.

---

## 💻 Como Visualizar o Projeto

1. Clone ou baixe este repositório.
2. Abra o arquivo `index.html` em qualquer navegador moderno (Chrome, Edge, Firefox, Safari).
3. Redimensione a janela ou utilize as Ferramentas de Desenvolvedor (`F12`) para inspecionar os elementos e testar os breakpoints de responsividade.
