# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Sobre o projeto

Repositório da Fabrizia Gonsales (`https://github.com/fabriziagonsales/teste2`). Contém sites demo para prospecção de clientes (negócio de revenda de soluções digitais para negócios locais) e projetos pessoais.

## Idioma

Sempre responder em **português (pt-BR)**.

## Estrutura

```
Área de Trabalho/          ← raiz do repositório (branch: main)
├── demos/                 ← sites demo para prospecção de clientes
│   ├── index.html         ← portfólio público com lista dos demos
│   ├── academia/          ← demo para academia
│   ├── clinica-estetica/  ← demo para clínica estética
│   ├── odontologia/       ← demo odontologia (git próprio → fabriziagonsales/odontologia)
│   └── petshop/           ← demo petshop (git próprio → fabriziagonsales/petshop)
├── sabor-e-saude/         ← blog de receitas (deletado do disco, ainda no git)
└── site-teste/            ← git próprio — não versionar aqui
```

## Demos — padrão de desenvolvimento

Todos os demos são **single-file HTML** (`index.html`) com CSS e JS inline. Sem frameworks, sem build step, sem dependências locais. Fontes via Google Fonts.

### Stack padrão dos demos
- **Fontes:** Cormorant Garamond + DM Sans (demos premium) ou Inter + Playfair Display (portfólio)
- **Paleta padrão odontologia:** `--navy #0f1f35`, `--gold #b8973a`, `--cream #faf7f2`
- **Fotos:** Pexels (`images.pexels.com/photos/{ID}/pexels-photo-{ID}.jpeg?auto=compress&cs=tinysrgb&w=700`)
- **WhatsApp:** links `https://wa.me/55{DDD}{NUMERO}?text=...`

### Funcionalidades recorrentes nos demos
- Chatbot de agendamento (JS puro, respostas em objeto `const respostas = {}`)
- Scroll reveal via `IntersectionObserver` (classe `.reveal` → `.reveal.visible`)
- Comparison slider antes/depois (drag com mouse/touch, `clip-path` no `.comp-after`)
- Carrossel de depoimentos com auto-avanço e dots
- Banner LGPD com `localStorage` para salvar consentimento
- Máscara de telefone (`mascaraTel()`)
- Botão "Voltar ao topo" aparece após 400px de scroll
- Navbar ganha sombra ao rolar (`nav.scrolled`)
- Botão WhatsApp com animação pulse (`@keyframes pulse-wpp`)

## Git

- **Branch principal:** `main` (repositório teste2)
- **Demos com git próprio:** `demos/odontologia/` (branch `master`) e `demos/petshop/` (branch `master`) — **não adicionar como submodule, não commitar arquivos dessas pastas no repositório pai**
- **Nunca commitar:** `*.lnk`, `*.url`, `desktop.ini`, `ROMS/`, `SUPER NINTENDO/`, `Dura_Client-6.2/`, `Miracle74-1.3/`, `Novo(a) Documento de Texto.txt`
- Para commitar em odontologia ou petshop, entrar na pasta e usar o git deles separadamente
