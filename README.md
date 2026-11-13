# Pack de démarrage Claude Code

Ce dossier rassemble ce que j'aurais aimé avoir au début. Ce n'est pas une formation : ce sont
des fiches courtes, des modèles à copier et deux skills prêts à installer.

Tu peux le lire toi-même, ou le donner à Claude et lui dire :

> Lis `README.md` et aide-moi à mettre ce pack en place, une étape à la fois.

---

## L'idée en 30 secondes

Claude Code, c'est Claude qui travaille **directement dans un dossier de ton ordinateur** : il lit
tes fichiers, en crée et lance des commandes. Ce qu'il produit dépend surtout de deux choses :

1. **Ce que tu lui donnes à lire.** Un **PRD** dit ce que tu veux obtenir. Une **charte** dit à quoi
   ça doit ressembler et comment ça parle. Sans eux, il devine, et il devine moyen.
2. **Comment ton dossier est rangé.** Un fichier `CLAUDE.md` contient tes règles, et quelques skills
   lui apprennent des méthodes.

Tout le reste (GitHub, bases de données, mise en ligne) viendra plus tard. Ce n'est pas utile pour
commencer.

---

## Le tout premier geste (5 minutes)

Il faut installer Claude Code une fois à la main. Ensuite, c'est lui qui fait le reste.

1. Dézippe ce dossier dans `Documents`.
2. Installe Claude Code avec la commande de la fiche [1-terminal-et-claude-code.md](1-terminal-et-claude-code.md).
3. Dans le terminal, va dans le dossier puis lance Claude :

   ```powershell
   cd $HOME\Documents\pack-claude-code
   claude
   ```

   Sur Mac : `cd ~/Documents/pack-claude-code`, puis `claude`.
4. Dis-lui : « Lis README.md et aide-moi à mettre ce pack en place. »

Il t'installera Warp, les outils et les skills, et il créera ton premier projet. Il te demandera
la permission avant chaque action.

---

## Dans l'ordre

| # | Quoi | Fiche | Temps |
|---|------|-------|-------|
| 1 | Comprendre le terminal, installer Claude Code | [1-terminal-et-claude-code.md](1-terminal-et-claude-code.md) | 10 min |
| 2 | Installer Warp et y lancer Claude | [2-warp.md](2-warp.md) | 5 min |
| 3 | Ranger un dossier de projet | [3-configurer-un-projet.md](3-configurer-un-projet.md) et `modele-projet/` | 10 min |
| 4 | Installer les skills | [skills/README.md](skills/README.md) | 5 min |
| 5 | **Écrire un PRD** | [4-le-prd.md](4-le-prd.md) | 30 min |
| 6 | **Faire la charte de ta marque** | [5-la-charte.md](5-la-charte.md) | 1 h |
| 7 | Voir comment une vraie vidéo IA a été faite | [7-les-coulisses-du-tuto-SAS.html](7-les-coulisses-du-tuto-SAS.html) (à ouvrir dans le navigateur) | 10 min |
| 8 | Faire ta vidéo | [6-video-hyperframes.md](6-video-hyperframes.md) | à toi |

Les étapes 5 et 6 sont **les plus importantes**. Une vidéo ou une app sans PRD ni charte, c'est
l'IA qui décide à ta place.

---

## Ce qu'il y a dans le dossier

```
pack-claude-code/
├── README.md                      ← tu es ici
├── 1-terminal-et-claude-code.md   ← le terminal, installer Claude Code
├── 2-warp.md                      ← Warp en une page
├── 3-configurer-un-projet.md      ← CLAUDE.md, AGENTS.md, mémoire, skills, contexte
├── 4-le-prd.md                    ← le PRD : pourquoi celui-là, comment il est construit
├── 5-la-charte.md                 ← SOUL.md, VOICE.md, DESIGN.md : ta marque en 3 fichiers
├── 6-video-hyperframes.md         ← la méthode vidéo, et HyperFrames pour fabriquer
├── 7-les-coulisses-du-tuto-SAS.html ← le making-of d'une vraie vidéo IA : outils et méthode
├── skills/
│   ├── README.md                  ← les skills à installer depuis skills.sh
│   ├── prd/                       ← skill /prd (à copier)
│   └── charte/                    ← skill /charte (à copier)
└── modele-projet/                 ← un dossier de projet prêt à copier
```

---

## Pour Claude (si c'est toi qui lis ce fichier)

Tu aides un débutant qui n'a jamais utilisé de terminal. Règles :

- **Fais à sa place** ce que tu sais faire (installer, copier, créer des dossiers). Explique en une
  phrase ce que tu vas faire et pourquoi, et demande-lui son accord avant chaque installation.
- **Une étape à la fois**, dans l'ordre du tableau. Attends qu'il confirme avant de passer à la
  suivante. Ne lui fais pas lire toutes les fiches d'un coup.
- **Étape 2** : installe Warp (`winget install Warp.Warp` sur Windows, `brew install --cask warp`
  sur Mac). Ensuite, propose-lui de fermer cette session et de relancer `claude` depuis Warp.
- **Étape 3** : demande-lui le nom de son premier projet, crée le dossier dans `Documents`, et
  copie dedans le contenu de `modele-projet/`.
- **Étape 4** : copie `skills/prd` et `skills/charte` dans `~/.claude/skills/`. Installe Node.js
  s'il manque, puis les skills listés dans `skills/README.md`.
- **Étapes 5 et 6** : elles se font dans son projet, pas ici. Rappelle-lui `/prd` et `/charte`.
- **Étape 7** : ouvre-lui `7-les-coulisses-du-tuto-SAS.html` dans son navigateur, et résume-lui la
  méthode en 5 étapes de la fiche 6.
- Explique chaque mot technique la première fois que tu l'emploies.
