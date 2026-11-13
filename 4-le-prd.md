# Le PRD

> En pratique : tape `/prd` dans Claude Code, ou dis « fais-moi le PRD de… ». Le skill fait le
> reste. Cette fiche explique **pourquoi ce PRD est construit comme ça**.

## C'est quoi

**PRD** veut dire *Product Requirements Document*, le « document des exigences du produit ».
C'est le texte qui dit **quoi construire, pour qui, et quand c'est fini**, avant de commencer à
construire.

Il ne dit pas *comment* le faire. Ça, c'est le travail de Claude.

## D'où ça vient

- **Années 1960-70** : l'industrie et l'ingénierie (aéronautique, défense) écrivent des cahiers des
  charges avant de fabriquer, parce qu'une erreur découverte en usine coûte cent fois plus cher
  qu'une erreur découverte sur papier.
- **Années 1980-90** : les éditeurs de logiciels reprennent l'idée. Le marketing écrit ce que veut
  le marché, et le chef de produit le traduit en PRD, souvent très long.
- **Années 2000** : les méthodes agiles raccourcissent tout ça. On écrit moins et on teste plus
  vite. Amazon invente une variante : écrire le communiqué de presse **avant** de construire le
  produit (le PR/FAQ, voir plus bas).
- **Aujourd'hui** : avec l'IA, le PRD revient en force sous le nom de *spec-driven development*
  (développement guidé par la spécification). GitHub Spec Kit et Kiro, par exemple, sont construits
  autour de cette idée.

**Pourquoi il revient** : une IA exécute exactement ce que tu lui dis, très vite. Si c'est flou,
elle remplit les trous avec la moyenne de ce qu'elle a vu. Tu passes alors ton temps à corriger.
Une heure de PRD économise une journée de « non, pas comme ça ».

---

## La règle qui commande tout

**Le PRD fait 80 % du travail.** On ne produit rien (pas de code, pas d'image, pas de vidéo)
avant qu'il soit écrit **et relu par toi**.

---

## L'architecture : un noyau et des modules

```
┌─────────────────────────────────────────────┐
│  NOYAU (7 rubriques)  →  pour tout produit   │   ne bouge pas
├─────────────────────────────────────────────┤
│  Sections 7 à 12      →  si le sujet en a    │   précisions
├──────────────────────┬──────────────────────┤
│  Module logiciel     │  Module vidéo        │   se réécrit quand
│  (app, site, outil)  │  (vidéo, série)      │   l'outil change
└──────────────────────┴──────────────────────┘
```

**Pourquoi séparer** : le noyau décrit **le besoin**, qui ne dépend d'aucun outil. Les modules
décrivent **la fabrication**. Si tu passes de Kling à HyperFrames, ou d'un site à une app, tu
réécris le module sans toucher au besoin. Et le même noyau marche pour une vidéo, une app, une
offre ou un événement.

---

## Le noyau, rubrique par rubrique

### 1. « C'est fini quand… »

> **C'est fini quand** [qui] peut [geste visible] [dans telle condition difficile], sans [ce qui
> disparaît].

**Pourquoi** : sans ligne d'arrivée, ni toi ni l'IA ne savez quand vous arrêter. Chaque morceau de
la phrase a un rôle :

- **qui** : un acteur précis, pas « les utilisateurs » ;
- **geste visible** : quelque chose qu'on peut regarder se produire ;
- **condition difficile** : là où ça casse d'habitude (sur téléphone, sans le son, en 10 secondes) ;
- **sans** : la douleur qui disparaît.

| ❌ Flou | ✅ Observable |
|--------|--------------|
| « Une vidéo de prospection réussie » | « C'est fini quand un gérant de salle de sport qui ne me connaît pas comprend en 20 secondes, **sans le son**, ce que je fais pour lui, et voit son propre site dans la vidéo. » |

### 2. Trois critères, par oui ou par non

**Pourquoi binaires** : « est-ce que c'est beau ? » se discute pendant des heures. « Est-ce que le
prénom du prospect apparaît dans les 3 premières secondes ? » se vérifie en une minute.
**Pourquoi trois au maximum** : au-delà, on dilue, et plus rien n'est prioritaire.

### 3. Les problèmes, classés par douleur

Chaque problème vient avec sa **conséquence concrète** (temps, argent, client perdu).

**Pourquoi** : c'est le filtre anti-« tant qu'on y est ». Chaque fonction ou scène doit renvoyer à
un problème de cette table. Si elle n'y renvoie pas, elle sort.

### 4. Les utilisateurs et le moment d'usage

Qui, où, sur quel appareil, avec combien de temps.

**Pourquoi** : la scène réelle change tout. Une vidéo regardée dans le métro, son coupé, entre
deux stories, ne se fait pas comme une vidéo regardée sur un ordinateur au bureau.

### 5. Le parcours de A à B

La situation de départ, les étapes, puis le résultat.

**Pourquoi** : tout ce qui ne sert pas ce parcours sort de la version. C'est la colonne vertébrale.

### 6. Le périmètre : dedans **et dehors**

**Pourquoi le « dehors » compte autant** : l'IA adore ajouter des choses. Écrire ce qu'on ne fait
**pas**, avec la raison et la version où on le fera, l'arrête net, et ça t'évite de tout vouloir
dans la V1.

### 7. La question avant construction

La question dont la réponse peut changer tout le périmètre.

**Pourquoi** : une seule question peut transformer le projet. « La vidéo est-elle regardée avec le
son ? » Si non, toute l'histoire passe par le texte à l'écran. On ne commence pas tant qu'elle n'a
pas de réponse. Les autres incertitudes vont dans « questions ouvertes », avec **comment on le
saura**.

---

## Les choix de méthode, et pourquoi

| Choix | Pourquoi |
|-------|----------|
| **Le quoi, pas le comment** | Si le PRD impose les outils, les fichiers et les détails, l'IA s'enferme dedans et la complexité monte. On décrit l'intention et on laisse la réalisation libre. |
| **Taille proportionnée** | Une vidéo n'a pas besoin de 24 sections. On garde le noyau et le module utile, c'est tout. |
| **Supprimer les sections vides** | Une section vide fait croire qu'un sujet a été traité. |
| **Ne rien inventer** | Un chiffre ou une contrainte que tu n'as pas donnés devient une question ouverte, pas une règle. |
| **Deux façons de le remplir** | Idée claire : Claude rédige directement, avec 3 questions au maximum. Idée floue : il t'interviewe par groupes de 3 questions, et le PRD sort de tes réponses. |
| **La relecture humaine** | Claude termine par une seule question : « Est-ce que la phrase *C'est fini quand* décrit bien ce que tu veux voir marcher ? » Si oui, on produit. |
| **La preuve** | Un bon PRD se teste ainsi : une session neuve, qui ne reçoit que le PRD, construit le produit sans poser de question sur le besoin, et sait quand elle a fini. |

## Ce qu'on a volontairement laissé de côté

- **Les longues listes de « user stories »** : elles n'apparaissent qu'en section 7, quand un
  écran a des états à décrire.
- **Les personas marketing détaillés** (âge, hobbies, photo) : on garde seulement la scène d'usage,
  c'est elle qui décide.
- **La roadmap sur un an** : on écrit la version actuelle et ce qui est repoussé, rien de plus.
- **Le choix des outils dans le noyau** : il est rangé dans les modules, pour que le besoin
  survive à un changement d'outil.

---

## Exemple : une vidéo de prospection (extrait)

> **C'est fini quand** un gérant de salle de sport qui ne me connaît pas comprend en 20 secondes,
> sans le son, ce que je fais pour lui, et voit son propre site dans la vidéo.
>
> **Critères** : 1. Son prénom et sa salle apparaissent avant 3 s. 2. La vidéo fait moins de 30 s.
> 3. Le dernier plan dit exactement quoi faire (« Répondez "oui" à ce message »).
>
> **P1** : les messages de prospection écrits ne sont pas lus → 2 % de réponses.
>
> **Hors de cette version** : la voix off (V2, à tester une fois le format validé) ; la version
> anglaise (jamais pour l'instant).
>
> **Question avant construction** : est-ce que j'ai une capture du site de chaque prospect, ou
> est-ce que Claude doit la faire lui-même ?

---

## La variante : le PR/FAQ d'Amazon

Avant de lancer un projet, Amazon écrit **le communiqué de presse du jour du lancement** (une
page), puis **la FAQ** que poseraient les clients et l'équipe.

**Quand l'utiliser** : avant même le PRD, quand tu ne sais pas encore si l'idée vaut le coup. Si
le communiqué ne donne envie à personne, le projet ne vaudra rien non plus.

Demande à Claude : « Écris le communiqué de presse du lancement de [projet], puis les 10 questions
les plus dures qu'on me poserait, avec mes réponses. »

## Pour aller plus loin

- Le PR/FAQ expliqué : https://workingbackwards.com/resources/working-backwards-pr-faq/
- GitHub Spec Kit (le PRD pour les agents) : https://github.com/github/spec-kit
- Marty Cagan sur la spec produit : https://www.svpg.com/revisiting-the-product-spec/
