# La charte : ta marque en 3 fichiers

> En pratique : tape `/charte` dans Claude Code. Il t'interviewe, écrit les fichiers et te propose
> trois directions visuelles à comparer. Cette fiche explique **pourquoi** on fait comme ça.

## Pourquoi c'est indispensable

Sans charte, l'IA fait **la moyenne de tout ce qu'elle a vu** : c'est propre, mais générique, et
différent à chaque fois. En vidéo, c'est encore pire : chaque plan est généré à part, et à la fin
rien ne se ressemble.

La charte, c'est **la mémoire de ta marque**. Tu l'écris une fois, Claude la relit à chaque fois,
et tout ce qu'il produit (vidéos, visuels, textes, pages) a la même tête et la même voix.

Ça marche pour :

- une **marque** ou une entreprise ;
- une **app** ou un site ;
- une **chaîne vidéo** ou un compte sur les réseaux ;
- une simple **ambiance** (un mood) pour un projet perso.

---

## Les 3 fichiers

| Fichier | Question | Ce qu'il contient |
|---------|----------|-------------------|
| **SOUL.md** | Qui est la marque ? | Raison d'être, promesse, valeurs (avec ce qu'elles interdisent), personnalité, ce qu'elle n'est pas, le client |
| **VOICE.md** | Comment parle-t-elle ? | Le ton, ses mots, ses mots interdits, tu ou vous, la signature, des exemples par canal, les règles pour l'accroche, les sous-titres et la voix off |
| **DESIGN.md** | À quoi ressemble-t-elle ? | Couleurs, polices, formes, mise en page, composants, et pour la vidéo : formats, rythme, mouvement, sous-titres, prompt de style |

Ils vont dans `docs/marque/` du projet. Le `CLAUDE.md` dit à Claude de les lire avant toute
création.

## Pourquoi dans cet ordre : l'âme, puis la voix, puis le visuel

L'erreur classique, c'est de commencer par les couleurs (« je veux du bleu et du noir »). Mais une
couleur ne veut rien dire toute seule. **Elle se justifie par une personnalité.** Une marque
« coach exigeant, direct et drôle » n'a pas les mêmes couleurs qu'une marque « grande sœur
bienveillante ».

Donc :

1. **SOUL** fixe qui on est.
2. **VOICE** en découle : quelqu'un de direct parle court.
3. **DESIGN** en découle aussi : quelqu'un de direct a des formes nettes, peu de décoration, et une
   couleur d'action franche.

Quand tout découle du même endroit, tout se ressemble, même ce que tu n'avais pas prévu.

---

## Comment Claude la construit (le skill `/charte`)

1. **L'interview** : 4 groupes de 3 questions (le pourquoi, la personnalité, le client, l'univers).
   Si tu réponds « je sais pas », il propose une valeur et te demande de confirmer.
2. **SOUL.md et VOICE.md** : il les écrit, et tu les relis.
3. **Trois directions visuelles**, chacune dans un fichier HTML que tu ouvres dans ton navigateur
   (palette, polices, et des images clés de vidéo ou un écran d'app). Elles sont **vraiment
   différentes** : pas trois fois la même page en trois couleurs.
4. **Tu choisis**, ou tu mélanges (« la palette de A avec les formes de C »).
5. **DESIGN.md** : il écrit la direction retenue, avec les valeurs exactes.
6. **Les variantes**, si tu veux : mode sombre, version TikTok, campagne d'été. Une variante ne
   change qu'une chose et garde tout le reste.

## Le secret : puiser dans l'univers, pas dans le web

Les meilleures chartes viennent **du métier ou du monde de la marque** : ses matières, ses outils,
ses lieux, ses vêtements, son vocabulaire. Une salle d'escalade peut prendre la magnésie, les cordes,
les prises colorées. Une marque de café peut prendre le papier kraft, la vapeur, le
tampon.

À l'inverse, les « codes du web » (dégradé violet, fond crème avec un serif, gros chiffre en
vedette) donnent des marques que tout le monde a déjà vues. La liste des pièges est dans le modèle
`DESIGN.md`.

---

## Spécial vidéo

Une charte pour la vidéo doit préciser ce qu'une charte web oublie :

- **Les formats** : 9:16 pour les réseaux, 16:9 pour YouTube, 1:1 pour certains posts.
- **Les zones de sécurité** : en vertical, le bas et la droite sont cachés par les boutons du réseau.
- **Le texte à l'écran** : la taille minimum, le nombre de mots par ligne, la durée d'affichage.
- **Les sous-titres** : la police, la position, et la couleur du mot prononcé.
- **Le rythme et le mouvement** : la durée d'un plan, la façon d'entrer et de sortir, ce qui est
  interdit.
- **Le son** : l'ambiance de la musique et le type de voix off.
- **Le prompt de style** : un paragraphe à coller à la fin de **chaque** prompt Veo, Kling ou
  Runway. C'est ce qui fait que tous les plans générés se ressemblent.

Avec HyperFrames (fiche 6), la charte devient directement du code : les couleurs et les polices de
`DESIGN.md` sont celles de la vidéo. HyperFrames a même un format, `frame.md`, qui traduit un
`DESIGN.md` pour la caméra.

---

## Pour aller plus loin

- Le format DESIGN.md de Google : https://github.com/google-labs-code/design.md
- Des dizaines de DESIGN.md de marques connues, pour s'inspirer : https://github.com/VoltAgent/awesome-design-md
- Des chartes graphiques réelles : https://brandingstyleguides.com
