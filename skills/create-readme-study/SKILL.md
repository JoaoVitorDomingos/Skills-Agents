---
name: create-readme-study
description: 'Create a README.md for the user''s own study/portfolio projects (a site, a web system, or a CLI tool built to practice and showcase on GitHub) in the user''s personal style — not a generic open-source template. Use this whenever the user asks to create, write, draft, update, or improve a README for one of their own learning projects, even if they just say "cria um readme", "faz o readme desse projeto", "preciso de um readme pra mostrar pros recrutadores", or similar, in Portuguese or English. The output is HTML-heavy, with badges, a linked index with no trailing bullet, a centered hero image, a learning-focused Detalhamento/Funcionalidades section, and a License section at the end. Always prefer this skill over a plain/generic README template whenever the project looks personal or educational rather than a corporate or open-source library.'
---

# Create README (Study Projects)

## Role

You're helping the user document their own study/portfolio projects — small sites and systems built to learn and practice specific technologies, then published on GitHub for recruiters and other developers to see. Unlike a typical open-source README, this style exists to show **what was built, with what, and what was learned** while building it.

## Before writing anything

1. **Review the project.** Look for: a package-manager file (`package.json`, `pom.xml`, `requirements.txt`, `build.gradle`, `go.mod`, etc.) to detect the tech stack and versions; a deploy config or link (GitHub Pages, Vercel, Netlify); an existing `LICENSE` / `LICENSE.md` file or a `license` field to detect the license; image folders (commonly `img/`, `img/readme/`, `imagens/readme/`, `src/img/readme/`); and any existing README so you don't lose content the user wants kept.
2. **Classify the project** as one of:
   - **Site** — a static/front-end website (HTML/CSS/JS, maybe a framework), usually has a live deploy link.
   - **Sistema web** — an interactive web app with its own UI logic (vanilla JS, a framework, a backend).
   - **Sistema CLI/backend** — a command-line tool or backend-only project, usually has install/run instructions instead of a live link.
   This decides which section set from `references/structure-guide.md` to follow.
3. **Read `references/structure-guide.md`** for the full template: section order per project type, fixed emoji titles, badge patterns, and HTML conventions (index, image blocks, `<details>` summary, license block).
4. **Skim 1–2 matching files in `examples/`** (site vs. sistema) to calibrate tone, HTML density, and how much detail each section usually carries.

## Hard rules

- **Never infer or invent** the content of Detalhamento, Funcionalidades, Objetivo de Aprendizado, Arquitetura, or any other technical/learning section. Only use what's explicit in the code, config files, or what the user tells you. If the project itself doesn't make something obvious (what was learned, why a library was chosen, how a tricky feature works), **ask the user** — don't guess, and don't pad the section with generic filler.
- Ask the user, before writing or as soon as a gap appears, about: what the project does and why (if not obvious from the code), the features to list, the technical/learning points to highlight, and whether there's a live deploy link. Batch these into a short, focused set of questions rather than one at a time when possible.
- **License**: try to detect it from the project (`LICENSE` file, `license` field in a manifest). If you can't determine it with confidence, ask the user which license applies — never default to MIT just because it's common in the examples.
- The structure in `references/structure-guide.md` is a **guide, not a checklist**: skip any section that doesn't apply to this project (e.g., no Mobile section for a CLI tool, no Créditos section if no third-party assets were used).
- Write the README itself in **Brazilian Portuguese**, first person, in the same didactic, learning-focused voice as the examples. (These instructions are in English; the output never is.)

## Formatting rules

- HTML-heavy style throughout (`<p>`, `<strong>`, `<ul>`/`<li>`, `<img>`, `<details>`), matching `examples/` — not a plain-Markdown README.
- Title in `<h1 align="center" style="font-weight: bold;">`, badges right below it, declared as Markdown reference links at the very top of the file. See `references/structure-guide.md` for ready-to-adapt badge snippets for common stacks.
- A centered index right after the badges, linking to every `<h2 id="...">` section with ` • ` between items — **no trailing bullet after the last item.**
- Centered images and blocks use `align="center"` — never `display="flex"` (it has no centering effect).
- When an image's actual path is unknown, leave `src=""` empty but keep a descriptive `alt` text — never invent a path.
- `<br>` between minor blocks, `<br><br>` between `<h2>` sections.
- One emoji per `<h2>` title, matching the density in the examples — don't over-decorate the body text.
- Wrap the Detalhamento/Funcionalidades section in `<details><summary><h3>Sumário</h3></summary><ol>...</ol></details>` with anchors to its subsections, as in the examples — this is the standing pattern, used regardless of how many subsections there are.
- End every README with a `📃 Licença` section pointing to the `LICENSE` file. Unlike generic open-source templates, this section always stays inline here — don't omit it, and don't add separate "Contributing"/"Changelog" guide sections (this style doesn't use them; a short Créditos/Contribuidores section for assets or collaborators is fine when it applies).

## Writing the draft

1. Title + badges + index + hero image.
2. 📌 Sobre — what it is, what it's made with, why it was built (the learning goal, in plain terms).
3. 🚀 Acesse o Projeto (site, if there's a live link) or ▶️ Como Executar (system/CLI — prerequisites, install, run).
4. The learning/technical core — pick what fits: 🎯 Objetivo de Aprendizado, 💻 Funcionalidades / 📋 Detalhamento (with the `<details>` sumário), 🎨 Design, 📱 Mobile, 🏗️ Arquitetura, 📚 Conceitos/Conhecimentos Aplicados, 🔮 Próximas Melhorias.
5. 📚 Fontes & Créditos and/or 🤝 Contribuidores, only if applicable.
6. 📃 Licença, always last.

Present the draft and ask the user what to adjust, add, or cut — remind them the structure is flexible per project, and some sections may simply not apply.
