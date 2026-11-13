# Les skills

Un skill est une **méthode écrite** que Claude charge quand il en a besoin, ou quand tu tapes
`/nom-du-skill`. Ce dossier contient deux skills du pack, et la liste des skills de base à
installer depuis **skills.sh**.

Le plus simple : dis à Claude « Installe les skills de `skills/README.md` ». Il fera tout ce qui
suit.

---

## 1. Les skills du pack (à copier)

| Skill | Ce qu'il fait |
|-------|---------------|
| `prd/` | `/prd` : écrit le PRD de ton projet avant de produire quoi que ce soit (fiche 4) |
| `charte/` | `/charte` : crée SOUL.md, VOICE.md et DESIGN.md, avec trois directions visuelles (fiche 5) |

Copie-les dans tes skills personnels, pour qu'ils marchent dans tous tes projets.

**Windows** (PowerShell, depuis le dossier du pack) :

```powershell
New-Item -ItemType Directory -Force "$HOME\.claude\skills" | Out-Null
Copy-Item -Recurse -Force skills\prd, skills\charte "$HOME\.claude\skills\"
```

**Mac** :

```bash
mkdir -p ~/.claude/skills && cp -R skills/prd skills/charte ~/.claude/skills/
```

Tu peux les modifier : ce sont de simples fichiers texte. Si une règle ne te va pas, change-la.

---

## 2. Les skills de base (depuis skills.sh)

**skills.sh** est l'annuaire public de skills, tenu par Vercel. Chaque skill s'installe avec une
commande `npx skills add`. Il faut **Node.js** (demande à Claude de l'installer).

Le `-g` installe le skill pour tous tes projets, et `-a claude-code` l'installe pour Claude Code.

| Skill | À quoi il sert |
|-------|----------------|
| **find-skills** | Quand Claude manque d'une compétence, il cherche lui-même le bon skill sur skills.sh |
| **skill-creator** | Créer tes propres skills, les tester et les améliorer |
| **frontend-design** | Des pages et des interfaces qui n'ont pas l'air « faites par une IA » |
| **web-design-guidelines** | Vérifier une page : lisibilité, accessibilité, bonnes pratiques |
| **agent-browser** | Claude pilote un navigateur : ouvrir un site, cliquer, faire des captures (pratique pour capturer le site d'un prospect) |
| **hyperframes** | Faire des vidéos en HTML (fiche 6) |

```bash
npx skills add vercel-labs/skills --skill find-skills -g -a claude-code
```

```bash
npx skills add anthropics/skills --skill skill-creator -g -a claude-code
```

```bash
npx skills add anthropics/skills --skill frontend-design -g -a claude-code
```

```bash
npx skills add vercel-labs/agent-skills --skill web-design-guidelines -g -a claude-code
```

```bash
npx skills add vercel-labs/agent-browser --skill agent-browser -g -a claude-code
```

HyperFrames s'installe plutôt dans le dossier de ton projet vidéo (voir la fiche 6) :

```bash
npx skills add heygen-com/hyperframes
```

`agent-browser` a aussi besoin de son outil en ligne de commande. Le skill explique comment
l'installer, et Claude s'en occupe.

---

## 3. Les commandes utiles

| Commande | Ce qu'elle fait |
|----------|-----------------|
| `npx skills find vidéo` | Cherche des skills sur un sujet |
| `npx skills list` | Liste tes skills installés |
| `npx skills update` | Met tes skills à jour |
| `npx skills remove nom` | Supprime un skill |

Tu peux aussi parcourir l'annuaire sur https://skills.sh.

**Un conseil** : n'installe pas cinquante skills d'un coup. Commence par ceux-là, et ajoute-en un
quand un vrai besoin se présente. Pour savoir lequel, demande à Claude : find-skills est fait pour
ça.
