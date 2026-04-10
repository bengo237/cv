[![Compiler CV avec LuaLaTeX](https://github.com/bengo237/cv/actions/workflows/compile-cv.yml/badge.svg)](https://github.com/bengo237/cv/actions/workflows/compile-cv.yml)
# CV — Chanel Dylane Bengono

**RSSI | Expert Cybersécurité** — Gouvernance SI · ISO 27001 · Pentest · SOC/SIEM · DevSecOps

[Portfolio](https://dylane-mu.vercel.app/) · [GitHub](https://github.com/bengo237) · [LinkedIn](https://www.linkedin.com/in/chanel-dylane-b-91b850194/)

---

## Structure

```
cv/
├── .github/workflows/compile-cv.yml   # GitHub Actions (LuaLaTeX → PDF + Release)
├── cvSections/
│   ├── professionalExperience.tex
│   ├── education.tex
│   ├── projects.tex
│   └── honors.tex
├── pics/                               # Photo et fond de page
├── CV_Dylane_Bengono.tex               # Fichier principal
└── ReCeiVe.cls                         # Classe LaTeX
```

## Compilation locale

Requiert **LuaLaTeX** (TeXLive ou MiKTeX) :

```bash
lualatex -interaction=nonstopmode CV_Dylane_Bengono.tex
```

Éditeurs recommandés : VS Code + LaTeX Workshop (`Ctrl+Alt+B`) · TeXstudio (`F5`)

## Compilation automatique

Un push sur `main` déclenche le [workflow GitHub Actions](.github/workflows/compile-cv.yml) qui :
1. Compile avec LuaLaTeX (Docker TeXLive)
2. Uploade le PDF comme **artefact** (90 jours)
3. Crée une **Release** avec le PDF en téléchargement

**Télécharger le dernier PDF** → [Releases](https://github.com/bengo237/cv/releases)

---

**Template** : ReCeiVe — Ged Lex · Claud D. Park · **v2.0.0**
