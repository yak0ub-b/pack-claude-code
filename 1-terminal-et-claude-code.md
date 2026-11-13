# Le terminal et Claude Code

## Le terminal, en deux phrases

C'est une fenêtre où tu **tapes des commandes** au lieu de cliquer. Tu n'as pas besoin de le
maîtriser : Claude tape les commandes pour toi, et il te demande la permission avant de les lancer.

Sur Windows, le terminal s'appelle **PowerShell** (touche Windows, puis tape « PowerShell »). Sur
Mac, c'est **Terminal** (Cmd + Espace, puis « Terminal »). Ensuite, on passera sur **Warp** (fiche 2).

## Les 6 commandes à reconnaître

Tu ne les taperas presque jamais. Elles servent surtout à comprendre ce que fait Claude.

| Commande | Ce qu'elle fait |
|----------|-----------------|
| `pwd` | Affiche le dossier où tu es |
| `ls` | Liste ce qu'il y a dans le dossier |
| `cd nom-du-dossier` | Entre dans un dossier |
| `cd ..` | Remonte d'un dossier |
| `mkdir nom` | Crée un dossier |
| `clear` | Vide l'écran |

Astuce : la touche **Tab** complète les noms de dossiers, et la **flèche du haut** rappelle la
dernière commande.

---

## Installer Claude Code

Il faut un abonnement Claude **Pro** ou **Max**.

**Windows** (dans PowerShell) :

```powershell
irm https://claude.ai/install.ps1 | iex
```

Installe aussi **Git pour Windows**, que Claude Code utilise pour travailler :

```powershell
winget install --id Git.Git -e
```

**Mac** (dans Terminal) :

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

Ferme le terminal et rouvre-le, puis tape `claude`. La première fois, il ouvre le navigateur pour
te connecter à ton compte.

> Sans terminal : l'app **Claude** de bureau a un onglet **Code** qui fait la même chose. Le
> terminal reste plus pratique avec Warp.

---

## Une session Claude Code, c'est quoi

Tu ouvres le terminal **dans le dossier de ton projet**, tu tapes `claude`, puis tu parles
normalement. Claude ne voit que ce dossier et ce qu'il contient.

| Dans Claude Code | Ce que ça fait |
|------------------|----------------|
| `/init` | Crée un `CLAUDE.md` en lisant ton projet |
| **Shift + Tab** | Passe en **mode plan** : il réfléchit et propose, sans rien toucher |
| **Échap** | L'arrête au milieu de ce qu'il fait |
| `@nom-du-fichier` | Lui montre un fichier précis |
| `/clear` | Repart d'une conversation vide (à faire entre deux tâches) |
| `/context` | Montre à quel point sa mémoire de travail est remplie |
| `/resume` | Reprend une conversation d'avant |
| `/model` | Change de modèle |
| `/help` | Toutes les commandes |

## Ce qu'il faut retenir

- **Un projet = un dossier.** Lance toujours `claude` depuis le dossier du projet.
- **Il demande avant d'agir.** Lis ce qu'il propose, puis accepte ou refuse.
- **Tu peux tout lui demander**, y compris « installe-moi X » ou « explique-moi cette commande ».

## Pour aller plus loin

- Guide du terminal pour débutants (officiel, en français) : https://code.claude.com/docs/fr/terminal-guide
- Démarrage rapide : https://code.claude.com/docs/fr/quickstart
- Cours gratuits d'Anthropic : https://anthropic.skilljar.com
