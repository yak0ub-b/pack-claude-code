---
name: prd
description: Écrit le PRD d'un projet avant de le construire (vidéo, app, page, fonctionnalité), avec un noyau valable pour tout produit et un module pour le logiciel ou pour la vidéo. TRIGGER, « /prd », « fais-moi le PRD », « cadre ce projet », avant de produire quelque chose de nouveau. SKIP, un correctif de bug, une retouche dans un projet dont le PRD existe déjà.
---

# Le PRD

Ton entrée est une idée : une vidéo, une page, une app, une fonctionnalité. Ta sortie est un fichier
PRD rempli à partir de `modeles/PRD.md`, et relu par l'utilisateur. Rien n'est produit avant.

## La règle qui commande tout

**Le PRD fait 80 % du travail. Pas une ligne de code, pas une image, pas une vidéo avant qu'il soit
écrit et relu.** Sans lui : des prompts vagues, des corrections en boucle, et un projet qui dérive
vers autre chose que ce qui était voulu.

## Le noyau : 7 rubriques, pour tout produit

Elles ne dépendent ni de la technique ni du domaine.

| Rubrique | Section du gabarit |
|---|---|
| **C'est fini quand** : « [qui] peut [geste visible] [dans telle condition difficile], sans [ce qui disparaît] » | 1 |
| **Critères** : 3 au plus, chacun se répond par oui ou par non | 2 |
| **Problèmes**, classés par douleur, avec leur conséquence concrète | 3 |
| **Utilisateurs et rôles** : qui, où, sur quel appareil, avec quels droits | 4 |
| **Parcours** de A à B : ce qui ne le sert pas sort de la version | 5 |
| **Périmètre** : dedans (chaque fonction renvoie à un problème), dehors (raison et version cible) | 6 |
| **Questions ouvertes** : celle à trancher avant de construire, puis les autres, avec comment on le saura | 13, 14 |

Les sections 7 à 12 précisent le noyau quand le sujet le demande : spécifications, données de
démonstration, règles métier, exigences, conformité, référence visuelle.

## Les modules

Un module ajoute ce qui est propre à un type de produit. Il se réécrit quand la technique change,
sans toucher au noyau.

- **Module logiciel** (sections 15 à 19) : stack, modèle de données, structure, règles pour
  `CLAUDE.md`, jalons. Pour une app, un site, un outil.
- **Module vidéo** (sections 20 à 24) : format et diffusion, message, découpage, personnalisation,
  production. Pour une vidéo ou une série de vidéos.

Pour un autre type de produit (un service, une offre, un événement), le noyau suffit. Dis-le à
l'utilisateur, sans inventer de module.

## La taille

- **Une vidéo, une page ou une tâche** : sections 1 à 6 et 13, plus le module concerné. Ajoute 9
  (règles métier), 12 (référence visuelle) ou 18 (règles pour `CLAUDE.md`) seulement si le sujet en
  a.
- **Un produit complet**, sur plusieurs sessions : garde tout ce qui sert, et découpe le travail en
  jalons (section 19 ou 24). Une session = un jalon.

Supprime les sections non retenues, les commentaires et les crochets. Une section vide fait croire
qu'un sujet a été traité.

## Les 2 façons de le remplir

**L'idée est claire** (l'utilisateur sait ce qu'il veut) : rédige directement le PRD à partir de
ce qu'il a dit et de ce que tu lis dans le projet. Ne pose de question **que** sur les rubriques
que tu ne peux pas remplir. 3 questions au maximum.

**L'idée est floue** (« je sais pas trop », page blanche) : tu poses les questions, il répond, et le
PRD sort de ses réponses. Environ 20 questions pour un petit projet, **par groupes de 3**, jamais
toutes d'un coup. Reformule chaque réponse en une phrase avant le groupe suivant.

Réponse floue → ne la note pas telle quelle. Propose une valeur par défaut, dis ce qu'elle engage,
et demande de confirmer.

## Le bon dosage

Intention claire, **réalisation laissée libre**. Le PRD dit *quoi* et *pour qui*, pas *comment*.
Ce qui est décidé s'écrit comme une règle. Ce qui est incertain s'écrit comme une option à
justifier. Pas de liste de librairies, pas de schéma de base imposé, pas de nom de fichier à créer,
sauf si c'est une vraie contrainte de l'utilisateur. Plus précis n'est pas meilleur : trop rigide,
l'IA s'enferme et la complexité monte.

## Les fichiers

Copie `modeles/PRD.md` dans le projet et remplis-le. Emplacement : `docs/PRD-<sujet>.md` si le
projet a un dossier `docs/`, sinon `PRD-<sujet>.md` à la racine. Date du jour en tête.

Si le produit a un écran ou une image (app, page, vidéo) et que le projet n'a pas de charte
(`docs/marque/`), dis-le, et propose `/charte` avant de produire. La section 12 du PRD pointe vers
la charte.

## Avant de finir

1. Coche la « Relecture avant envoi » du gabarit sur le PRD rempli. Un état qu'aucune action
   n'atteint est un trou : ajoute l'action ou retire l'état.
2. Affiche le PRD dans la conversation.
3. **Demande à l'utilisateur de le relire**, et pose-lui une seule question : « Est-ce que la
   phrase *C'est fini quand* décrit bien ce que tu veux voir marcher ? »
4. Attends son accord. Ensuite seulement, la production peut commencer, avec le PRD comme contexte.

Pour faire critiquer un PRD existant, l'utilisateur peut demander : « Attaque ce PRD : ce qui est
flou, ce qui se contredit, ce qu'on ne peut pas vérifier, ce qui manque. »

## Ce que tu refuses

- **De produire** (code, image, vidéo), même « juste pour voir ». Ta sortie, c'est un fichier texte.
- **De laisser vides « C'est fini quand » ou « Hors de cette version ».** Si l'utilisateur ne sait
  pas, propose une valeur.
- **D'inventer une contrainte** ou un chiffre qu'il n'a pas donné. Marque-le comme question ouverte.
- **D'inventer un module** pour un autre type de produit que le logiciel ou la vidéo.

## La preuve

Une session ouverte à froid, à qui on donne seulement le PRD, construit le produit sans poser de
question sur le besoin, et sait quand elle a fini.

## Où sont les gabarits

Les fichiers `modeles/` cités ici vivent dans le dossier de ce skill, pas dans le projet. Copie le
gabarit dans le projet avant de le remplir, et ne modifie jamais l'original. Si une copie remplie
existe déjà dans le projet, c'est elle qui fait foi.
