# Configurer un projet

Quel que soit le projet (une vidéo, une app, une marque), la base est la même : **un dossier bien
rangé**, avec quelques fichiers que Claude lit pour savoir quoi faire et comment.

## Le dossier type

```
mon-projet/
├── CLAUDE.md          ← les règles du projet, lues à chaque session
├── docs/
│   ├── PRD.md         ← ce qu'on construit, et quand c'est fini
│   └── marque/
│       ├── SOUL.md    ← qui est la marque
│       ├── VOICE.md   ← comment elle parle
│       └── DESIGN.md  ← à quoi elle ressemble
├── assets/            ← tes fichiers : logos, images, musiques, polices
└── ...                ← le travail (vidéos, code, pages)
```

Le dossier `modele-projet/` de ce pack contient déjà ce squelette. Copie-le pour chaque nouveau
projet.

---

## CLAUDE.md : les règles du projet

C'est le fichier le plus important de la configuration. **Claude le lit au début de chaque
session.** Il y trouve :

- le projet en une phrase ;
- où sont les documents à lire (PRD, charte) ;
- les règles à respecter (« pas de vidéo avant que le PRD soit validé », « uniquement les couleurs
  de DESIGN.md ») ;
- les commandes utiles (prévisualiser, exporter).

Les règles d'or :

- **Court** : moins de 200 lignes. Pour un long document, mets un lien vers lui plutôt que de le
  recopier.
- **Vivant** : quand Claude se trompe deux fois sur la même chose, dis-lui « ajoute cette règle au
  CLAUDE.md ».
- `/init` en écrit un premier à partir de ce qu'il trouve dans le dossier.

## AGENTS.md : la même chose pour les autres IA

`AGENTS.md` joue le même rôle que `CLAUDE.md`, mais c'est un format ouvert, lu par les autres
agents de code (Codex, Cursor, Gemini…).

- **Tu n'utilises que Claude** : `CLAUDE.md` suffit. Les versions récentes de Claude Code lisent
  aussi `AGENTS.md` quand il n'y a pas de `CLAUDE.md`.
- **Tu utilises plusieurs IA** : mets tes règles dans `AGENTS.md`, et écris dans `CLAUDE.md` la
  ligne `@AGENTS.md`. Claude le chargera aussi.

## La mémoire : 3 couches

| Couche | Où | Pour quoi |
|--------|-----|-----------|
| **Toi** | `~/.claude/CLAUDE.md` | Tes préférences pour tous les projets. Exemple : « Réponds toujours en français. » |
| **Le projet** | `CLAUDE.md` à la racine du projet | Les règles de ce projet |
| **La mémoire automatique** | `MEMORY.md`, tenu par Claude lui-même | Ce qu'il apprend en travaillant avec toi. `/memory` pour le voir et le modifier. |

Le `~` veut dire « ton dossier utilisateur » (`C:\Users\ton-nom` sur Windows).

---

## Les skills : des méthodes que Claude charge quand il en a besoin

Un skill est un dossier qui contient un fichier `SKILL.md` : une **méthode écrite** (comment faire
un PRD, comment faire une charte, comment monter une vidéo). Claude ne lit que la description de
chaque skill. Il charge la méthode complète quand le sujet arrive, ou quand tu tapes `/nom-du-skill`.

| Où le mettre | Disponible |
|--------------|------------|
| `~/.claude/skills/nom/SKILL.md` | Dans tous tes projets |
| `mon-projet/.claude/skills/nom/SKILL.md` | Dans ce projet seulement |

- **Installer des skills tout faits** : voir [skills/README.md](skills/README.md) (skills.sh).
- **Les deux skills de ce pack** : `/prd` et `/charte`.
- **Créer le tien** : le skill `skill-creator`, ou dis simplement « fais-moi un skill qui… ».

Quand utiliser quoi :

| Tu veux… | Mets-le dans… |
|----------|---------------|
| Une règle toujours vraie dans ce projet | `CLAUDE.md` |
| Une méthode que tu réutilises souvent | Un skill |
| Ce que tu veux construire cette fois | `docs/PRD.md` |
| L'identité de la marque | `docs/marque/` |

---

## Gérer le contexte : 5 règles

Le **contexte**, c'est la mémoire de travail de Claude pendant une conversation. Elle est grande
mais pas infinie, et plus elle est encombrée, moins il est précis.

1. **Une tâche = une conversation.** Fais `/clear` avant de passer à autre chose.
2. **Les décisions vont dans des fichiers**, pas seulement dans la conversation. Une conversation
   s'efface, un fichier reste.
3. **Mode plan avant les grosses tâches** (Shift + Tab) : il propose d'abord, il agit ensuite.
4. **Montre des fichiers précis** avec `@fichier` plutôt que « regarde tout ».
5. **`/context`** te montre le remplissage. Au-delà de la moitié, termine la tâche et repars à
   neuf.

## Pour aller plus loin

- La mémoire et CLAUDE.md : https://code.claude.com/docs/fr/memory
- Les skills : https://code.claude.com/docs/fr/skills
- Les bonnes pratiques : https://code.claude.com/docs/fr/best-practices
