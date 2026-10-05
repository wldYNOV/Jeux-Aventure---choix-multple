## Contenu

- **14 vraies pages HTML** : l’accueil est la première scène, suivie de 9 scènes et de 4 dénouements.
- Deux boutons de choix sur chaque page, y compris des liens de rejouabilité dans les dénouements.
- Une feuille de style commune, six icônes SVG et une illustration locale.
- Quatre issues : libération, sacrifice, disparition et départ.
- Un arbre de navigation de trois pages : vue d’ensemble, détails des choix et liens de retour.
- Mise en page adaptative, animation d’apparition et effets au survol.
- Navigation au clavier, focus visible, lien d’évitement, langue déclarée et respect de la réduction des animations.

## Organisation des fichiers

```text
nom-tp-web/
├── index.html
├── style.css
├── pages/
│   ├── scene01.html
│   ├── ...
│   └── scene13.html
├── assets/
│   ├── backgrounds/
│   │   └── ker-is.webp
│   └── icons/
│       ├── book.svg
│       ├── compass.svg
│       ├── key.svg
│       ├── moon.svg
│       ├── spark.svg
│       └── wave.svg
├── arbre-navigation.pdf
└── README.md
```

## Comprendre le code

Chaque page suit la même structure : `header`, `main`, une `section` narrative, une `nav` contenant les choix, une `aside` d’ambiance et un `footer`. La navigation repose sur de vrais liens `<a href="…">` ; leur classe `choice` leur donne une apparence de bouton.

Depuis `index.html`, les scènes sont dans `pages/`. Depuis une scène, `../` remonte au dossier principal : par exemple `../style.css` ou `../index.html`. Les icônes sont décoratives : leur attribut `alt` est vide, car le libellé du bouton décrit déjà l’action.

`style.css` est organisé en six sections : palette, en-tête et pied de page, mise en page, boutons, ambiances, adaptation aux écrans et accessibilité. Les variables `--ink`, `--paper` et `--copper` centralisent les couleurs. Les variantes `theme-coast`, `theme-village`, `theme-depth`, `theme-tower` et `theme-dawn` modifient l’atmosphère.

Le fond est fourni en WebP pour limiter le poids. Les polices système évitent tout chargement extérieur. Les icônes sont des fichiers SVG simples et lisibles. Il n’y a pas de JavaScript, d’inventaire, de score ou de musique : la navigation seule fait progresser l’histoire.

## Logique narrative

Les itinéraires se rejoignent parfois, mais les détours permettent de découvrir d’autres indices et d’accéder à des issues différentes. Aucun choix ne dépend d’un objet conservé implicitement : les informations et le matériel nécessaires sont présents dans la scène où ils sont utilisés. Les libellés « Revoir… » dans les fins proposent volontairement de rejouer une décision.

Exemples de parcours (attention, révélations) :

- Libération : `00 → 02 → 06 → 08 → 10`.
- Sacrifice : `00 → 01 → 04 → 09 → 11`.
- Disparition : `00 → 02 → 05 → 12`.
- Départ : `00 → 01 → 04 → 09 → 13`.

`00` correspond à `index.html` ; les autres numéros correspondent aux fichiers `pages/sceneXX.html`.

## Vérifications réalisées

- Présence des 14 pages et des deux choix par page.
- Résolution de tous les liens et des ressources locales.
- Accessibilité de toutes les scènes depuis le départ.
- Accessibilité des quatre fins et absence de voie narrative sans issue.
- Correspondance des liens HTML avec les transitions du PDF.
- Contrôle visuel des trois pages du PDF.

La mise en page adaptative est prévue dans le CSS. Une vérification visuelle dans le navigateur de rendu du cours reste à faire.

## Dépôt Git et remise

Renommer le dossier et le dépôt **votre-nom-tp-web**, en remplaçant `votre-nom` par le nom demandé par l’établissement. Placer directement `index.html`, `style.css`, `pages/`, `assets/`, le PDF et ce README à la racine du dépôt.

Dans le dossier décompressé :

```bash
git init
git add .
git commit -m "Créer le jeu Le Phare des âmes"
git branch -M main
```

Créer ensuite un dépôt vide sur la plateforme Git choisie, y relier le dépôt local et envoyer la branche `main`. Déposer le lien du dépôt sur Vimtrack selon les consignes du cours. La création du dépôt scolaire et la soumission sur Vimtrack ne sont pas effectuées par ce dossier.

## Crédits et transparence

Histoire, HTML/CSS et icônes créés avec l’assistance de ChatGPT. Illustration originale générée avec l’outil de génération d’images d’OpenAI. Aucun média issu d’Unsplash, de Font Awesome ou de Freesound. Ker-Is et ses personnages sont fictifs ; les coordonnées affichées servent à l’ambiance.

Ce projet a été préparé avec une assistance IA à la demande de l’utilisateur. Respecter les règles de l’établissement concernant cette assistance et être capable d’expliquer les fichiers remis.
