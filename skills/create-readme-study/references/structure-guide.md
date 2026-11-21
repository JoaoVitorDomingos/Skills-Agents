# README Structure Guide — Study Projects

This is the reference template for the user's personal README style. It merges the general-purpose README advice the user keeps for themselves with the concrete patterns found across their own projects. Treat every section below as a building block, not a mandatory checklist — see "Hard rules" in `SKILL.md`.

## Why this style exists

A README is the entry point to a project. For the user's study projects, it serves two audiences at once: other developers who want to understand the project, and recruiters who want to see what the user actually knows how to do. That's why, unlike a typical open-source README, this style always keeps a learning-focused section (Funcionalidades / Detalhamento / Objetivo de Aprendizado) instead of treating the README as pure user documentation.

## Section order by project type

| Site (static front-end) | Sistema web (own UI logic) | Sistema CLI / backend |
|---|---|---|
| 📌 Sobre | 📌 Sobre | 📌 Sobre |
| 🚀 Acesse o Projeto | 🚀 Acesse o Projeto | ▶️ Como Executar |
| 🎨 Design (if there's a Figma/design file) | 💻 Funcionalidades (with `<details>` sumário) | 🎯 Objetivo de Aprendizado |
| 📱 Mobile (if Mobile First was used) | 📱 Mobile (or an explanation of why there isn't one) | 📋 Detalhamento (with `<details>` sumário: Funcionalidades, Arquitetura, Conceitos Aplicados, Persistência, etc.) |
| Any extra integration section (e.g. 📝 Mailchimp) | — | 🔮 Próximas Melhorias |
| 📚 Fontes & Créditos | 🤝 Contribuidores | — |
| 📃 Licença | 📃 Licença | 📃 Licença |

Mix and match freely — e.g. a site with a deep technical build can still use a 📋 Detalhamento section instead of (or alongside) 🎨 Design.

## Fixed section titles (emoji + id)

Use these verbatim when the section applies; the `id` is what the index links to.

| Title | `id` | Notes |
|---|---|---|
| 📌 Sobre | `sobre` | Always first after the hero image. |
| 🚀 Acesse o Projeto | `acesso` | Sites with a live deploy link. |
| ▶️ Como Executar | `como_executar` | Systems/CLI tools: prerequisites, install, run. |
| 🎯 Objetivo de Aprendizado | `objetivo` | What topics the project was meant to practice. |
| 📋 Detalhamento | `detalhamento` | The technical deep-dive; wrap in `<details>` sumário. |
| 💻 Funcionalidades | `funcionalidades` | Alternative to Detalhamento for JS-heavy web systems. |
| 🎨 Design | `design` | Figma link, palette, etc. |
| 📱 Mobile | `mobile` | Mobile First evidence, or a note on desktop-only scope. |
| 🏗️ Arquitetura | `arquitetura` | Usually a subsection inside Detalhamento, not a top-level one. |
| 📚 Conceitos Aplicados / Conhecimentos Aplicados | `conceitos_aplicados` | List of concepts practiced, grouped by category when there are many. |
| 🔮 Próximas Melhorias | `melhorias` | Ideas for future versions. |
| 📚 Fontes & Créditos | `creditos` | Third-party assets (stock photos, icons, fonts) with attribution. |
| 🤝 Contribuidores | `contribuidores` | People who helped (design, etc.) — not a "how to contribute" guide. |
| 📃 Licença | `licenca` | Always last, always present. |

## Header block

```html
[HTML__BADGE]: https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white
[CSS__BADGE]: https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white
[MIT__BADGE]: https://img.shields.io/github/license/USUARIO/REPOSITORIO.svg

<h1 align="center" style="font-weight: bold;">Nome do Projeto</h1>

![html][HTML__BADGE]
![css3][CSS__BADGE]
![mit][MIT__BADGE]

<p align="center">
  <a href="#sobre">Sobre</a> • 
  <a href="#acesso">Acesse Aqui</a> • 
  <a href="#licenca">Licença</a>
</p>

<br>
<p align="center">
    <img src="img/readme/img_projeto.png" alt="Imagem do Projeto" width="800px">
</p>
<br>
```

Notes:
- Badges are declared once as Markdown reference links at the very top of the file, then used inline with `![name][REF]`.
- The index always ends **without** a trailing ` •` after the last link.
- If the exact image path isn't known, keep `src=""` and write a real, descriptive `alt`.

## Badge snippets by stack

Adapt color/logo to what's actually in the project; this is a starting set, not an exhaustive list.

| Stack | Snippet |
|---|---|
| HTML5 | `https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white` |
| CSS3 | `https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white` |
| JavaScript | `https://img.shields.io/badge/Javascript-000?style=for-the-badge&logo=javascript` |
| Bootstrap | `https://img.shields.io/badge/bootstrap-%238511FA.svg?style=for-the-badge&logo=bootstrap&logoColor=white` |
| React | `https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB` |
| Node.js | `https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white` |
| TypeScript | `https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white` |
| Java | `https://img.shields.io/badge/Java-21-orange?style=for-the-badge&logo=openjdk&logoColor=white` (adjust version) |
| Maven | `https://img.shields.io/badge/Maven-3.x-red?style=for-the-badge&logo=apachemaven&logoColor=white` |
| Python | `https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54` |
| MIT License | `https://img.shields.io/github/license/USUARIO/REPOSITORIO.svg` (swap in the real GitHub path once known) |

For any other license, use the matching `img.shields.io/github/license/...` badge or a plain `![License](https://img.shields.io/badge/License-<nome>-green?style=for-the-badge)` if the repo isn't public yet.

## Detalhamento / Funcionalidades block

```html
<h2 id="detalhamento">📋 Detalhamento</h2>
<p>Nesta seção detalharei sobre o projeto, citando os pontos mais importantes sobre ele e sua criação.</p>
<details>
  <summary><h3>Sumário</h3></summary>
  <ol>
    <li><a href="#subsecao_1">Nome da Subseção 1</a></li>
    <li><a href="#subsecao_2">Nome da Subseção 2</a></li>
  </ol>
</details>

<h3 id="subsecao_1">Nome da Subseção 1</h3>
<p>Explicação do que foi feito, como, e por quê.</p>
```

The `<details>` sumário is always used for this section, regardless of how many subsections it ends up having.

## License block

```html
<h2 id="licenca">📃 Licença</h2>
Veja a licença do projeto: <a href="https://github.com/USUARIO/REPOSITORIO?tab=MIT-1-ov-file">MIT License</a>
<br>
<br>
```

Swap the link text/tab fragment for whatever license actually applies (e.g. `Apache-2.0-1-ov-file`, `GPL-3.0-1-ov-file`).

## Conventions checklist

- No `--` anywhere in the file.
- `<br>` separates minor blocks; `<br><br>` separates `<h2>` sections.
- `align="center"` for centering — never `display="flex"`.
- Images default to `img/` (general project assets) and `img/readme/` (images made specifically for the README); if the real path isn't known, leave `src=""` with a descriptive `alt`.
- One emoji per `<h2>` title; don't add more decoration than the examples use.
- Common typos to avoid in the output: **licença** (not "lincença"), **design** (not "desing"), **seção** (not "sessão" — "sessão" is only correct when it means an actual session/sitting, e.g. a class session), **Mobile First** (not "Mobile Firs").
