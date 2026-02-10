# Teste Técnico — Frontend — V4 Company (HTML Email)

Este repositório contém minha solução para o teste técnico de **Frontend da V4 Company**, focado na implementação de um **HTML Email marketing** compatível com diferentes clients.

O objetivo foi aplicar boas práticas reais de mercado para email HTML, considerando limitações de renderização, compatibilidade e responsividade.

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
│   ├── index.html
│   └── style.css
│
└── README.md
```



---

# Como abrir e testar localmente

## Visualização básica

1. Acesse a pasta `/email`
2. Abra o arquivo `index.html` no navegador

Isso permite validar:
- Estrutura
- Hierarquia visual
- Espaçamentos
- Conteúdo

## teste mais próximo do real (recomendado)

Para validar comportamento em clients de email:

- Colar o HTML em plataformas como:
  - Mailtrap
  - Sendgrid
  - Mailchimp (modo HTML)
- Enviar para:
  - Gmail
  - Outlook
  - Apple Mail
- Testar:
  - Desktop
  - Mobile
  - Dark mode

---

# Decisões Técnicas — HTML Email

## Estrutura

- Layout 100% baseado em **tabelas**
- Sem uso de `<div>` para layout (padrão de mercado para email)
- Container principal com largura de **600px**
- Blocos separados por tabelas:
  - Header
  - Hero
  - Benefícios
  - Prova social
  - Agenda
  - CTA
  - Footer

## Estilos

- CSS principal em **inline**
- `<style>` usado apenas para:
  - reset básico
  - media query simples
  - suporte a dark mode
- Evitado CSS moderno com baixa compatibilidade

## Responsividade

- Media query para telas menores:
  - container vira 100%
  - colunas empilham
  - headline reduz tamanho
- Mesmo sem media query, o conteúdo permanece legível

## Botões (CTA)

- Implementados como **bulletproof buttons**
- Estrutura:
  - `<table>` + `<td bgcolor>` + `<a>`
- Funciona mesmo com suporte parcial de CSS

## Preheader

Implementado com técnica compatível com Outlook:

- display:none
- font-size:0
- overflow:hidden
- mso-hide:all

Evita aparecer no corpo do email e melhora preview na inbox.

## Acessibilidade

- Texto real (não imagem com texto)
- `alt` nas imagens
- Contraste adequado
- Tabelas de layout com `role="presentation"`

## Dark Mode

- Uso de `prefers-color-scheme`
- Footer adaptado para fundo escuro
- Links com cor definida inline para evitar sumir no modo claro/escuro

---

# Compatibilidade e Limitações — Email

HTML Email possui limitações importantes que foram consideradas:

## Outlook Desktop

- Suporte limitado a:
  - background-image
  - border-radius
  - CSS avançado
- Hero possui fallback de cor sólida

## Gmail

- Pode sobrescrever cores de links
- Links críticos usam cor inline forçada

## CSS evitado por compatibilidade

- flexbox
- grid
- position
- CSS externo
- seletores complexos
- variáveis CSS

## Background de imagem

Nem todos os clients suportam — definido também `bgcolor` de fallback.

## Dark mode

Cada client aplica regras próprias — implementação é defensiva, não pixel-perfeita.

---

# Decisões de Design do Email

O design foi pensado para:

- Leitura rápida (escaneável)
- Hierarquia clara de informação
- Contraste forte no hero
- Corpo com fundo claro e texto preto para máxima legibilidade
- CTAs com cor de destaque consistente
- Blocos bem separados por espaçamento
- Tipografia segura (Arial / sans-serif)

Estrutura segue padrão comum de campanhas:

Hero → Benefícios → Prova → Estrutura → CTA → Footer

---

# Melhorias de Design que eu aplicaria com mais tempo

- Sistema de tokens de cor e espaçamento padronizado
- Versão alternativa de hero sem imagem (100% sólido)
- Ícones visuais nos blocos de benefícios
- Cards de benefícios com borda e sombra compatível
- Variação visual entre seções (faixas de fundo alternadas)
- Ajustes finos de tipografia por client
- Versão A/B com variação de CTA
- Ajustes específicos para dark mode por bloco

---

# Observação Final

A implementação prioriza:

- Compatibilidade real de clients de email
- Estrutura table-based correta
- Inline CSS
- Responsividade básica
- Boas práticas de acessibilidade
- Legibilidade de código

Seguindo o padrão esperado para emails de campanha em ambiente de produção.
