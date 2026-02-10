# Frontend Technical Test — V4 Company  
**HTML Email + Landing Page**

🇧🇷 [Versão em Português](#-versão-em-português)  
🇺🇸 [English Version](#-english-version)

# 🇧🇷 Versão em Português

Este repositório contém minha solução para o teste técnico de Frontend da V4 Company. O desafio envolve dois cenários diferentes: **HTML Email marketing** e **Landing Page estática**, ambos implementados sem frameworks e com foco em boas práticas de mercado.

---

# 📂 Estrutura do Projeto


```
.
├── email/
│   ├── assets/
│   │   ├── BANNER.png
│   │   └── LOGO.png
│   └── index.html
│
├── lp/
    ├── assets/
    │   └── BANNER.png
│   ├── index.html
│   └── style.css
│
└── README.md
```

---

# Como testar localmente

## Email
1. Acesse `/email`
2. Abra `index.html` no navegador (validação estrutural)

Para teste real:
- Mailtrap / SendGrid / Mailchimp (modo HTML)
- Envio para Gmail, Outlook e Apple Mail
- Testes em desktop, mobile e dark mode

---

## Landing Page
1. Acesse `/lp`
2. Abra `index.html` no navegador

---

---

# Parte 1 — HTML Email

## Objetivo

Construir um email marketing compatível com múltiplos clients, considerando limitações reais de renderização, suporte de CSS e responsividade.

---

## Estrutura

- Layout 100% baseado em **tabelas**
- Sem uso de divs estruturais
- Container principal com largura fixa de **600px**
- Blocos separados:
  - Header
  - Hero
  - Benefícios
  - Prova social
  - Agenda
  - CTA final
  - Footer

Esse modelo garante maior compatibilidade com Gmail, Outlook e Apple Mail.

---

## Estilos

- CSS principal aplicado **inline**
- `<style>` no head usado apenas para:
  - reset básico
  - media queries simples
  - ajustes de dark mode
- Evitado CSS moderno com baixo suporte

---

## Responsividade

- Media query para telas menores:
  - container 100%
  - colunas empilhadas
  - headline reduzida
- Fallback legível mesmo sem suporte a media query

---

## Botões (CTA)

- Implementados como **bulletproof buttons**
- Estrutura:
  - table + td com bgcolor + link estilizado
- Mantém aparência de botão mesmo com suporte CSS parcial

---

## Preheader

Implementado com técnica de ocultação compatível com clients:

- display none
- tamanho mínimo de fonte
- overflow hidden
- opacity zero

Garante preview correto na inbox.

---

## Acessibilidade — Email

- Texto real (não imagem com texto)
- Alt nas imagens
- Contraste adequado
- Tabelas de layout com role="presentation"
- Tipografia segura (Arial / sans-serif)

---

## Dark Mode — Email

- Uso de prefers-color-scheme
- Ajustes de fundo e contraste
- Cores críticas definidas inline
- Abordagem defensiva (cada client aplica dark mode de forma diferente)

---

## Compatibilidade considerada

### Outlook Desktop
- Suporte limitado a background-image e CSS avançado
- Hero com fallback de cor sólida

### Gmail
- Pode sobrescrever cores de links
- Links importantes com cor inline

---

## CSS evitado no Email

- Flexbox
- Grid
- Position
- CSS externo
- Variáveis CSS
- Seletores complexos

---

## Melhorias futuras — Email

- Versão alternativa de hero sem imagem
- VML fallback para background no Outlook
- Mais variações de CTA
- Ajustes finos por client
- Tokens de cor e espaçamento

---

---

# Parte 2 — Landing Page

## Objetivo

Criar uma landing page estática com layout moderno, semântico, responsivo e acessível, sem uso de frameworks ou JavaScript.

---

## Estrutura HTML

- Uso de HTML semântico:
  - header
  - main
  - section
  - article
  - footer
- Hierarquia correta de headings
- Seções implementadas:
  - Hero
  - Como funciona (3 passos)
  - Planos (3 cards)

---

## CSS

- Arquivo separado (`style.css`)
- Sem frameworks
- Organização por blocos de seção
- Classes consistentes
- Mobile-first

---

## Responsividade — LP

- Abordagem mobile-first
- Grids com breakpoints progressivos
- Cards reorganizam em colunas conforme largura
- Hero com ajuste de tipografia por tela

---

## Acessibilidade — LP

- Contraste adequado
- Focus visível
- Headings hierárquicos
- aria-label no plano recomendado
- CTAs com texto claro

---

## Layout e UI

- Hero com overlay para contraste
- Cards com hover e elevação
- Plano recomendado com destaque visual
- Botões com estados hover, active e focus
- Tipografia segura e legível

---

## Melhorias futuras — LP

- Tokens de design (cores, radius, spacing)
- Sistema de utilitários CSS
- Seção FAQ com details/summary
- Mais variações visuais entre blocos
- Ajustes finos de acessibilidade

---

# Considerações Finais

A solução prioriza:

- Compatibilidade real no HTML Email
- Estrutura table-based correta
- CSS inline para email
- Semântica e responsividade na Landing Page
- Acessibilidade básica aplicada
- Código organizado e legível

Seguindo padrões utilizados em ambientes reais de produção.

# 🇺🇸 English Version

This repository contains my solution for the **V4 Company Frontend Technical Test**.  
The challenge includes two different scenarios: **HTML marketing email** and a **static Landing Page**, both implemented without frameworks and focused on real-world best practices.

---

# 📂 Project Structure

```
.
├── email/
│   ├── assets/
│   │   ├── BANNER.png
│   │   └── LOGO.png
│   └── index.html
│
├── lp/
    ├── assets/
    │   └── BANNER.png
│   ├── index.html
│   └── style.css
│
└── README.md
```


---

# How to Test Locally

## Email

1. Open `/email`
2. Open `index.html` in your browser (structure validation)

For real-world testing:

- Mailtrap / SendGrid / Mailchimp (HTML mode)
- Send to Gmail, Outlook, and Apple Mail
- Test on desktop, mobile, and dark mode

---

## Landing Page

1. Open `/lp`
2. Open `index.html` in your browser

---

---

# Part 1 — HTML Email

## Goal

Build a marketing email compatible with multiple email clients, considering real rendering limitations, CSS support constraints, and responsiveness.

---

## Structure

- 100% **table-based layout**
- No structural div-based layout
- Main container with fixed **600px width**
- Sections separated into blocks:
  - Header
  - Hero
  - Benefits
  - Social proof
  - Agenda
  - Final CTA
  - Footer

This structure ensures better compatibility with Gmail, Outlook, and Apple Mail.

---

## Styles

- Main CSS applied **inline**
- `<style>` in the head used only for:
  - basic reset
  - simple media queries
  - dark mode adjustments
- Modern CSS with low support was intentionally avoided

---

## Responsiveness

- Media query for small screens:
  - container becomes 100%
  - columns stack vertically
  - headline font size reduced
- Content remains readable even without media query support

---

## Buttons (CTA)

- Implemented as **bulletproof buttons**
- Structure:
  - table + td with bgcolor + styled link
- Preserves button appearance even with partial CSS support

---

## Preheader

Implemented using client-safe hidden text technique:

- display none
- minimal font size
- overflow hidden
- zero opacity

Ensures proper inbox preview text.

---

## Accessibility — Email

- Real text (not text inside images)
- Image alt attributes
- Proper contrast
- Layout tables with `role="presentation"`
- Safe typography (Arial / sans-serif)

---

## Dark Mode — Email

- Uses prefers-color-scheme
- Background and contrast adjustments
- Critical colors defined inline
- Defensive approach (each client handles dark mode differently)

---

## Compatibility Considerations

### Outlook Desktop

- Limited support for background-image and advanced CSS
- Hero section includes solid color fallback

### Gmail

- May override link colors
- Important links use forced inline color

---

## CSS Avoided in Email

- Flexbox
- Grid
- Position
- External CSS
- CSS variables
- Complex selectors

---

## Future Improvements — Email

- Alternative hero version without background image
- Outlook VML background fallback
- More CTA variations
- Client-specific fine tuning
- Color and spacing tokens

---

---

# Part 2 — Landing Page

## Goal

Create a static landing page with modern layout, semantic structure, responsiveness, and accessibility — without frameworks or JavaScript.

---

## HTML Structure

- Semantic HTML elements:
  - header
  - main
  - section
  - article
  - footer
- Proper heading hierarchy
- Implemented sections:
  - Hero
  - How it works (3 steps)
  - Plans (3 cards)

---

## CSS

- Separate stylesheet (`style.css`)
- No frameworks
- Section-based organization
- Consistent class naming
- Mobile-first approach

---

## Responsiveness — LP

- Mobile-first strategy
- Progressive grid breakpoints
- Cards reorganize into columns based on width
- Hero typography adapts per screen size

---

## Accessibility — LP

- Proper contrast ratios
- Visible focus states
- Hierarchical headings
- aria-label on recommended plan
- Clear CTA text

---

## Layout and UI

- Hero with contrast overlay
- Cards with hover elevation
- Recommended plan visually highlighted
- Buttons with hover, active, and focus states
- Safe and readable typography

---

## Future Improvements — LP

- Design tokens (colors, radius, spacing)
- CSS utility system
- FAQ section using details/summary
- More visual variation between sections
- Additional accessibility refinements

---

# Final Notes

This solution prioritizes:

- Real-world HTML Email compatibility
- Correct table-based structure
- Inline CSS for email
- Semantic and responsive Landing Page
- Basic accessibility practices
- Clean and organized code

Following standards commonly used in production environments.


