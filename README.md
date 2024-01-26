# Projet 5 d'OpenClassrooms : Nina Carducci, photographe

Bienvenue sur mon repository GitHub destiné à la réalisation du projet 5 de la formation de développeur web OpenClassrooms : « Débuggez et optimisez un site de photographe »

## Contexte

Ce projet consiste à reprendre le site de Nina Carducci, photographe, de l'optimiser et de le débugger.

### Débuggage

La première partie de l'intervention concerne le débuggage de la galerie. La sélection des catégories ne fonctionne pas et l'affichage en modale des photos choisies ne permet pas de circuler de l'une à l'autre.

Pour la partie concernant la sélection de catégories, c'était simplement un oubli d'ajouter la classe CSS "active" lors de la sélection du filtre voulu.

La sélection des photos a été faite différemment. Le code a été revu pour être plus petit, plus simple à maintenir et plus lisible :

- Le paramètre lightboxId a été rajouté dans les fonctions pour spécifier l'id et éviter un problème en cas de présence de plusieurs modales
- On utilise la fonction filter pour obtenir galleryItems, donc en créant un tableau avec tous les éléments
- On anticipe le début ou la fin de la galerie avec la gestion de l'index en faisant attention que le tableau de galleryItems commence à 0 là où galleryItems.length donnerait la longueur totale d'entrées. Être à la première image et aller en arrière va ramener à la dernière image et inversement
- On gère l'index actuel grâce à la méthode findIndex qui permet de retrouver l'index de l'élément que l'on va afficher directement dans le tableau créé avec filter

### Optimisation

L'optimisation a été faite grâce à plusieurs points :

- L'utilisation de balises sémantiques
- La mise en place de photos moins lourdes avec un format adapté et un lazy loading
- La revue de l'accessibilité
- La mise en place d'une SEO efficace
- L'utilisation de ressources minifiées

### Résultats

- Google Rich Snippet ressort un résultat parfait
- Wave Evaluation Tool trouve 0 erreur, 0 alerte, 0 erreur de contraste
- Lighthouse met en avant un score de 92 en performance, 100 en accessibilité, Best Practices et SEO

## Contenu du projet

Vous retrouverez sur ce projet un fichier index.html ainsi que les assets qui vont comprendre Bootstrap, les fonts utilisées, les différentes images, les scripts, dont le CSS, et leurs versions minifiées.
## Auteur

- [@Nomera67 / Yan Rechtenstein](https://www.github.com/Nomera67)
