# Changements

Une ligne par changement, la version la plus récente en haut.

**Chaque ligne commence par un titre en gras.** Lire les seuls titres doit suffire à savoir ce
qui a été ajouté, corrigé ou changé. Ce qui suit le titre est facultatif : une ou deux lignes au
maximum, et rien du tout quand le titre se suffit à lui-même.

Ce fichier est **destiné à être lu par un utilisateur** : ce qui s'y trouve décrit ce qui change
à l'écran ou dans l'usage, pas comment c'est écrit. Le détail technique vit dans
`docs/PHASE-N.md`, et les décisions dans `ARCHITECTURE.md`.

⚠️ **La source est l'anglais**, c'est `CHANGELOG.md`, comme l'interface et le README. Ce fichier-ci
en est la traduction, et les deux s'écrivent ensemble.

**Ce qui appartient à StreamyChat xD a sa propre section**, en fin de version. Tout le monde la
voit, y compris ceux qui sont sur l'édition gratuite : ce qu'une édition payante apporte mérite
d'être su avant de décider si on l'essaie.

Il alimente un panneau de la fenêtre de réglages : d'où la structure régulière : un titre
`## <version> - <date>`, puis des sections, puis des lignes courtes.

**Un numéro de version = une build distribuée** (CLAUDE.md, règle 13).

---

## Non publiée

### Corrigé

- **« Ajouter une langue » ouvre le dossier**, et le crée s'il n'est pas là. Il n'existe pas
  tant que rien ne le crée, donc les instructions envoyaient les gens vers un chemin que
  Windows disait introuvable.

---

## 0.9.0 - 25 août 2026

**StreamyChat parle anglais, et ta chaîne raconte ce qui s'y passe.**

⚠️ **Reconnecte-toi à Twitch au premier lancement** : six autorisations de plus, sans lesquelles
ta chaîne ne dira rien de ce qui s'y passe.

### Ajouté

- **Un menu de pseudos.** Photo de profil, couleur du pseudo, et depuis quand la personne a
  parlé. Tape `@` et il s'ouvre tout seul.
- **Il filtre pendant que tu tapes.** Tu ouvres sur « ge », tu continues avec « ek », la liste
  se réduit et ton texte ne bouge pas.
- **Un pseudo se trouve par le milieu.** « geek » propose aussi « LeGeeK ».
- **Les commandes à pseudo ouvrent ce menu.** `/ban`, `/timeout`, `/warn`, `/vip`, `/mod` et les
  autres, comme `/raid` ouvre celui des chaînes.
- **Ta chaîne raconte ce qui s'y passe.** Redeems, sondages, prédictions, hype trains, objectifs
  et coupures pub arrivent dans le chat.
- **Les shoutouts apparaissent.** Ceux que tu envoies, ceux que tu reçois, ceux des autres
  modos. Twitch n'en met aucun dans le chat : sans ça, ils n'existaient nulle part.
- **Les nouveaux follows aussi.** Sur ta chaîne et sur celles où tu es modérateur.
- **StreamyChat parle anglais.** La langue se choisit dans « Avancé » ; par défaut, elle suit
  celle de ton PC.
- **Tu peux ajouter ta langue.** Un fichier `.po` dans le dossier `lang` de tes données, puis tu
  relances. Une traduction incomplète retombe sur l'anglais.
- **StreamyChat se met à jour toute seule.** Elle vérifie au lancement, télécharge en arrière-plan
  et installe au redémarrage suivant.
- **Une section « À propos »**, avec ta version, le bouton de mise à jour et ce qu'apporte chaque
  version.
- **Un bouton « Signaler un bug ».** Il ouvre le formulaire sur GitHub, déjà rempli avec ta
  version, et pose le fichier de rapport dans un dossier à côté, prêt à glisser dedans.

### Corrigé

- **Le sélecteur d'emotes pouvait rester vide toute la session**, sur tous les onglets. Les
  emotes étaient chargées : c'est l'écran qui ne le savait pas.
- **Les pseudos sans couleur étaient tous blancs.** Ils prennent une couleur de Twitch dérivée
  du pseudo : la même d'une soirée à l'autre, comme sur le site.
- **Les emotes de la chaîne manquaient une fois sur deux** dans la section « Cette chaîne ».

### Changé

- **Les textes de modération emploient les mots de Twitch.** Un « timeout », un « ban », un
  « warn », comme les commandes, qui s'appelaient déjà comme ça.
- **Les six thèmes fournis gardent leur nom anglais.** Un nom de thème voyage avec le fichier
  que tu exportes : il reste le même quelle que soit la langue. Ton thème en cours n'est pas
  touché.
- **Plus de textes suivent la langue choisie.** L'âge d'un compte, les lignes de modération, les
  modes du salon, les messages de connexion, l'écran de connexion.
- **Les montants s'écrivent comme ta langue les écrit.** « 0,003 $ » en français, « $0.003 » en
  anglais.
- **Le nombre de chaînes ouvertes passe de 33 à 10.** L'ancien chiffre était faux : au-delà de
  la 11e, Twitch cessait de signaler les raids sans que rien ne le dise. Tes onglets sont tous
  rouverts.
- **Les emotes globales sont rangées par fournisseur** (Twitch, 7TV, BTTV, FFZ) au lieu d'une
  seule rubrique.
- **Les versions empaquetées s'affichent « Bêta », et plus « Alpha ».** L'application disait
  une chose et la page de téléchargement une autre.

### StreamyChat xD

- **Cinq sections de réglages au lieu de six.** « Corriger les messages » est passé en bas de
  « Voix », avec sa clé OpenRouter et son champ d'essai.
- **Le modèle et le prompt de correction ne se règlent plus.** StreamyChat répond de la qualité
  de la correction, donc il en règle les détails.
- **Les compteurs de dépense sont dans « Avancé »**, à côté du rapport de bug.

---

## 0.8.0 - 23 août 2026

**Tes onglets se déplacent à la souris.** Prends-en un et lâche-le où tu veux : ailleurs dans la
barre pour les remettre dans l'ordre, sur une autre fenêtre pour l'y envoyer, ou n'importe où en
dehors pour lui ouvrir sa propre fenêtre.

### Ajouté

- **Les onglets se déplacent à la souris.** Les remettre dans l'ordre, les faire passer d'une
  fenêtre à l'autre, ou en sortir un sur le bureau pour lui ouvrir sa propre fenêtre.
- **Un bouton « Remettre en place »** dans Réglages → Fenêtre. Il rend à tes fenêtres de chat
  leur taille de départ et les recentre.

### Corrigé

- **La croix de la barre de titre dit ce qu'elle fait.** « Quitter StreamyChat » sur la fenêtre
  principale, « Fermer cette fenêtre » sur les autres. Les deux affichaient « Fermer », alors
  qu'une seule est sans retour.
- **Fermer la fenêtre principale quitte pour de bon.** L'app restait en vie derrière tes autres
  fenêtres de chat, sans plus aucun moyen de faire revenir la principale.
- **Tes fenêtres de chat retrouvent leurs chaînes au redémarrage**, quand tu quittes par la
  croix de la principale.
- **La fenêtre peut enfin devenir aussi petite que son texte.** À 70 % de taille d'interface,
  elle descend à 208 px de large au lieu de 296.
- **Le bandeau de chaîne ne s'ouvre plus quand tu survoles le haut du fil.** Il ne réagit que
  juste au-dessus de lui, au niveau des onglets.

---

## 0.7.0 - 23 août 2026

**La recherche d'emotes trouve par le milieu du nom**, et Tab ne transforme plus tes mots en
images.

### Ajouté

- **La recherche d'emotes trouve enfin par le milieu du nom.** Taper `:sad` propose `peepoSad`
  et `FeelsBadMan`, là où il fallait connaître le début.
- **Tab sur un mot ordinaire ne complète plus que des pseudos.** Il proposait aussi des emotes,
  et transformait un mot de ta phrase en image. Pour une emote, tape `:`.
- **`Ctrl+E` ouvre le sélecteur d'emotes** quand tu es dans le champ d'écriture, comme sur
  Discord.

### Corrigé

- **La croix d'un onglet qui arrive sous la souris.** Fermer un onglet fait glisser le suivant
  sous un curseur qui n'a pas bougé ; sa croix n'apparaissait qu'après être sorti et revenu.
- **Le menu d'ajout de chaîne restait ouvert une seconde et demie** après le clic.

### À savoir

- **Le bandeau de raid n'a pas de compte à rebours, et il ne peut pas en avoir.** Twitch ne
  signale un raid qu'au moment où il **part**. Les quatre-vingt-dix secondes du site vivent
  dans le lecteur vidéo, sur un canal qui n'est pas public.

### StreamyChat xD

- **Les messages sont corrigés avant d'être lus à voix haute.** Abréviations, accents manquants,
  lettres étirées. Le texte devient prononçable sans changer ce qui était dit.
- **Un champ d'essai** dans les réglages, pour entendre la différence avant d'allumer.
- **Un curseur « Puissance de la voix »**, au-dessus du volume. Le volume ne fait que baisser le
  son ; celui-là le monte à la source.
- **Deux compteurs disent ce que tout ça coûte**, par session, par jour et en tout.
- **Un message déjà corrigé n'est jamais repayé**, même après un redémarrage.
- **Les émoticônes ne sont plus prononcées n'importe comment.** Un `x)` se faisait lire « ixe »
  au milieu d'une phrase. Elles deviennent une petite pause. `xD`, lui, reste.
- **La voix était beaucoup trop faible.** Elle sort maintenant environ **sept fois plus fort**.
- **Toutes les voix sortent au même niveau.** Changer de voix pouvait diviser ou multiplier le
  volume par vingt sans prévenir.
- **La liste des pseudos ignorés ne prenait pas de retour à la ligne.** Entrée ne faisait rien,
  il fallait coller le texte.
- **La correction est éteinte au départ**, et il faut une clé OpenRouter. Elle coûte de l'argent
  à chaque message et réécrit ce que les gens ont tapé : c'est à toi de décider.
- **Compte environ 17 centimes pour mille messages corrigés**, avant l'effet du cache.
- **Un troll qui essaie de piéger le modèle n'obtient rien.** Son message est corrigé comme les
  autres, ou lu tel qu'il l'a écrit.
- **Si la correction échoue, le message est lu tel quel.** Rien ne s'arrête et rien ne
  s'affiche : ton direct continue.

---

## 0.6.0 - 22 août 2026

**Le chat se lit à voix haute.** Tout ce qui suit est éteint au départ.

### StreamyChat xD

- **Les messages du chat peuvent être lus à voix haute**, par une voix Fish Audio.
- **Un bouton sur chaque message au survol**, et un raccourci que tu choisis, clic molette par
  défaut.
- **Choisis où le son sort.** Envoie la voix sur la sortie audio que tu veux.
- **Une page pour choisir ta voix** : filtre par langue, cherche, et écoute avant de choisir.
- **La lecture automatique, en option**, avec des filtres : abonnés, bits, longueur, pseudos
  ignorés.
- **Une barre dédiée** : elle dit ce qui se lit, et permet de passer ou de tout couper.
- **Les emotes ne sont pas prononcées**, donc un message qui n'est que des emotes n'est pas lu.
- **Les messages déjà lus ne sont pas repayés** : ils sont gardés sur ton PC un moment.

---

## 0.5.1 - 22 août 2026

**Ce que l'essai en direct de la 0.5.0 a fait remonter** : une session qu'on peut réparer, et
des messages qui parlent français.

### Ajouté

- **Une barre réclame une reconnexion** tant qu'il manque des autorisations, et ne part qu'une
  fois réglée.
- **« Se déconnecter » dans les réglages**, en bas à gauche, avec le compte connecté au-dessus.
- **La déconnexion retire aussi l'autorisation côté Twitch.**

### Corrigé

- **Les messages d'erreur ne parlent plus technique** : plus de noms d'autorisations, de codes,
  ni d'anglais.
- **Plus de bouton « Exclure » ou « Bannir » sur ses propres messages**, que Twitch refuse de
  toute façon.
- **`/vip` et `/mod` partent sur les chaînes que tu modères** : c'est Twitch qui décide, plus
  l'application.

---

## 0.5.0 - 22 août 2026

**La modération, de bout en bout** : sanctionner, lever, régler le salon, et savoir à qui on a
affaire avant de décider.

### Ajouté

- **Bannir, exclure, avertir, supprimer un message, purger le chat.**
- **`/ban`, `/timeout`, `/unban`, `/untimeout`, `/warn`, `/delete`, `/clear`.**
- **Les durées s'écrivent comme on les dit** : `/timeout bob 10m`, `1h`, `24h`.
- **Les modes du salon en commande** : `/slow`, `/followers`, `/subscribers`, `/emoteonly`,
  `/uniquechat`, et leur contraire.
- **`/vip`, `/unvip`, `/mod`, `/unmod`** sur ta propre chaîne.
- **Les modes du salon en un clic** dans le bandeau : lent, followers, abonnés, emotes, unique.
- **Une fiche au clic sur un pseudonyme** : photo, âge du compte, follow, ses messages.
- **Un compte créé il y a moins d'une heure est signalé en rouge**. C'est la signature d'un
  jetable.
- **La fiche propose d'exclure, bannir, et de lever une sanction en cours.**
- **Au survol d'un message** : supprimer, exclure, bannir, et un menu de durées.
- **Ces boutons n'apparaissent que sur les chaînes où tu peux modérer.**
- **Une commande mal tapée propose la bonne** au lieu de partir dans le chat.
- **Un badge de rôle que StreamyChat ne connaît pas encore s'affiche quand même.**
- ⚠️ **Une reconnexion à Twitch sera demandée** : trois autorisations de plus.

### Corrigé

- **La fenêtre principale garde son nom**, « StreamyChat », au lieu de prendre celui de l'onglet
  actif.
- **Le pseudonyme d'un message effacé s'ouvre en fiche** : on peut lever la sanction depuis le
  dépliant.

---

## 0.4.2 - 22 août 2026

**Plusieurs chaînes à la fois, dans plusieurs fenêtres**, et un flux fusionné qui les mêle
toutes.

### Ajouté

- **Une seule connexion Twitch partagée** : le plafond passe de 3 à 33 chaînes.
- **Toutes les fenêtres ont leur barre d'onglets et leur « + ».**
- **Une chaîne se déplace d'une fenêtre à l'autre** par le menu contextuel.
- **Fermer une fenêtre rend ses chaînes à la principale**, sans rien déconnecter.
- **Un onglet « Tout » dès deux chaînes** : tous les messages mêlés dans l'ordre d'arrivée.
- **Une photo et un liseré de couleur devant chaque ligne** pour dire sa chaîne.
- **Un message de chat partagé n'apparaît qu'une fois** dans le flux fusionné.
- **Un bandeau de chaîne** : titre du live, jeu, spectateurs, durée, suivi et abonnement.
- **La photo de la chaîne remplace la pastille** sur les onglets, estompée hors ligne.

### Corrigé

- **Le fil ne défile plus tout seul** quand on a remonté et que le tampon est plein.
- **Une nouvelle fenêtre s'ouvre à côté de celle qui a le focus**, pas sur l'autre écran.
- **Le menu du clic droit ne sort plus de la fenêtre.**
- **L'infobulle d'onglet ne se pose plus par-dessus le menu.**
- **Le clic-à-travers épingle la fenêtre**, et lui rend son épinglage d'avant en le coupant.
- **Le sélecteur d'emotes reste collé au champ de saisie.**
- **Échap sur `/raid` ou `/shoutout` ne bloque plus le menu de chaînes** pour la session.
- **Les versions empaquetées s'affichent « Alpha ».**

---

## 0.3.2 - 22 août 2026

### Corrigé

- **Le clic-à-travers épingle la fenêtre au premier plan**, et le réglage se range juste en
  dessous.
- **Échap sur `/raid` ou `/shoutout` ne bloque plus le menu de chaînes** pour la session.
- **Le sélecteur d'emotes reste collé au champ de saisie.**

---

## 0.3.1 - 22 août 2026

**La première version numérotée.** Elle rassemble tout ce qui existait alors : lecture du chat,
écriture, emotes tierces, apparence et transparence.

### Ajouté

- **Connexion à Twitch en trois clics**, sans coller de jeton.
- **Le chat en direct** : emotes, badges, couleurs de pseudonyme, réponses, liens, cheermotes.
- **Reconnexion automatique après une coupure réseau**, sans doublon.
- **Des onglets de chaînes**, avec photo, titre du live et compteur de non-lus.
- **Une chaîne se sort dans sa propre fenêtre.**
- **Les messages d'une personne sanctionnée se replient**, et se rouvrent au clic.
- **Les levées de bannissement et d'exclusion sont annoncées.**
- **Un champ d'écriture avec brouillon et historique par chaîne.**
- **Les réponses à un message**, au survol ou au clavier.
- **L'autocomplétion des pseudonymes, emotes, commandes et chaînes.**
- **Un sélecteur d'emotes à quatre sections**, qui retient les récentes.
- **`/me`, `/announce`, `/shoutout`, `/raid` et `/unraid`.**
- **Un salon en mode « abonnés » ou « followers » ferme le champ et dit pourquoi.**
- **7TV, BetterTTV et FrankerFaceZ**, globales et par chaîne.
- **Les emotes superposées (zero-width).**
- **Les emotes animées peuvent être figées.**
- **Un éditeur de thème** : couleurs, polices, densité, tailles.
- **Six thèmes fournis**, et l'export/import en `.json`.
- **La taille de l'interface et celle du texte sont réglables.**
- **L'opacité de la fenêtre et celle du fond, séparément.**
- **Le clic-à-travers** : les clics passent au chat vers ce qu'il y a derrière.
- **Une fenêtre sans cadre**, un liseré de fenêtre active, des coins arrondis.
