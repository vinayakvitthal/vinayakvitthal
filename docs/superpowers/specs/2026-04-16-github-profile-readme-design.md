# GitHub Profile README Redesign

**Date:** 2026-04-16  
**Status:** Approved

---

## Overview

Redesign the `vinayakvitthal` GitHub profile README from the current layout (trophies + stats table) into a clean, minimal, fully animated profile that fills width effectively and represents Vinayak as a Full Stack Developer and AI enthusiast.

---

## Design Decisions

### Direction
- **Style:** Clean & Minimal — content-first, no clutter
- **Layout:** Single column flow, top to bottom
- **Color theme:** Nord (matches existing stats widgets)

### Animations (all 4)
1. **Waving header + footer** — via `capsule-render` (twinkling gradient)
2. **Multi-line typing SVG** — rotates: "Full Stack Developer", "AI Agent Builder", "Open Source Enthusiast", "Always Learning"
3. **Animated skill icons** — via `skillicons.dev` (colorful, hover-animated)
4. **Contribution snake** — via GitHub Actions + `platane/snk`, served from `output` branch

---

## Section Order

1. Wave header (capsule-render)
2. Name + subtitle + typing SVG
3. Connect with Me badges (GitHub, LinkedIn, PyNotes, MyLearning)
4. Divider
5. About Me + Currently — **side-by-side cards** (2-column grid)
6. Tech Stack — **full-width rows** (label left, icons right)
7. GitHub Stats — Activity Graph (full width) → Stats + Streak (side by side)
8. Contribution Snake
9. Wave footer (capsule-render)

---

## Content

### Name & Subtitle
- **Name:** Hi, I'm Vinayak V Kaddi 👋
- **Subtitle:** Full Stack Developer · AI Enthusiast · Open Source Learner

### About Me
> Full Stack Developer passionate about building scalable web applications and exploring the frontiers of AI. I work across the stack — from crafting clean UIs with React and Next.js to designing robust backends and experimenting with LLMs and AI agents.

### Currently
- 🔨 **Building:** Full Stack applications
- 📚 **Learning:** AI Agents & pipelines (LangChain, AgentScope, RAG)

### Tech Stack (skillicons.dev — dark theme)

| Category | Icons |
|---|---|
| Languages | Python, Java, JavaScript |
| Frontend | React, Next.js |
| Backend & DBs | Node.js, MySQL, PostgreSQL, MongoDB |
| AI / ML | LangChain, AgentScope, RAG, Vector DB (badges — no skillicon available) |
| Tools | Git, VS Code, IntelliJ IDEA, Android Studio, Kiro (badge) |

### GitHub Stats
- **Activity Graph:** `github-readme-activity-graph` — Nord theme, full width
- **Stats card:** `github-readme-stats` — Nord theme
- **Streak card:** `streak-stats.demolab.com` — Nord theme

### Connect Badges (for-the-badge style, #2E3440 background)
- GitHub → `https://github.com/vinayakvitthal`
- LinkedIn → `https://www.linkedin.com/in/vinayak-v-kaddi/`
- PyNotes → `https://vinayakvitthal.github.io/pynotes/`
- MyLearning → `https://vinayak-kaddi743.gitbook.io/mylearning`

---

## Snake Animation Setup

The snake requires a GitHub Actions workflow (`.github/workflows/snake.yml`) that:
- Runs on a schedule (daily) and on push to `main`
- Uses `platane/snk@v3` to generate the SVG from the contribution grid
- Pushes the output SVG to the `output` branch
- README references: `https://raw.githubusercontent.com/vinayakvitthal/vinayakvitthal/output/github-contribution-grid-snake-dark.svg`

---

## Files to Create / Modify

- `README.md` — full rewrite
- `.github/workflows/snake.yml` — new GitHub Actions workflow

---

## What's Removed from Current README

- GitHub trophies widget (clutters minimal design)
- Profile summary card (replaced by cleaner about + stats layout)
- Nested `<table>` layout
