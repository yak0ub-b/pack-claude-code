---
name: charte
description: Crée la charte d'une marque, d'une app, d'une chaîne vidéo ou d'une simple ambiance en trois fichiers, SOUL.md (qui elle est), VOICE.md (comment elle parle) et DESIGN.md (à quoi elle ressemble), avec des directions visuelles en HTML pour choisir. TRIGGER, « /charte », « fais-moi une charte graphique », « crée l'identité de… », « il me faut une marque », « une variante de la charte », avant la première vidéo ou le premier écran d'un projet sans charte. SKIP, changer une seule couleur ou un seul mot d'une charte existante.
---

# La charte

Ton entrée : une idée de marque, de produit ou d'ambiance. Ta sortie : trois fichiers dans
`docs/marque/`, plus le fichier HTML de la direction visuelle choisie.

## La règle qui commande tout

Sans charte, l'IA produit la moyenne de ce qu'elle a vu : propre, générique, et différent à chaque
fois. En vidéo, c'est pire : chaque plan est généré à part, et rien ne se ressemble. **La charte
est la mémoire de la marque.** Chaque visuel, texte ou vidéo doit pouvoir s'y relier.

## L'ordre : l'âme, puis la voix, puis le visuel

1. **SOUL.md** : pourquoi la marque existe, qui elle est, à qui elle parle, ce qu'elle n'est pas.
2. **VOICE.md** : comment elle parle, avec ses mots, ses mots interdits et ses exemples.
3. **DESIGN.md** : couleurs, polices, formes, mise en page et mouvement.

**Ne commence jamais par la palette.** Une couleur se justifie par une personnalité, pas l'inverse.

## La taille

- **Une marque ou une app** : les trois fichiers, complets.
- **Une ambiance (mood) ou un projet perso** : un SOUL court (raison d'être, personnalité, ce
  qu'on n'est pas) et un DESIGN. VOICE seulement s'il y a des textes ou une voix off.
- Supprime les sections qui ne servent pas. Une section vide fait croire qu'un sujet a été traité.

## Étape 1 — L'interview

Pose les questions **par groupes de 3**, jamais toutes d'un coup. Reformule chaque réponse en une
phrase avant le groupe suivant. Si l'utilisateur a déjà donné une réponse (dans la conversation ou
dans le PRD), ne repose pas la question.

1. **Le pourquoi** : Que fais-tu, et pour qui ? Qu'est-ce qui change pour eux grâce à toi ? Contre
   quoi te bats-tu (un problème, pas un concurrent) ?
2. **La personnalité** : Si la marque était une personne, qui serait-elle ? Donne 3 adjectifs, et
   pour chacun ce qu'il interdit. Qu'est-ce que la marque n'est surtout pas ?
3. **Le client** : Qui exactement, où, avec quoi dans les mains ? Comment parle-t-il ? Tu le
   tutoies ou tu le vouvoies ?
4. **L'univers** : De quel métier, de quel lieu, de quels objets ou de quelles matières peut-on
   s'inspirer ? Cite 2 ou 3 marques, films ou lieux dont tu aimes l'ambiance, et dis pourquoi.
   Qu'est-ce que tu détestes visuellement ?

Réponse floue → ne la note pas telle quelle. Propose une valeur par défaut, dis ce qu'elle engage,
et demande de confirmer.

Rédige `SOUL.md` puis `VOICE.md` à partir de `modeles/`. **Fais-les relire avant de passer au
visuel.**

## Étape 2 — Trois directions visuelles

- Puise chaque direction dans **l'univers** (groupe 4), pas dans les codes génériques du web.
- Une direction = **une idée + un élément signature + des règles d'usage**. Une palette sans
  règles ne sert à rien.
- Les trois doivent être **vraiment différentes** : pas la même mise en page avec trois palettes.
- Pour chacune, crée un fichier HTML autonome, `docs/marque/direction-[a|b|c]-[nom].html`, qui
  montre :
  - la palette, avec l'usage de chaque couleur ;
  - la typographie à l'échelle, avec un vrai texte de la marque (tiré de VOICE.md) ;
  - **si le projet fait des vidéos** : trois images clés (accroche, plan central, appel à l'action)
    en 9:16 et en 16:9, avec les sous-titres, et une phrase sur le mouvement ;
  - **si c'est une app ou un site** : l'écran principal, sa version mobile, les boutons et leurs
    états, un état vide ou une erreur.
- CSS dans le fichier. Polices en fichiers locaux (`assets/fonts/`) ou police système, jamais
  chargées depuis un service distant.
- Vérifie le rendu (capture d'écran si tu peux), et corrige ce qui déborde ou manque de contraste.
- Passe les **garde-fous anti-générique** de `modeles/DESIGN.md`.
- Présente les trois avec une phrase chacune et ta recommandation. L'utilisateur choisit, ou
  mélange.

## Étape 3 — DESIGN.md

Remplis `modeles/DESIGN.md` avec la direction choisie : les valeurs exactes dans l'en-tête YAML
(format DESIGN.md de Google), puis le texte qui dit **pourquoi** et **comment** les utiliser. Garde
la section Vidéo si le projet fait des vidéos, avec le **prompt de style** à coller dans les
générateurs (Veo, Kling, Runway…).

Garde le HTML de la direction retenue comme référence. Supprime les autres.

## Étape 4 — Les variantes (si demandé)

Une variante garde l'âme et la voix, et ne change **qu'une dimension** : mode sombre, saison,
réseau social, campagne, sous-marque. Elle s'écrit dans la section « Variantes » de DESIGN.md, en
ne listant que ce qui change.

## Les fichiers

- `docs/marque/SOUL.md`, `VOICE.md`, `DESIGN.md`, et le HTML de la direction retenue.
- Ajoute au `CLAUDE.md` du projet, s'il n'y est pas : « Avant tout visuel, texte ou vidéo, lis
  `docs/marque/`. »
- Les fichiers `modeles/` vivent dans le dossier de ce skill. Copie-les dans le projet, et ne
  modifie jamais l'original.

## Ce que tu refuses

- **Commencer par les couleurs.**
- **Les choix par défaut sans raison** : Inter ou Arial partout, dégradé violet, fond crème avec un
  accent terre cuite.
- **Inventer** un client, un chiffre, un avis ou une valeur que l'utilisateur n'a pas donnés.
- **Trois directions qui se ressemblent.**

## La preuve

Une session ouverte à froid, à qui on donne seulement `docs/marque/`, produit une vignette, une
légende et une vidéo de 10 secondes qu'on reconnaît comme venant de la même marque.
