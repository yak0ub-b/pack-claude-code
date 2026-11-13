# Faire des vidéos

## 1. D'abord, un exemple réel

Ouvre **[7-les-coulisses-du-tuto-SAS.html](7-les-coulisses-du-tuto-SAS.html)** dans ton navigateur
(double-clic sur le fichier). C'est le making-of d'une vraie vidéo de 2 minutes faite avec l'IA :
les outils utilisés, la façon de travailler, les versions successives et le film plan par plan.

Ce qu'il faut en retenir :

| Étape | Ce qu'on fait | Outil |
|-------|---------------|-------|
| 1. Le texte d'abord | Écrire ce que la voix va dire **avant la moindre image**, comme si on l'expliquait à quelqu'un assis à côté | Claude |
| 2. La voix | Essayer plusieurs voix, et garder la plus humaine | ElevenLabs |
| 3. Les images suivent la voix | Chaque élément arrive à l'écran au moment où la voix le nomme | Claude |
| 4. Le son | Une musique sous la voix, qui ne la couvre jamais | Claude |
| 5. Regarder, corriger, recommencer | Regarder chaque version en entier, avec le son, comme un spectateur qui la découvre. Quatre versions dans la journée, c'est normal. | — |

Deux astuces à garder :

- **Le test Whisper** : on fait transcrire la vidéo finie, musique comprise, par Whisper (une IA
  qui écoute et écrit ce qu'elle entend). Si elle comprend chaque phrase, un humain aussi.
- **Les logos** des marques qu'on montre viennent de Simple Icons (https://simpleicons.org), aux
  couleurs officielles, au lieu d'être redessinés par l'IA.

C'est l'ordre de tout ce pack : **le texte (le PRD) avant les images, et une identité (la charte)
avant de produire.**

---

## 2. HyperFrames : un outil pour les fabriquer

### C'est quoi

**HyperFrames** est un outil gratuit et open source, créé par HeyGen. L'idée : **une vidéo est une
page HTML** (des textes, des images, des vidéos, des animations), et HyperFrames la transforme en
fichier MP4.

Tu n'as pas besoin de savoir coder : **c'est Claude qui écrit le HTML**, et c'est un langage qu'il
maîtrise très bien. Toi, tu décris ce que tu veux, tu regardes l'aperçu dans le navigateur, et tu
demandes des changements.

### Pourquoi c'est bien pour commencer

- **Reproductible** : la même page donne toujours la même vidéo. Tu changes un mot, tu relances,
  et le reste ne bouge pas. Avec un générateur comme Veo ou Kling, chaque essai donne autre chose.
- **Fidèle à ta charte** : les couleurs, polices et règles de `DESIGN.md` sont appliquées
  telles quelles.
- **Fait pour les séries** : une vidéo de prospection, puis la même pour 50 prospects, avec leur
  nom, leur logo et une capture de leur site.
- **Combinable** : tu peux y mettre la voix d'ElevenLabs, ta musique, et des plans générés par IA
  (Veo, Kling, Runway) comme fond ou comme séquence.

Exemples : présentations de produit, vidéos de prospection personnalisées, sous-titres animés,
graphiques animés, tutoriels, vidéos à partir d'un site ou d'un PDF.

### Ce qu'il faut sur l'ordinateur

- **Node.js** version 22 ou plus ;
- **FFmpeg**, l'outil qui fabrique le fichier vidéo.

Demande à Claude : « Installe-moi Node.js et FFmpeg. »

### L'installer dans Claude Code

Le plus simple, c'est le plugin officiel (deux commandes dans le terminal) :

```bash
claude plugin marketplace add heygen-com/hyperframes
claude plugin install hyperframes@hyperframes
```

Ou en skills, depuis le dossier de ton projet vidéo :

```bash
npx skills add heygen-com/hyperframes
```

Dans la liste qui s'affiche, coche le groupe **Core Skills**. C'est tout ce qu'il te faut.

### L'utiliser

Ouvre Claude dans ton projet (qui a déjà son PRD et sa charte) et demande par exemple :

> Avec /hyperframes, crée la vidéo décrite dans `docs/PRD.md`, en suivant `docs/marque/`. Format
> 9:16, 20 secondes, sous-titres animés, logo de `assets/logo/` sur le dernier plan.

Claude prépare la vidéo et t'ouvre un aperçu. Tu demandes les retouches, puis il exporte le MP4.

Si tu veux le faire à la main :

```bash
npx hyperframes init ma-video     # crée le projet
cd ma-video
npx hyperframes preview           # aperçu dans le navigateur
npx hyperframes render            # export en MP4
```

### Le projet vidéo type

```
prospection-video/
├── CLAUDE.md            ← règles (copié de modele-projet/)
├── docs/
│   ├── PRD.md           ← /prd, avec le module vidéo
│   └── marque/          ← /charte : SOUL, VOICE, DESIGN
├── assets/              ← logo, voix, musique, polices, rushs
├── prospects.csv        ← si série personnalisée : une ligne par prospect
└── exports/             ← les MP4 finaux
```

L'ordre ne change pas : **PRD, puis charte, puis texte et voix, puis images.**

### Et Remotion ?

**Remotion** fait la même chose, mais en React (un langage de développeur web plus complexe). Il
est très solide et a aussi des skills pour Claude. Sa licence est payante pour les entreprises
au-delà d'une petite équipe. Pour débuter, HyperFrames est plus simple.

## Pour aller plus loin

- HyperFrames, le code et la documentation : https://github.com/heygen-com/hyperframes
- HyperFrames, démarrage rapide : https://hyperframes.heygen.com/quickstart
- Des exemples de vidéos HyperFrames : https://hyperframes.heygen.com/examples
- Les voix : https://elevenlabs.io
- Whisper : https://openai.com/index/whisper/
