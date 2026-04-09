# Identidade Visual — Comunidade Coda

> **Tagline:** "Coda — Comunidade de Builders"

---

## 🎨 Paleta de Cores

### Cores Principais (Brand)

| Token | Hex | Uso |
|---|---|---|
| `mgt-orange` | `#ff5000` | **Cor principal da marca** — CTAs, destaques, badges admin |
| `mgt-neon` (dark) | `#c8f55a` | Neon verde-lima — acentos, destaques secundários |
| `mgt-neon` (light) | `#749e15` | Versão mais escura do neon para modo claro |

### Favicon

> Fundo `#E8612A` (laranja), com ícone de terminal `>_` em `#0e0e0e`, bordas arredondadas (`rx=7`)

### Dark Mode (`.dark`) — **Modo padrão**

| Token | Hex | Uso |
|---|---|---|
| `--bg-primary` | `#0e0e0e` | Background principal |
| `--bg-secondary` | `#1a1a1a` | Cards, sidebar |
| `--bg-tertiary` | `#2a2a2a` | Bordas, separadores |
| `--text-primary` | `#f5f5f5` | Texto principal |
| `--grid-color` | `rgba(255,255,255,0.02)` | Grid do background pixel |

### Light Mode (`:root`)

| Token | Hex | Uso |
|---|---|---|
| `--bg-primary` | `#f5f5f5` | Background principal |
| `--bg-secondary` | `#e5e5e5` | Cards, sidebar |
| `--bg-tertiary` | `#d4d4d4` | Bordas, separadores |
| `--text-primary` | `#121212` | Texto principal |
| `--grid-color` | `rgba(0,0,0,0.04)` | Grid do background pixel |

### Escala de Cinzas (invertida entre temas)

| Token | Dark | Light |
|---|---|---|
| `gray-50` | `#f9fafb` | `#030712` |
| `gray-100` | `#f3f4f6` | `#111827` |
| `gray-200` | `#e5e7eb` | `#1f2937` |
| `gray-300` | `#d1d5db` | `#4b5563` |
| `gray-400` | `#9ca3af` | `#6b7280` |
| `gray-500` | `#6b7280` | `#9ca3af` |
| `gray-600` | `#4b5563` | `#d1d5db` |
| `gray-700` | `#374151` | `#e5e7eb` |
| `gray-800` | `#1f2937` | `#f3f4f6` |
| `gray-900` | `#111827` | `#f9fafb` |
| `gray-950` | `#030712` | `#ffffff` |

---

## 🔤 Tipografia

| Token | Font Family | Uso |
|---|---|---|
| `--font-sans` | **Inter** | Corpo de texto padrão |
| `--font-display` | **Space Grotesk** | Headings (`h1`-`h6`) |
| `--font-pixel` | **Pixelify Sans** | Texto estilo pixel art |
| `--font-clean` | **Montserrat** | Texto limpo/moderno |
| *(adicional)* | **Poppins** | Carregada mas sem token dedicado |

### Letter-spacing dos Headings

| Tag | Spacing |
|---|---|
| `h1` | `-0.04em` |
| `h2` | `-0.03em` |
| `h3` | `-0.02em` |

---

## 🕹️ Efeitos Visuais

### Pixel Corners (`.pixel-corners`)
Bordas recortadas estilo pixel-art usando `clip-path: polygon(...)` com chanfros de `4px`. Usado em cards, botões e containers.

### Pixel Border (`.pixel-border`)
Sombra interna que simula profundidade 8-bit:
```css
box-shadow: 
  inset 0 4px 0 0 rgba(255,255,255,0.1),
  inset 0 -4px 0 0 rgba(0,0,0,0.3);
```

### Glitch / Chromatic Aberration
- `.text-glitch` — texto com aberração cromática forte (2px offset em Cyan, Magenta, Amarelo)
- `.text-glitch-sm` — versão menor (1px)

### Pixel Background Grid (`.pixel-bg`)
Grid sutil de 60×60px com linhas de 1px usando `--grid-color`.

### CTA Button Shadow (`.btn-cta-shadow`)
Sombra profunda com inner highlight branco, elevação no hover (`translateY(-1px)`).

---

## 🎬 Animações

| Classe | Direção | Descrição |
|---|---|---|
| `.float-left` | ← ↑ | Move -120px X, -40px Y |
| `.float-right` | → ↑ | Move +120px X, -60px Y |
| `.float-up` | → ↑ | Move +30px X, -100px Y |
| `.float-diag` | ← ↑ | Move -60px X, -80px Y |

Todas usam fade-in no 10% e fade-out no 90% (opacidade).

### Outras
- `.section-dot` — Pulsação do dot em section tags (2s ease-in-out)
- `@keyframes marquee` — Scroll horizontal infinito para carrossel de "Founding Members"

---

## 🏅 Sistema de Roles (Badges)

| Role | Label | Emoji | Cor do texto | Cor da borda |
|---|---|---|---|---|
| `ceo` | CEO | 👑 | `yellow-400` | `yellow-500/40` |
| `founder` | Founder | 🚀 | `purple-400` | `purple-500/40` |
| `admin` | Admin | 🛡️ | `mgt-orange` | `mgt-orange/40` |
| `moderator` | Moderador | ⚔️ | `blue-400` | `blue-500/40` |
| `member` | Membro | 👤 | `gray-400` | `gray-500/20` |

Roles privilegiados (acesso admin): `ceo`, `admin`

---

## 📁 Assets Estáticos (`/public/`)

| Arquivo | Descrição |
|---|---|
| `favicon.svg` | Ícone de terminal `>_` em fundo laranja |
| `comunidade_coda.png` | Logo/imagem da comunidade |
| `Google-Stitch-Logo.png` | Logo Google Stitch |
| `antigravity-icon__one-color.png` | Ícone Antigravity |
| `mockup notebook coda.png` | Mockup da plataforma em notebook |
| `daniel_lima.png` / `enzo_segatto.png` / `foto_marcelo.png` / `foto_naval.png` | Fotos de membros/founders |
| `logo_tech_stacks.png` | Logo do projeto (raiz) |

---

## 🛠️ Stack de Estilização

- **Tailwind CSS v4** — via `@import "tailwindcss"` (sem config file separado, tokens via `@theme`)
- **CSS Variables** — Tema dinâmico dark/light via variáveis CSS
- **Google Fonts** — Inter, Space Grotesk, Pixelify Sans, Montserrat, Poppins

---

## 📐 Resumo da Identidade

> **Conceito:** Terminal hacker meets pixel-art gaming community
> 
> - **Dark-first** com suporte a light mode
> - **Laranja `#ff5000`** como cor de destaque principal
> - **Neon verde `#c8f55a`** como cor secundária
> - **Cantos pixelados** em cards e botões (`pixel-corners`)
> - **Efeito glitch/chromatic aberration** em títulos
> - **Grid sutil de pixels** no background
> - **Tipografia tight** nos headings (letter-spacing negativo)
> - **Badges coloridos por role** com emoji
