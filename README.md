# CV — Chanel Dylane Bengono

**RSSI | Expert Cybersécurité**

Professionnel en Gouvernance SI, Gestion des Risques, Sécurité Offensive & Défensive, Cloud Security et DevSecOps.

🔗 **Portfolio** : https://dylane-mu.vercel.app/
🔗 **GitHub** : https://github.com/bengo237
🔗 **LinkedIn** : https://www.linkedin.com/in/chanel-dylane-b-91b850194/

---

## 📋 Table des matières

- [Structure du projet](#structure-du-projet)
- [Compilation locale](#compilation-locale)
- [Compilation automatique (GitHub Actions)](#compilation-automatique-github-actions)
- [Versions](#versions)
- [Modifications récentes](#modifications-récentes)
- [Dépannage](#dépannage)

---

## 📁 Structure du projet

```
cv/
├── .github/
│   └── workflows/
│       └── compile-cv.yml              # Workflow GitHub Actions (LuaLaTeX)
├── cvSections/
│   ├── education.tex                   # Formation + Compétences techniques
│   ├── honors.tex                      # Certifications et Distinctions
│   ├── professionalExperience.tex      # Expérience professionnelle
│   └── projects.tex                    # Projets et contributions Open Source
├── pics/
│   ├── background5.pdf                 # Fond de page
│   └── pp2.png                         # Photo de profil
├── ReCeiVe.cls                         # Classe LaTeX customisée
├── ReCeiVe_cv_[2021].tex               # CV principal
├── debug-compile.sh                    # Script de debugging
└── README.md                           # Ce fichier
```

---

## 🖥️ Compilation locale

### Prérequis

- **LuaLaTeX** (fourni par TeXLive ou MiKTeX)
- **Bash** (pour les scripts)

### Installation

**Windows (MiKTeX)** :
```bash
# Installer MiKTeX depuis https://miktex.org/download
# Vérifier l'installation :
lualatex --version
```

**Linux (TeXLive)** :
```bash
sudo apt-get update
sudo apt-get install texlive-full
```

**macOS (HomeBrew)** :
```bash
brew install basictex
sudo tlmgr install collection-fontsextra
```

### Compilation

Depuis la racine du projet :

```bash
# Compilation simple
lualatex -interaction=nonstopmode ReCeiVe_cv_[2021].tex

# Compilation avec debugging
bash debug-compile.sh
```

**Output** : `ReCeiVe_cv_[2021].pdf` → Renommé en `CV_Dylane_Bengono_RSSI.pdf`

### Édition interactive

**VS Code + LaTeX Workshop** :
1. Installez l'extension `James-Yu.latex-workshop`
2. Ouvrez `ReCeiVe_cv_[2021].tex`
3. Appuyez sur `Ctrl+Alt+B` pour compiler
4. Le PDF s'ouvre automatiquement

**TeXstudio** :
1. Installez depuis https://www.texstudio.org/
2. Ouvrez `ReCeiVe_cv_[2021].tex`
3. Cliquez **Outils → Compiler** (ou `F5`)

---

## ⚡ Compilation automatique (GitHub Actions)

Le workflow compile automatiquement et génère des **Releases** à chaque push.

### Déclencheurs

✅ Push sur `main` ou `master`
✅ Changement dans `*.tex`, `*.cls`, `cvSections/`, `pics/`
✅ Pull Request
✅ Déclenchement manuel depuis **Actions**

### Résultats

1. **Artefact PDF** (90 jours) — accessible dans chaque run
2. **Release GitHub** — créée sur `main/master` avec
   - Tag : `cv-YYYY-MM-DD-HASH`
   - PDF dans les **Assets**
   - Marquée "Latest"

### Télécharger

**Releases (archivage)** :
```
https://github.com/bengo237/cv/releases
```

**Dernier build** :
1. Allez à **Actions** → **Compiler CV avec LuaLaTeX**
2. Cliquez sur le run le plus récent
3. Téléchargez `CV_Dylane_Bengono_RSSI`

---

## 🔄 Versions

### Format

`MAJOR.MINOR.PATCH (DATE)`

### Historique

| Version | Date | Notes |
|---------|------|-------|
| **2.0.0** | 2026-04-10 | Mise à jour complète : Profil RSSI, Projets, GitHub Actions |
| **1.0.0** | Base | Template original ReCeiVe |

### Fichiers versionés

- `ReCeiVe_cv_[2021].tex` : v2.0.0
- `ReCeiVe.cls` : v1.1 (template original)

---

## 📝 Modifications récentes (v2.0.0)

### Contenu

- ✅ En-tête auteur/version modernisé
- ✅ Profil "À propos de moi" densifié (6 lignes → plus d'impact)
- ✅ Compétences réorganisées par priorité RSSI
- ✅ Expériences avec **bullets en gras** (scannable en 3 sec)
- ✅ Section **Projets Open Source** ajoutée
- ✅ Certifications réordonnées (Gouvernance, Réseaux, Pentest)
- ✅ Cisco Ethical Hacker, CASA certifications ajoutées
- ✅ Eden Group (non pertinent) supprimé

### Automatisation

- ✅ **GitHub Actions Workflow** : Compilation LuaLaTeX en Docker
- ✅ **Artefacts** : PDF sauvegardés 90 jours
- ✅ **Releases** : Tags datés, téléchargement facile
- ✅ **Debugging** : Logs LaTeX capturés et affichés en cas d'erreur
- ✅ **Script local** : `debug-compile.sh` pour tests rapides

---

## 🐛 Dépannage

### PDF non généré sur GitHub Actions

1. **Vérifier les logs** :
   - Allez à **Actions** → dernier run → cherchez "ERREURS DE COMPILATION"

2. **Compiler localement** :
   ```bash
   bash debug-compile.sh
   ```

3. **Problèmes courants** :
   - Fichier `.log` vide → erreur avant la compilation
   - Chemins `cvSections/` non trouvés → vérifier le commit
   - Images manquantes → pousser le dossier `pics/`

### Erreur "Undefined control sequence"

Regardez le fichier `.log` à la ligne signalée pour l'erreur exacte.

---

## 📞 Contact

**Chanel Dylane Bengono**
- 📧 Email : chaneldylanebengono@gmail.com
- 🌐 Portfolio : https://dylane-mu.vercel.app/
- 💻 GitHub : https://github.com/bengo237
- 💼 LinkedIn : https://www.linkedin.com/in/chanel-dylane-b-91b850194/

---

**Template** : ReCeiVe (Ged Lex, Claud D. Park)
**Dernière compilation** : Voir [GitHub Actions](https://github.com/bengo237/cv/actions)
